---
description: IMFWorkQueueServices：： EndUnregisterPlatformWorkQueueWithMMCSS 方法的可遠端執行版本。
ms.assetid: 92eef511-0af0-4146-ac81-7dfa4a649016
title: 'RemoteEndUnregisterPlatformWorkQueueWithMMCSS (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a03f8cdc1bfdded539c8143c3fa50c6bafb54de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851915"
---
# <a name="remoteendunregisterplatformworkqueuewithmmcss"></a><span data-ttu-id="e302b-103">RemoteEndUnregisterPlatformWorkQueueWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="e302b-103">RemoteEndUnregisterPlatformWorkQueueWithMMCSS</span></span>

<span data-ttu-id="e302b-104">[**IMFWorkQueueServices：： EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss)方法的可遠端執行版本。</span><span class="sxs-lookup"><span data-stu-id="e302b-104">Remotable version of the [**IMFWorkQueueServices::EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) method.</span></span>

``` syntax
[call_as(EndUnregisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteEndUnregisterPlatformWorkQueueWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="e302b-105">備註</span><span class="sxs-lookup"><span data-stu-id="e302b-105">Remarks</span></span>

<span data-ttu-id="e302b-106">應用程式無法直接呼叫這個方法，而物件也不會執行此方法。</span><span class="sxs-lookup"><span data-stu-id="e302b-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="e302b-107">方法不會出現在介面的 vtable 中。</span><span class="sxs-lookup"><span data-stu-id="e302b-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="e302b-108">如果跨進程界限呼叫 [**EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) ，媒體基礎 proxy/stub DLL 會將呼叫轉譯為遠端方法的呼叫，然後再將它轉譯回來。</span><span class="sxs-lookup"><span data-stu-id="e302b-108">If [**EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="e302b-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="e302b-109">Requirements</span></span>



| <span data-ttu-id="e302b-110">需求</span><span class="sxs-lookup"><span data-stu-id="e302b-110">Requirement</span></span> | <span data-ttu-id="e302b-111">值</span><span class="sxs-lookup"><span data-stu-id="e302b-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e302b-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e302b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e302b-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e302b-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e302b-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e302b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e302b-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e302b-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e302b-116">標頭</span><span class="sxs-lookup"><span data-stu-id="e302b-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="e302b-117"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="e302b-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="e302b-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="e302b-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="e302b-119"><dt>Mfuuid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e302b-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="e302b-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e302b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e302b-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="e302b-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




