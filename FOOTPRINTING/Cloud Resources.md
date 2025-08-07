## CLOUD RESOURCES

Use of cloud such as `AWS`, `Google GCP`, `Azure` and others are now essential components.

Even though cloud provider secure their infra. centrally this doesn't mean that companies are free from vulnerabilities.

This often starts with S3 bucket, blob, cloud storage which can be accessed without authentication.

## Company Hosted Server

```
NiteshKS22@htb[/htb]$ for i in $(cat subdomainlist);do host $i | grep "has address" | grep inlanefreight.com | cut -d" " -f1,4;done

blog.inlanefreight.com 10.129.24.93
inlanefreight.com 10.129.27.33
matomo.inlanefreight.com 10.129.127.22
www.inlanefreight.com 10.129.127.33
s3-website-us-west-2.amazonaws.com 10.129.95.250
```

Often Cloud Storage is added to DNS when used for admin purpose by other employee.

We can also search cloud storage using google search combined with `google Dork`

<img width="1354" height="420" alt="image" src="https://github.com/user-attachments/assets/71f43071-3eab-4d96-a160-8db0af75a30d" />
<img width="1354" height="437" alt="image" src="https://github.com/user-attachments/assets/c71601db-5383-4404-98d9-e75788c40f27" />

result can be PDF, PPT, codes, and many more

we can also use 3rd party tool -- `domain.glass` this can also tell a lot about company infra.

## domain.glass

<img width="1298" height="808" alt="image" src="https://github.com/user-attachments/assets/b959bf70-a85a-4435-9ce2-76bd264e349f" />

`here see that Cloudflare's security assessment status has been classified as "Safe". This means we have already found a security measure that can be noted for the second layer (gateway).`

Another tool that can be usefull `GrayHatWarfare` 

## grayhatwarfare
<img width="1404" height="785" alt="image" src="https://github.com/user-attachments/assets/c153b61e-9023-4935-a97b-0d76ad5e9ad4" />

many company can also use abbreviations of the company name.

## public and private SSH keys Leaked

<img width="1410" height="192" alt="image" src="https://github.com/user-attachments/assets/283c274b-b35e-4c5e-a441-d6e5a1394e91" />

Sometimes miconfiguration can lead to leaked SSH KEYs

<img width="1024" height="493" alt="image" src="https://github.com/user-attachments/assets/d75ae598-e709-48db-b74f-42419728014a" />
