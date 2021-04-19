---
description: 撰寫安全的提供者需要考慮提供者的裝載方式、提供者如何處理模擬，以及確保檢查使用者是否有資料的存取權限。
ms.assetid: 9a8b7730-cbb8-48fa-8a8f-8e551f00d20b
ms.tgt_platform: multiple
title: 保護您的提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6b8fef1e90f09bc09488c058240b7fd1a88ebd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971717"
---
# <a name="securing-your-provider"></a><span data-ttu-id="9d5cf-103">保護您的提供者</span><span class="sxs-lookup"><span data-stu-id="9d5cf-103">Securing Your Provider</span></span>

<span data-ttu-id="9d5cf-104">撰寫安全的提供者需要考慮提供者的裝載方式、提供者如何處理模擬，以及確保檢查使用者是否有資料的存取權限。</span><span class="sxs-lookup"><span data-stu-id="9d5cf-104">Writing a secure provider requires considering how the provider is hosted, how the provider handles impersonation, and ensuring that users are checked for access rights to data.</span></span> <span data-ttu-id="9d5cf-105">您可以藉由要求資料先經過加密驗證，再透過網路傳送，來保護提供者命名空間中的資料。</span><span class="sxs-lookup"><span data-stu-id="9d5cf-105">You can secure the data in your provider namespace by requiring that data be encrypted authentication before sending it over a network.</span></span> <span data-ttu-id="9d5cf-106">如需詳細資訊，請參閱 [要求命名空間的加密連接](requiring-an-encrypted-connection-to-a-namespace.md)。</span><span class="sxs-lookup"><span data-stu-id="9d5cf-106">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

<span data-ttu-id="9d5cf-107">如果使用者具有任何命名空間的 **完整 \_ 寫入** 存取權，則使用者可以針對命名空間中限制使用者的資料，建立跨命名空間訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d5cf-107">If a user has **FULL\_WRITE** access in any namespace, then the user can create cross-namespace subscriptions for data in a namespace in which the user is restricted.</span></span> <span data-ttu-id="9d5cf-108">因為提供者可以載入至任何命名空間，並且在任何安全性內容中執行，所以提供者應該執行它自己的存取檢查，以確保只有獲得授權的使用者可以存取資料或執行方法。</span><span class="sxs-lookup"><span data-stu-id="9d5cf-108">Because a provider can be loaded into any namespace and be executing in any security context, the provider should perform its own access checks to ensure that only authorized users are allowed access to data or to execute methods.</span></span> <span data-ttu-id="9d5cf-109">如需詳細資訊，請參閱 [執行存取檢查](performing-access-checks.md)。</span><span class="sxs-lookup"><span data-stu-id="9d5cf-109">For more information, see [Performing Access Checks](performing-access-checks.md).</span></span>

<span data-ttu-id="9d5cf-110">下列主題討論提供者安全性：</span><span class="sxs-lookup"><span data-stu-id="9d5cf-110">The following topics discuss provider security:</span></span>

-   [<span data-ttu-id="9d5cf-111">提供者裝載和安全性</span><span class="sxs-lookup"><span data-stu-id="9d5cf-111">Provider Hosting and Security</span></span>](provider-hosting-and-security.md)
-   [<span data-ttu-id="9d5cf-112">執行存取檢查</span><span class="sxs-lookup"><span data-stu-id="9d5cf-112">Performing Access Checks</span></span>](performing-access-checks.md)
-   [<span data-ttu-id="9d5cf-113">用來控制提供者安全性的登錄機碼</span><span class="sxs-lookup"><span data-stu-id="9d5cf-113">Registry Keys for Controlling Provider Security</span></span>](registry-keys-for-controlling-provider-security-.md)
-   [<span data-ttu-id="9d5cf-114">存取 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="9d5cf-114">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
-   [<span data-ttu-id="9d5cf-115">模擬用戶端</span><span class="sxs-lookup"><span data-stu-id="9d5cf-115">Impersonating a Client</span></span>](impersonating-a-client.md)

<span data-ttu-id="9d5cf-116">下列主題將討論用戶端和腳本如何與提供者安全性互動：</span><span class="sxs-lookup"><span data-stu-id="9d5cf-116">The following topics discuss how clients and scripts interact with provider security:</span></span>

-   [<span data-ttu-id="9d5cf-117">在 WMI 中設定驗證</span><span class="sxs-lookup"><span data-stu-id="9d5cf-117">Setting Authentication in WMI</span></span>](setting-authentication-in-wmi.md)
-   [<span data-ttu-id="9d5cf-118">在不同的作業系統間連接</span><span class="sxs-lookup"><span data-stu-id="9d5cf-118">Connecting Between Different Operating Systems</span></span>](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)
-   [<span data-ttu-id="9d5cf-119">使用 VBScript 設定預設進程安全性等級</span><span class="sxs-lookup"><span data-stu-id="9d5cf-119">Setting the Default Process Security Level Using VBScript</span></span>](setting-the-default-process-security-level-using-vbscript.md)
-   [<span data-ttu-id="9d5cf-120">設定用戶端應用程式處理安全性</span><span class="sxs-lookup"><span data-stu-id="9d5cf-120">Setting Client Application Process Security</span></span>](setting-client-application-process-security.md)

## <a name="related-topics"></a><span data-ttu-id="9d5cf-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="9d5cf-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d5cf-122">維護 WMI 安全性</span><span class="sxs-lookup"><span data-stu-id="9d5cf-122">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="9d5cf-123">使用 WMI</span><span class="sxs-lookup"><span data-stu-id="9d5cf-123">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 
