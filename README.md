# Lab 3 — hello-app on Kubernetes with Terraform

Name:Varsha H

Roll number:261100680003

## Part 1: first `terraform plan`

Paste the `Plan:` line and the summary above it.

```
Plan: 2 to add, 0 to change, 0 to destroy.
```

## Part 1: `terraform output -raw url`

```
http://localhost:8080/
```

## Part 2: plan for the v1 → v2 image change

Paste the lines that show the image change, and the `Plan:` line.

**In-place update**

```diff
~ update in-place
~ image = "shripada/hello-app:v1" -> "shripada/hello-app:v2"
```

> **Plan:** 0 to add, **1 to change**, 0 to destroy.

## Part 3: plan that found the drift after `kubectl scale`

```
  # kubernetes_deployment_v1.hello will be updated in-place
  ~ resource "kubernetes_deployment_v1" "hello" {
        id               = "default/hello-app"
        # (1 unchanged attribute hidden)

      ~ spec {
          ~ replicas                  = "5" -> "3"
            # (4 unchanged attributes hidden)

            # (3 unchanged blocks hidden)
        }

        # (1 unchanged block hidden)
    }

Plan: 0 to add, 1 to change, 0 to destroy.
```
## Part 4: `kubectl get svc -A` showing dev and prod

```

```

## Break it: the error after deleting `terraform.tfstate`

```

```

## Break it: the wrong selector

What did you see, and how did you find the cause? One or two sentences.



## Screenshot

Save a browser screenshot as `screenshot.png` in the repository root.
