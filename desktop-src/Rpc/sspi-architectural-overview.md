---
title: SSPI 架構總覽
description: SSPI 是軟體介面。
ms.assetid: 2497afea-33dd-45ae-891b-bacf390ef338
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910cef52def2f398606fd541b8ed170f7e216078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023822"
---
# <a name="sspi-architectural-overview"></a><span data-ttu-id="7cff1-103">SSPI 架構總覽</span><span class="sxs-lookup"><span data-stu-id="7cff1-103">SSPI Architectural Overview</span></span>

<span data-ttu-id="7cff1-104">SSPI 是軟體介面。</span><span class="sxs-lookup"><span data-stu-id="7cff1-104">SSPI is a software interface.</span></span> <span data-ttu-id="7cff1-105">分散式程式設計程式庫（例如 RPC）可以使用它來進行驗證通訊。</span><span class="sxs-lookup"><span data-stu-id="7cff1-105">Distributed programming libraries such as RPC can use it for authenticated communications.</span></span> <span data-ttu-id="7cff1-106">一或多個軟體模組提供實際的驗證功能。</span><span class="sxs-lookup"><span data-stu-id="7cff1-106">One or more software modules provide the actual authentication capabilities.</span></span> <span data-ttu-id="7cff1-107">每個模組（稱為安全性支援提供者 (SSP) ）會實作為動態連結程式庫 (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="7cff1-107">Each module, called a security support provider (SSP), is implemented as a dynamic link library (DLL).</span></span> <span data-ttu-id="7cff1-108">SSP 會提供一或多個安全性套件。</span><span class="sxs-lookup"><span data-stu-id="7cff1-108">An SSP provides one or more security packages.</span></span>

<span data-ttu-id="7cff1-109">有各種不同的 Ssp 和套件可供使用。</span><span class="sxs-lookup"><span data-stu-id="7cff1-109">A variety of SSPs and packages are available.</span></span> <span data-ttu-id="7cff1-110">Windows 隨附的是 NTLM 安全性套件和 Microsoft Kerberos 通訊協定安全性封裝。</span><span class="sxs-lookup"><span data-stu-id="7cff1-110">Windows ships with the NTLM security package and the Microsoft Kerberos protocol security package.</span></span> <span data-ttu-id="7cff1-111">此外，您可以選擇安裝安全通訊端層 (SSL) 安全性封裝，或任何其他與 SSPI 相容的 SSP。</span><span class="sxs-lookup"><span data-stu-id="7cff1-111">In addition, you may choose to install the Secure Socket Layer (SSL) security package, or any other SSPI-compatible SSP.</span></span>

<span data-ttu-id="7cff1-112">使用 SSPI 可確保無論您選取哪一個 SSP，您的應用程式都能以一致的方式存取驗證功能。</span><span class="sxs-lookup"><span data-stu-id="7cff1-112">Using SSPI ensures that no matter which SSP you select, your application accesses the authentication features in a uniform manner.</span></span> <span data-ttu-id="7cff1-113">這項功能可讓您的應用程式比過去所提供的網路更有更大的獨立性。</span><span class="sxs-lookup"><span data-stu-id="7cff1-113">This capability provides your application greater independence from the implementation of the network than was available in the past.</span></span>

<span data-ttu-id="7cff1-114">分散式應用程式會透過 RPC 介面進行通訊。</span><span class="sxs-lookup"><span data-stu-id="7cff1-114">Distributed applications communicate through the RPC interface.</span></span> <span data-ttu-id="7cff1-115">接著，RPC 軟體會透過 SSPI 存取 SSP 的驗證功能。</span><span class="sxs-lookup"><span data-stu-id="7cff1-115">The RPC software in turn, accesses the authentication features of an SSP through the SSPI.</span></span>

<span data-ttu-id="7cff1-116">如需詳細資訊，請參閱 [SSPI](/windows/desktop/SecAuthN/sspi)。</span><span class="sxs-lookup"><span data-stu-id="7cff1-116">For more information, see [SSPI](/windows/desktop/SecAuthN/sspi).</span></span>

 

 