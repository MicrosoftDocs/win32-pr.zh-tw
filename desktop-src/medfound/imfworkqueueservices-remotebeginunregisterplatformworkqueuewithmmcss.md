---
description: IMFWorkQueueServices：： BeginUnregisterPlatformWorkQueueWithMMCSS 方法的可遠端執行版本。
ms.assetid: c3117086-268e-4e52-acfb-2c8167adaa07
title: 'RemoteBeginUnregisterPlatformWorkQueueWithMMCSS (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab364f041d6bc8d0f6275879c82a937e98f463b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996989"
---
# <a name="remotebeginunregisterplatformworkqueuewithmmcss"></a><span data-ttu-id="77d3e-103">RemoteBeginUnregisterPlatformWorkQueueWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="77d3e-103">RemoteBeginUnregisterPlatformWorkQueueWithMMCSS</span></span>

<span data-ttu-id="77d3e-104">[**IMFWorkQueueServices：： BeginUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss)方法的可遠端執行版本。</span><span class="sxs-lookup"><span data-stu-id="77d3e-104">Remotable version of the [**IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) method.</span></span>

``` syntax
[call_as(BeginUnregisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteBeginUnregisterPlatformWorkQueueWithMMCSS(
    DWORD dwPlatformWorkQueue,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="77d3e-105">備註</span><span class="sxs-lookup"><span data-stu-id="77d3e-105">Remarks</span></span>

<span data-ttu-id="77d3e-106">應用程式無法直接呼叫這個方法，而物件也不會執行此方法。</span><span class="sxs-lookup"><span data-stu-id="77d3e-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="77d3e-107">方法不會出現在介面的 vtable 中。</span><span class="sxs-lookup"><span data-stu-id="77d3e-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="77d3e-108">如果跨進程界限呼叫 [**BeginUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) ，媒體基礎 proxy/stub DLL 會將呼叫轉譯為遠端方法的呼叫，然後再將它轉譯回來。</span><span class="sxs-lookup"><span data-stu-id="77d3e-108">If [**BeginUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="77d3e-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="77d3e-109">Requirements</span></span>



| <span data-ttu-id="77d3e-110">需求</span><span class="sxs-lookup"><span data-stu-id="77d3e-110">Requirement</span></span> | <span data-ttu-id="77d3e-111">值</span><span class="sxs-lookup"><span data-stu-id="77d3e-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77d3e-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="77d3e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="77d3e-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="77d3e-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="77d3e-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="77d3e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="77d3e-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="77d3e-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="77d3e-116">標頭</span><span class="sxs-lookup"><span data-stu-id="77d3e-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="77d3e-117"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="77d3e-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="77d3e-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="77d3e-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="77d3e-119"><dt>Mfuuid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="77d3e-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="77d3e-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77d3e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77d3e-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="77d3e-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




