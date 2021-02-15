---
title: EGo - Build confidential Go apps with ease​
claim: Build Confidential Go Apps with Ease​
description: EGo enables you to build and run Go code for Intel&reg; SGX enclaves with zero code changes.​

why:
  title: Why EGo
  description:
    Confidential computing enables the always-encrypted and verifiable processing of data - in the cloud and elsewhere. It is a breakthrough approach that solves many security and privacy problems.


    Developing confidential apps used to require arcane knowledge, significant code changes, and cumbersome build steps. With EGo, you can skip that and develop your Go code as usual.


    In the video above, [Visual Studio Code](https://code.visualstudio.com/) is used to debug unmodified [HashiCorp Vault](https://www.vaultproject.io/) running on EGo in an Intel&reg; SGX enclave in debug mode.
  image: "text_only.svg"
  points:
    - Build, debug, and run Go apps as usual
    - Have all the benefits of confidential computing
    - Permissive open-source license (MPL-2)​

howToUse:
  title: How to Use​
  description: >
    With EGo, you don't need to refactor your app to run it in a secure enclave. Just use three simple commands to build, sign, and run your code - be it 10 or 100,000 lines of Go with complex dependencies.


    **Want to scale your confidential app?** [Marblerun](https://marblerun.sh/) - "the service mesh for confidential computing" - has native support for EGo-based microservices and makes it easy to securely scale confidential apps on [Kubernetes](https://kubernetes.io).


    **Want to use Intel&reg; SGX features like sealing or remote attestion?** Easy! Just import EGo's [enclave library](https://pkg.go.dev/github.com/edgelesssys/ego@v0.1.0/enclave#section-documentation) and access everything in a single line of code. For example, get an attestation report for your TLS certificate:


    `r, err := enclave.GetRemoteReport(sha256.Sum256(cert)[:])`

features:
  heading: Features
  items:
    - title: Super secure
      icon: fas fa-lock
      description:
        All your data and code are kept inside the secure enclaves at runtime. No need to partition your app.
    - title: Easy to use
      icon: fas fa-keyboard
      description:
        Start by lifting & shifting your existing Go code without changing a line. Use the EGo runtime library to effortlessly access SGX-specific features.
    - title: Easy to scale
      icon: fas fa-rocket
      description: >
        [Marblerun](https://marblerun.sh/) has native support for EGo-based microservices and makes it easy to scale them securely on Kubernetes.
    - title: Built on industry standards
      icon: fas fa-layer-group
      description:
        EGo builds upon the industry standard [Open Enclave](https://openenclave.io/). This makes it future-proof and portable to other hardware platforms. EGo also supports the latest [DCAP](https://github.com/intel/SGXDataCenterAttestationPrimitives) attestation protocol.
    - title: Runs everywhere
      icon: fas fa-running
      description:
        Don't have SGX-enabled hardware? No problem! EGo apps run in simulation mode on any host. Also, many cloud providers already offer SGX-enabled VMs.
    - title: Lightweight
      icon: fas fa-feather
      description:
        EGo does not try to simulate a full POSIX environment in your enclave. It just loads as much code as necessary for the Go runtime to work well, keeping the trusted computing base (TCB) small.

banner:
  heading: Want to build confidential Go apps?​
  button:
    title: Get started →
    href: https://github.com/edgelesssys/ego#quick-start

blog:
  title: Blog
  items:
    - title: "[The Open-Source Landscape of Confidential Computing in 2021](https://medium.com/edgelesssystems/the-open-source-landscape-of-confidential-computing-in-2021-7f847ebfc0a9)"
      description: We give an overview of the open-source landscape in confidential computing and show where EGo fits in.

    - title: "[4 Use Cases for Confidential Computing](https://medium.com/edgelesssystems/4-use-cases-for-confidential-computing-34f62e77a4de)"
      description: We discuss specialized use cases for confidential computing that can be realized with EGo.

    - title: "[We’re Hosting the Open Confidential Computing Conference 2021!](https://medium.com/edgelesssystems/were-hosting-the-open-confidential-computing-conference-2021-72a847223bd1)"
      description: Come join us for free on March 11 and learn more about EGo and other exciting open-source projects for confidential computing!

    - title: "[Why Do We Need Confidential Computing?](https://medium.com/edgelesssystems/why-we-need-a-service-mesh-for-confidential-computing-part-1-3-28f4bd6df679)"
      description: We give an intro to the basics of confidential computing.

useCases:
  title: Use Cases for Confidential Computing ​
  items:
    - title: Privacy-preserving ML deployment​
      icon: fas fa-lock
      description:
        CC applications can ensure that different parties, who feed a ML model, cannot access the raw data.​ Processing takes place in secure enclaves and only the analysis results are played out to the participating parties.
    - title: Fraud detection​
      icon: fas fa-lock
      description:
        Through CC, companyies can cross-check their customer and transaction data for potential fraud while neither of them gets access to the original data. The privacy of their customers sensitive data is ensured by CC alongside the whole process.
    - title: Mobility data pooling​
      icon: fas fa-lock
      description:
        With CC, data from vehicles can be processed in an end-to-end encrypted and verifiable way. Even the vehicle manufacturer only get access to the aggregated and filtered output data. It can be mathematically ensured that no relevant conclusions can be drawn from the output data about individual drivers.
    - title: Disease recognition​
      icon: fas fa-lock
      description:
        When it comes to patient data in healthcare, one is clearly dealing with highly sensitive and regulated data. In this context, CC can enable secure multi-party training of AI for different purposes, e.g. cancer recognition.

---
