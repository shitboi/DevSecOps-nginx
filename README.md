THIS IS THE UNSCANNED VERSION OF THIS APPLICATION
(See scanned, remediated and with-actions versions)
```
docker scout cves $APP_NAME:$VERSION --output ./vulns.report
docker scout cves $APP_NAME:$VERSION --only-severity critical --exit-code
docker scout sbom --output $APP_NAME.sbom $APP_NAME:$VERSION


#TEST: Run the container
docker run -d -p 80:80 --name $APP_NAME webapp
```
