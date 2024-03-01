HAProxy Web Application Firewall
<h1>
  <img src="https://coraza.io/images/logo_shield_only.png" align="left" height="46px" alt=""/>
  <span>Coraza SPOA - HAProxy Web Application Firewall</span>
</h1>
Coraza SPOA is a system daemon which brings the Coraza Web Application Firewall (WAF) as a backing service for HAProxy. It is written in Go, Coraza supports ModSecurity SecLang rulesets and is 100% compatible with the OWASP Core Rule Set v4.

HAProxy includes a [Stream Processing Offload Engine](https://www.haproxy.com/blog/extending-haproxy-with-the-stream-processing-offload-engine) [SPOE](https://raw.githubusercontent.com/haproxy/haproxy/master/doc/SPOE.txt) to offload request processing to a Stream Processing Offload Agent (SPOA). Coraza SPOA embeds the [Coraza Engine](https://github.com/corazawaf/coraza), loads the ruleset and filters http requests or application responses which are passed forwarded by HAProxy for inspection.