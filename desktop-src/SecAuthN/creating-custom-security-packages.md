---
description: 說明如何建立自訂安全性封裝。
ms.assetid: af8b9796-77e7-43c1-8f8e-acee01a62bf9
title: 建立自訂安全性套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2136775d18e9d33f59d1b1f44fd817b3f3271ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849900"
---
# <a name="creating-custom-security-packages"></a><span data-ttu-id="6a2fa-103">建立自訂安全性套件</span><span class="sxs-lookup"><span data-stu-id="6a2fa-103">Creating Custom Security Packages</span></span>

## <a name="ssp-security-packages"></a><span data-ttu-id="6a2fa-104">SSP 安全性封裝</span><span class="sxs-lookup"><span data-stu-id="6a2fa-104">SSP Security Packages</span></span>

<span data-ttu-id="6a2fa-105">如果自訂安全性支援提供者 (SSP) 安全性套件將專門用於用戶端/伺服器安全性支援，它可以執行 Microsoft [安全性支援提供者介面](sspi.md)。</span><span class="sxs-lookup"><span data-stu-id="6a2fa-105">If a custom security support provider (SSP) security package will be used exclusively for client/server security support it can implement the Microsoft [Security Support Provider Interface](sspi.md).</span></span>

<span data-ttu-id="6a2fa-106">SampSSP 範例隨附于平臺軟體發展工具組 (SDK) 包含範例 SSP 安全性封裝的執行。</span><span class="sxs-lookup"><span data-stu-id="6a2fa-106">The SampSSP sample shipped with the Platform Software Development Kit (SDK) contains a sample SSP security package implementation.</span></span>

## <a name="sspap-security-packages"></a><span data-ttu-id="6a2fa-107">SSP/AP 安全性套件</span><span class="sxs-lookup"><span data-stu-id="6a2fa-107">SSP/AP Security Packages</span></span>

<span data-ttu-id="6a2fa-108"> (ssp/ap 的自訂 [*安全性支援提供者*](/windows/desktop/SecGloss/s-gly) / [*驗證套件*](/windows/desktop/SecGloss/a-gly)) 包含可作為驗證套件的安全性套件 (ap) 以及 (ssp) 的安全性支援提供者。</span><span class="sxs-lookup"><span data-stu-id="6a2fa-108">Custom [*security support provider*](/windows/desktop/SecGloss/s-gly)/[*authentication packages*](/windows/desktop/SecGloss/a-gly) (SSP/APs) contain security packages that function as authentication packages (APs) and security support providers (SSPs).</span></span> <span data-ttu-id="6a2fa-109">這些套件會執行個別的 Api 來支援每個角色。</span><span class="sxs-lookup"><span data-stu-id="6a2fa-109">These packages implement separate APIs to support each role.</span></span>

<span data-ttu-id="6a2fa-110">因為它是做為 AP 的功能，所以自訂 SSP/AP [*安全性封裝*](/windows/desktop/SecGloss/s-gly) 必須針對 [驗證封裝所執行](authentication-functions.md)的所有函式提供執行。</span><span class="sxs-lookup"><span data-stu-id="6a2fa-110">Because it functions as an AP, a custom SSP/AP [*security package*](/windows/desktop/SecGloss/s-gly) must provide implementations for all of the [Functions Implemented by Authentication Packages](authentication-functions.md).</span></span>

<span data-ttu-id="6a2fa-111">為了提供整合式安全性支援，自訂的 SSP/AP 安全性套件必須提供 [SSP/ap 所執行](authentication-functions.md)之函式的執行。</span><span class="sxs-lookup"><span data-stu-id="6a2fa-111">To provide integrated security support, a custom SSP/AP security package must provide implementations for the [Functions implemented by SSP/APs](authentication-functions.md).</span></span> <span data-ttu-id="6a2fa-112">[由 ssp/ap 所呼叫的 LSA](authentication-functions.md) 函式描述可供 SSP/ap 開發人員使用的支援函式，這些開發人員需要與 LSA 互動。</span><span class="sxs-lookup"><span data-stu-id="6a2fa-112">[LSA Functions Called by SSP/APs](authentication-functions.md) describes the support functions available to the SSP/AP developers that want to interact with the LSA.</span></span>

<span data-ttu-id="6a2fa-113">SSP/AP 安全性封裝若要同時以 AP 和 SSP 的形式執行，則可作為作業系統的一部分執行，並做為使用者應用程式的一部分。</span><span class="sxs-lookup"><span data-stu-id="6a2fa-113">SSP/AP security packages, in order to perform as both an AP and an SSP, may execute as part of the operating system and as part of a user application.</span></span> <span data-ttu-id="6a2fa-114">這兩種執行模式分別稱為 LSA 模式和使用者模式。</span><span class="sxs-lookup"><span data-stu-id="6a2fa-114">These two modes of execution are known as LSA mode and user mode, respectively.</span></span> <span data-ttu-id="6a2fa-115">如需 LSA 模式的自訂安全性封裝的詳細資訊，請參閱 [Lsa 模式初始化](lsa-mode-initialization.md)。</span><span class="sxs-lookup"><span data-stu-id="6a2fa-115">For details about custom security packages in LSA mode see [LSA Mode Initialization](lsa-mode-initialization.md).</span></span> <span data-ttu-id="6a2fa-116">如需使用者模式的詳細資訊，請參閱 [使用者模式初始化](user-mode-initialization.md)。</span><span class="sxs-lookup"><span data-stu-id="6a2fa-116">For details about user mode, see [User Mode Initialization](user-mode-initialization.md).</span></span>

<span data-ttu-id="6a2fa-117">如果自訂的 SSP/AP 安全性封裝提供服務給用戶端/伺服器應用程式，它應該會提供 [使用者模式 SSP/ap 所執行](authentication-functions.md)之函式中所述函式的執行。</span><span class="sxs-lookup"><span data-stu-id="6a2fa-117">If a custom SSP/AP security package offers services for client/server applications it should provide implementations for the functions described in [Functions Implemented by User-mode SSP/APs](authentication-functions.md).</span></span> <span data-ttu-id="6a2fa-118">[使用者模式 SSP/ap 所呼叫的 LSA 函式](authentication-functions.md) 描述可供在用戶端或伺服器進程中執行的 SSP/AP 使用的支援功能。</span><span class="sxs-lookup"><span data-stu-id="6a2fa-118">[LSA Functions Called By User-mode SSP/APs](authentication-functions.md) describes the support functions available to an SSP/AP executing in a client or server process.</span></span>

<span data-ttu-id="6a2fa-119">如需註冊 SSP/AP DLL 的詳細資訊，請參閱 [註冊 ssp/ap](registering-ssp-ap-dlls.md)dll。</span><span class="sxs-lookup"><span data-stu-id="6a2fa-119">For information about registering an SSP/AP DLL, see [Registering SSP/AP DLLs](registering-ssp-ap-dlls.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a2fa-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="6a2fa-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a2fa-121">註冊和安裝安全性套件的限制</span><span class="sxs-lookup"><span data-stu-id="6a2fa-121">Restrictions around Registering and Installing a Security Package</span></span>](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
