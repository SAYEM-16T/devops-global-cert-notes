ঠিক আছে 👍 নিচে **mkdir + প্রতিটা folder এর ভিতরে README.md add**—সব একসাথে করা কমান্ডটা দিলাম। তুমি 그대로 কপি–পেস্ট করে রান করতে পারো 👇

```bash
mkdir \
"11. IAM Introduction: Users, Groups, Policies" \
"12. IAM Users & Groups Hands On" \
"13. AWS Console Simultaneous Sign-in" \
"14. IAM Policies" \
"15. IAM Policies Hands On" \
"16. IAM MFA Overview" \
"17. IAM MFA Hands On" \
"18. AWS Access Keys, CLI and SDK" \
"19. AWS CLI Setup on Windows" \
"20. AWS CLI Setup on Mac OS X" \
"21. AWS CLI Setup on Linux" \
"22. AWS CLI Hands On" \
"23. AWS CloudShell: Region Availability" \
"24. AWS CloudShell" \
"25. IAM Roles for AWS Services" \
"26. IAM Roles Hands On" \
"27. IAM Security Tools" \
"28. IAM Security Tools Hands On" \
"29. IAM Best Practices" \
"30. IAM Summary" \
"31. Quiz 1: IAM & AWS CLI Quiz" \
&& for d in */; do echo "# ${d%/}" > "$d/README.md"; done
```

🔹 এতে যা হবে:

* সব folder তৈরি হবে
* প্রতিটা folder এর ভিতরে `README.md` তৈরি হবে
* `README.md` এর ভিতরে automatically **folder name as title** বসে যাবে
* GitHub-এ push করার জন্য একদম ready ✅

চাও তো আমি README-র জন্য **standard DevOps / AWS learning template**ও বানিয়ে দিতে পারি 😉









