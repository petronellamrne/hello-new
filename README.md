# hello-new
apiVersion: networking.istio.io/v1alpha3 kind: VirtualService metadata:   name: ratings spec:   hosts:   - ratings   http:   - fault:       delay:         percentage:           value: 0.1         fixedDelay: 5s     route:     - destination:         host: ratings         subset: v1
