### Setup link:  
In the O11y platform.

### Right after setup:  
```bash
systemctl status splunk-otel-collector
```

### Network connectivity test:  
```bash
curl -o - -I https://ingest.<realm>.signalfx.com/v2/datapoint
```

### Errors might be:  
- User permissions/sudo  
- Firewall  
- Insufficient  

### After fixing installation errors:  
```bash
sudo sh /tmp/splunk-otel-collector.sh --uninstall
```

### Check system journal for errors from Splunk OTel collector:  
```bash
journalctl -t otelcol -r
```

### Restart the agent:  
```bash
sudo systemctl restart splunk-otel-collector
```
