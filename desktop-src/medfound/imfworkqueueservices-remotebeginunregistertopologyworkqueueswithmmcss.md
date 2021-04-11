---
description: IMFWorkQueueServices：： BeginUnregisterTopologyWorkQueuesWithMMCSS 方法的可遠端執行版本。
ms.assetid: 1a168462-400d-46c9-a489-7b861770469f
title: 'RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f52f82c55d692a2e1d9160c7a619338d82956ea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850075"
---
# <a name="remotebeginunregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="5f95b-103">RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="5f95b-103">RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="5f95b-104">[**IMFWorkQueueServices：： BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss)方法的可遠端執行版本。</span><span class="sxs-lookup"><span data-stu-id="5f95b-104">Remotable version of the [**IMFWorkQueueServices::BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(BeginUnregisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS(
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="5f95b-105">備註</span><span class="sxs-lookup"><span data-stu-id="5f95b-105">Remarks</span></span>

<span data-ttu-id="5f95b-106">應用程式無法直接呼叫這個方法，而物件也不會執行此方法。</span><span class="sxs-lookup"><span data-stu-id="5f95b-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="5f95b-107">方法不會出現在介面的 vtable 中。</span><span class="sxs-lookup"><span data-stu-id="5f95b-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="5f95b-108">如果跨進程界限呼叫 [**BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) ，媒體基礎 proxy/stub DLL 會將呼叫轉譯為遠端方法的呼叫，然後再將它轉譯回來。</span><span class="sxs-lookup"><span data-stu-id="5f95b-108">If [**BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f95b-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f95b-109">Requirements</span></span>



| <span data-ttu-id="5f95b-110">需求</span><span class="sxs-lookup"><span data-stu-id="5f95b-110">Requirement</span></span> | <span data-ttu-id="5f95b-111">值</span><span class="sxs-lookup"><span data-stu-id="5f95b-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f95b-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f95b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="5f95b-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f95b-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5f95b-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f95b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="5f95b-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f95b-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5f95b-116">標頭</span><span class="sxs-lookup"><span data-stu-id="5f95b-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f95b-117"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="5f95b-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="5f95b-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="5f95b-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="5f95b-119"><dt>Mfuuid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f95b-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="5f95b-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f95b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f95b-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="5f95b-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




