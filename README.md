# try-sonarqube-api
Operations with sonarqube api

To run sonar analysis from gradle:
<pre>
./gradlew sonarqube \
  -Dsonar.host.url=http://localhost:9000 \
  -Dsonar.login=a4893b95baf5fbd69b7f2e8c209539c6d6c1d3dc \
  -Dsonar.verbose=true
</pre>

To fetch issues:
<pre>
curl -X GET \
-H "Cookie=_ga=GA1.1.1209645534.150651662…zGHRCFXIa7xkhx0qKvCaiNEfNhyaU" \
-H "x-xsrf-token=q2gqd0tg50lfgc4qjj0ia3om91" \
'http://localhost:9000/api/issues/search' \
--data-urlencode "s=FILE_LINE&resolved=false&ps=100&facets=severities,types&additionalFields=_all'"
</pre>
