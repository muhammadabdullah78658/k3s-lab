# K3s Lab

Hands-on lab for the Virtualization & K3s session.

## What you need
- An Ubuntu VM (2 CPU, 2 GB RAM, internet)
- Git: `sudo apt install -y git`

## Get the files
```bash
git clone <this-repo-url>
cd k3s-lab
```

## Files
| File | Used in | What it is |
|------|---------|------------|
| `lab-commands.txt` | All steps | Every command, in order. Copy one line at a time. |
| `hello.yml` | Step 1 | A Deployment with 3 nginx pods |
| `storage.yaml` | Step 2 | A PVC (disk request) + an app that uses it |
| `expose.yaml` | Step 3 | A Service + Ingress to open the app in a browser |
| `cafe.yaml` | Final project | Café menu app — **has 3 bugs for you to fix!** |

## Lab steps
1. **Install K3s** and run your first app
2. **Add storage** so data survives a pod restart
3. **Open it to the world** with Ingress
4. **Scale, break it, watch it heal**

## Final project: Café K3s
1. Make a namespace called `cafe`
2. Apply `cafe.yaml` — find and fix the 3 bugs
3. Write an Ingress so the menu opens in a browser
4. Add your own item to the menu (edit the ConfigMap)
5. Scale to 4 pods, delete one, show it comes back

**Stuck?** Use `kubectl get pods`, `kubectl describe pod <name>` and `kubectl logs <name>`.

## Tip
Always copy commands from `lab-commands.txt`, not from the slides.
