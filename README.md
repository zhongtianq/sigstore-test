# sigstore-test
test github sigstore 

## cosign工具blob签发、验证

```bash
cosign sign-blob test.txt --bundle cosign.bundle
```

```bash
cosign verify-blob test.txt --bundle cosign.bundle --certificate-identity=zhongtian.qzt@antgroup.com --certificate-oidc-issuer=https://github.com/login/oauth
```

## 查看rekor
```bash
curl -X 'GET' \
  'https://rekor.sigstore.dev/api/v1/log/entries?logIndex=269822714' \
  -H 'accept: application/json'
```
