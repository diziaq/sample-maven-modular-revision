This project is a sample for demonstration of Maven modular project issue.

### Prerequisites
1. use maven 3.6.1+
2. define parent project (`base`) version as ${revision} (see [docs](https://maven.apache.org/maven-ci-friendly.html))
3. define two child projects (`core`, `facade`) so that `facade` depends on `core`


### Problem description

- Command `mvn package` from root project works as expected - all submodules are being packaged
- Command `mvn package` from "./modules/facade" project fails with error
```
Failed to read artifact descriptor for sample.group:sample-core:jar:0.0.1:
Could not transfer artifact sample.group:sample-base:pom:${revision}
```

---

See related question https://stackoverflow.com/questions/65263905
