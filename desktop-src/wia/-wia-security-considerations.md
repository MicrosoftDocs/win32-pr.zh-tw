---
description: 本檔提供與 Windows 映像取得 (WIA) 相關之安全性考慮的資訊。
ms.assetid: 35455320-7d08-49de-938d-40dc0873917b
title: 安全性考慮： Windows 映像取得
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ab080582492a0c03eab7879624bfb49a370e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973476"
---
# <a name="security-considerations-windows-image-acquisition"></a><span data-ttu-id="71188-103">安全性考慮： Windows 映像取得</span><span class="sxs-lookup"><span data-stu-id="71188-103">Security Considerations: Windows Image Acquisition</span></span>

<span data-ttu-id="71188-104">本檔提供與 Windows 映像取得 (WIA) 相關之安全性考慮的資訊。</span><span class="sxs-lookup"><span data-stu-id="71188-104">This document provides information about security considerations related to Windows Image Acquisition (WIA).</span></span> <span data-ttu-id="71188-105">本檔並不提供您需要瞭解的安全性問題，而是將其作為此技術領域的起點和參考。</span><span class="sxs-lookup"><span data-stu-id="71188-105">This document doesn't provide all you need to know about security issues - instead, use it as a starting point and reference for this technology area.</span></span>

-   [<span data-ttu-id="71188-106">使用引號括住路徑名稱</span><span class="sxs-lookup"><span data-stu-id="71188-106">Use quotation marks around path names</span></span>](#use-quotation-marks-around-path-names)
-   [<span data-ttu-id="71188-107">將已註冊的應用程式放在安全的位置</span><span class="sxs-lookup"><span data-stu-id="71188-107">Place registered applications in secure locations</span></span>](#place-registered-applications-in-secure-locations)
-   [<span data-ttu-id="71188-108">請勿使用基礎目錄或登錄機碼</span><span class="sxs-lookup"><span data-stu-id="71188-108">Do not use underlying directories or registry keys</span></span>](#do-not-use-underlying-directories-or-registry-keys)
-   [<span data-ttu-id="71188-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="71188-109">Related Topics</span></span>](#related-topics)

## <a name="use-quotation-marks-around-path-names"></a><span data-ttu-id="71188-110">使用引號括住路徑名稱</span><span class="sxs-lookup"><span data-stu-id="71188-110">Use quotation marks around path names</span></span>

<span data-ttu-id="71188-111">使用 [**IWiaDevMgr：： RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) 註冊應用程式以接收裝置事件時，請務必將應用程式的路徑和檔案名括在引號中。</span><span class="sxs-lookup"><span data-stu-id="71188-111">When using [**IWiaDevMgr::RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) to register an application to receive device events, be sure to surround the path and filename of the application with quotation marks.</span></span> <span data-ttu-id="71188-112">這可避免路徑被誤解的可能性，以及執行未授權的應用程式。</span><span class="sxs-lookup"><span data-stu-id="71188-112">This avoids the possibility that the path is misinterpreted and an unauthorized application is run.</span></span>

## <a name="place-registered-applications-in-secure-locations"></a><span data-ttu-id="71188-113">將已註冊的應用程式放在安全的位置</span><span class="sxs-lookup"><span data-stu-id="71188-113">Place registered applications in secure locations</span></span>

<span data-ttu-id="71188-114">註冊應用程式以接收裝置事件時，該應用程式可以由任何可存取該裝置的使用者執行。</span><span class="sxs-lookup"><span data-stu-id="71188-114">When an application is registered to receive a device event, that application can be run by any user that has access to that device.</span></span> <span data-ttu-id="71188-115">例如，如果應用程式是針對掃描事件註冊的，則按掃描器上的 [掃描] 按鈕將會導致該應用程式執行。</span><span class="sxs-lookup"><span data-stu-id="71188-115">For example, if an application is registered for a scan event, pressing the "scan" button on a scanner will cause that application to run.</span></span> <span data-ttu-id="71188-116">如果應用程式執行時的許可權高於使用者所擁有的許可權，這會造成潛在的安全性問題。</span><span class="sxs-lookup"><span data-stu-id="71188-116">If the application runs with a higher privilege than the user has, this causes a potential security issue.</span></span>

## <a name="do-not-use-underlying-directories-or-registry-keys"></a><span data-ttu-id="71188-117">請勿使用基礎目錄或登錄機碼</span><span class="sxs-lookup"><span data-stu-id="71188-117">Do not use underlying directories or registry keys</span></span>

<span data-ttu-id="71188-118">WIA 會在內部使用數個目錄和登錄機碼來儲存資料或資訊。</span><span class="sxs-lookup"><span data-stu-id="71188-118">WIA uses several directories and registry keys internally to store data or information.</span></span> <span data-ttu-id="71188-119">請勿直接存取這些目錄或登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="71188-119">Do not access these directories or registry keys directly.</span></span> <span data-ttu-id="71188-120">相反地，請使用公開的介面方法來指定所取得映射的目錄。</span><span class="sxs-lookup"><span data-stu-id="71188-120">Instead, use the exposed interface methods to specify directories for acquired images.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71188-121">[相關主題]</span><span class="sxs-lookup"><span data-stu-id="71188-121">Related Topics</span></span>

-   [<span data-ttu-id="71188-122">Microsoft 安全性</span><span class="sxs-lookup"><span data-stu-id="71188-122">Microsoft Security</span></span>](https://www.microsoft.com/security/)
-   [<span data-ttu-id="71188-123">MSDN Library 安全性首頁</span><span class="sxs-lookup"><span data-stu-id="71188-123">MSDN Library Security Home Page</span></span>](https://msdn.microsoft.com/security/default.aspx)
-   [<span data-ttu-id="71188-124">安全性的如何資源</span><span class="sxs-lookup"><span data-stu-id="71188-124">Security How-to Resources</span></span>](https://www.microsoft.com/technet/solutionaccelerators/howto/sechow.mspx)
-   [<span data-ttu-id="71188-125">TechNet 安全性資源</span><span class="sxs-lookup"><span data-stu-id="71188-125">TechNet Security Resources</span></span>](https://technet.microsoft.com/security/default.aspx)
-   <span data-ttu-id="71188-126">[Windows XP Embedded 開發人員的安全性考慮](/previous-versions/ms838345(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="71188-126">[Security Considerations for Windows XP Embedded Developers](/previous-versions/ms838345(v=msdn.10))</span></span>
-   [<span data-ttu-id="71188-127">安全性最佳作法</span><span class="sxs-lookup"><span data-stu-id="71188-127">Security Best Practices</span></span>](../secbp/best-practices-for-the-security-apis.md)

 

 
