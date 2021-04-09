---
title: URL 標記函數
description: URL 標記函數
ms.assetid: 773743d3-9434-4ec9-b85c-9b971e37682f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2db726d8ce6a101b0b97fbe2128e074ee5e892e3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842784"
---
# <a name="url-moniker-functions"></a><span data-ttu-id="3cddc-103">URL 標記函數</span><span class="sxs-lookup"><span data-stu-id="3cddc-103">URL Moniker Functions</span></span>

<span data-ttu-id="3cddc-104">URL 標記函式會讓開發人員免于建立、管理及使用 URL 標記的複雜性。</span><span class="sxs-lookup"><span data-stu-id="3cddc-104">URL moniker functions insulate developers from the complexities of creating, managing, and using URL monikers.</span></span> <span data-ttu-id="3cddc-105">這些函數如下所示：</span><span class="sxs-lookup"><span data-stu-id="3cddc-105">These functions are as follows:</span></span>

-   <span data-ttu-id="3cddc-106">[**CreateURLMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775102(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3cddc-106">[**CreateURLMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775102(v=vs.85))</span></span>
-   <span data-ttu-id="3cddc-107">[**IsValidURL**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775112(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3cddc-107">[**IsValidURL**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775112(v=vs.85))</span></span>
-   <span data-ttu-id="3cddc-108">[**RegisterMediaTypes**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3cddc-108">[**RegisterMediaTypes**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85))</span></span>
-   [<span data-ttu-id="3cddc-109">**CreateFormatEnumerator**</span><span class="sxs-lookup"><span data-stu-id="3cddc-109">**CreateFormatEnumerator**</span></span>](/windows/desktop/api/Urlmon/nf-urlmon-createformatenumerator)
-   <span data-ttu-id="3cddc-110">[**RegisterFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3cddc-110">[**RegisterFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85))</span></span>
-   <span data-ttu-id="3cddc-111">[**RevokeFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775121(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3cddc-111">[**RevokeFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775121(v=vs.85))</span></span>
-   <span data-ttu-id="3cddc-112">[**RegisterMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775117(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3cddc-112">[**RegisterMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775117(v=vs.85))</span></span>
-   <span data-ttu-id="3cddc-113">[**FindMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775106(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3cddc-113">[**FindMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775106(v=vs.85))</span></span>
-   <span data-ttu-id="3cddc-114">[**GetClassFileOrMime**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775108(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3cddc-114">[**GetClassFileOrMime**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775108(v=vs.85))</span></span>
-   <span data-ttu-id="3cddc-115">[**UrlMkSetSessionOption**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775125(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3cddc-115">[**UrlMkSetSessionOption**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775125(v=vs.85))</span></span>

<span data-ttu-id="3cddc-116">您熟悉這些功能的方式如下：</span><span class="sxs-lookup"><span data-stu-id="3cddc-116">Your familiarity with these functions can be as follows:</span></span>

-   <span data-ttu-id="3cddc-117">如果您在獨立應用程式中使用 URL 的名字標記，請熟悉 [**CreateURLMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775102(v=vs.85)) 和 [**IsValidURL**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775112(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="3cddc-117">Be familiar with [**CreateURLMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775102(v=vs.85)) and [**IsValidURL**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775112(v=vs.85)) if you will be using URL monikers in stand-alone applications.</span></span> <span data-ttu-id="3cddc-118">如果您要撰寫 ActiveX 控制項，您應該使用 [**IBindHost：： CreateMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775075(v=vs.85)) 而不是 **CreateURLMoniker**。</span><span class="sxs-lookup"><span data-stu-id="3cddc-118">If you are authoring an ActiveX control, you should use [**IBindHost::CreateMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775075(v=vs.85)) instead of **CreateURLMoniker**.</span></span>
-   <span data-ttu-id="3cddc-119">如果您要使用 URL 標記來執行任何 MIME 協商，請熟悉 [**RegisterMediaTypes**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85))、 [**CreateFormatEnumerator**](/windows/desktop/api/Urlmon/nf-urlmon-createformatenumerator)、 [**RegisterFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85))和 [**RevokeFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775121(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="3cddc-119">Be familiar with [**RegisterMediaTypes**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85)), [**CreateFormatEnumerator**](/windows/desktop/api/Urlmon/nf-urlmon-createformatenumerator), [**RegisterFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85)), and [**RevokeFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775121(v=vs.85)) if you will be performing any MIME negotiation with URL monikers.</span></span>
-   <span data-ttu-id="3cddc-120">只有當您有大量的 URL 名字和 COM 的體驗時，才熟悉 [**RegisterMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775117(v=vs.85))、 [**FindMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775106(v=vs.85))、 [**GetClassFileOrMime**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775108(v=vs.85))和 [**UrlMkSetSessionOption**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775125(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="3cddc-120">Be familiar with [**RegisterMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775117(v=vs.85)), [**FindMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775106(v=vs.85)), [**GetClassFileOrMime**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775108(v=vs.85)), and [**UrlMkSetSessionOption**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775125(v=vs.85)) only if you have significant experience both with URL monikers and with COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3cddc-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="3cddc-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cddc-122">URL 的名字</span><span class="sxs-lookup"><span data-stu-id="3cddc-122">URL Monikers</span></span>](url-monikers.md)
</dt> </dl>

 

 