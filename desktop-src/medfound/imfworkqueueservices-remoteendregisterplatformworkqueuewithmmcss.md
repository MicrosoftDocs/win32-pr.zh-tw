---
description: IMFWorkQueueServices：： EndRegisterPlatformWorkQueueWithMMCSS 方法的可遠端執行版本。
ms.assetid: cb15129e-a3ad-4351-a7d6-dd4b883437bd
title: 'RemoteEndRegisterPlatformWorkQueueWithMMCSS (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 673281a8ed4e4c4174ecd2d874e7032776ea44c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689276"
---
# <a name="remoteendregisterplatformworkqueuewithmmcss"></a><span data-ttu-id="8d8df-103">RemoteEndRegisterPlatformWorkQueueWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="8d8df-103">RemoteEndRegisterPlatformWorkQueueWithMMCSS</span></span>

<span data-ttu-id="8d8df-104">[**IMFWorkQueueServices：： EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss)方法的可遠端執行版本。</span><span class="sxs-lookup"><span data-stu-id="8d8df-104">Remotable version of the [**IMFWorkQueueServices::EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) method.</span></span>

``` syntax
[call_as(EndRegisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteEndRegisterPlatformWorkQueueWithMMCSS(
    IUnknown *pResult,
    DWORD *pdwTaskId
);
```

## <a name="remarks"></a><span data-ttu-id="8d8df-105">備註</span><span class="sxs-lookup"><span data-stu-id="8d8df-105">Remarks</span></span>

<span data-ttu-id="8d8df-106">應用程式無法直接呼叫這個方法，而物件也不會執行此方法。</span><span class="sxs-lookup"><span data-stu-id="8d8df-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="8d8df-107">方法不會出現在介面的 vtable 中。</span><span class="sxs-lookup"><span data-stu-id="8d8df-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="8d8df-108">如果跨進程界限呼叫 [**EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) ，媒體基礎 proxy/stub DLL 會將呼叫轉譯為遠端方法的呼叫，然後再將它轉譯回來。</span><span class="sxs-lookup"><span data-stu-id="8d8df-108">If [**EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d8df-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d8df-109">Requirements</span></span>



| <span data-ttu-id="8d8df-110">需求</span><span class="sxs-lookup"><span data-stu-id="8d8df-110">Requirement</span></span> | <span data-ttu-id="8d8df-111">值</span><span class="sxs-lookup"><span data-stu-id="8d8df-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d8df-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8d8df-112">Minimum supported client</span></span><br/> | <span data-ttu-id="8d8df-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d8df-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8d8df-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8d8df-114">Minimum supported server</span></span><br/> | <span data-ttu-id="8d8df-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d8df-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8d8df-116">標頭</span><span class="sxs-lookup"><span data-stu-id="8d8df-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d8df-117"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="8d8df-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="8d8df-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="8d8df-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="8d8df-119"><dt>Mfuuid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d8df-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="8d8df-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d8df-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d8df-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="8d8df-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




