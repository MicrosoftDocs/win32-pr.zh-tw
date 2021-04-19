---
description: IMFWorkQueueServices：： EndRegisterTopologyWorkQueuesWithMMCSS 方法的可遠端執行版本。
ms.assetid: 94dce412-6a72-4ddf-86a3-5176ee1eb6d2
title: 'RemoteEndRegisterTopologyWorkQueuesWithMMCSS (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3333becfcd7a3c5e2621b628b6435b96af017cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991928"
---
# <a name="remoteendregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="c2a1d-103">RemoteEndRegisterTopologyWorkQueuesWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="c2a1d-103">RemoteEndRegisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="c2a1d-104">[**IMFWorkQueueServices：： EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss)方法的可遠端執行版本。</span><span class="sxs-lookup"><span data-stu-id="c2a1d-104">Remotable version of the [**IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(EndRegisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteEndRegisterTopologyWorkQueuesWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="c2a1d-105">備註</span><span class="sxs-lookup"><span data-stu-id="c2a1d-105">Remarks</span></span>

<span data-ttu-id="c2a1d-106">應用程式無法直接呼叫這個方法，而物件也不會執行此方法。</span><span class="sxs-lookup"><span data-stu-id="c2a1d-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="c2a1d-107">方法不會出現在介面的 vtable 中。</span><span class="sxs-lookup"><span data-stu-id="c2a1d-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="c2a1d-108">如果跨進程界限呼叫 [**EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) ，媒體基礎 proxy/stub DLL 會將呼叫轉譯為遠端方法的呼叫，然後再將它轉譯回來。</span><span class="sxs-lookup"><span data-stu-id="c2a1d-108">If [**EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2a1d-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2a1d-109">Requirements</span></span>



| <span data-ttu-id="c2a1d-110">需求</span><span class="sxs-lookup"><span data-stu-id="c2a1d-110">Requirement</span></span> | <span data-ttu-id="c2a1d-111">值</span><span class="sxs-lookup"><span data-stu-id="c2a1d-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2a1d-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2a1d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c2a1d-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2a1d-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c2a1d-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2a1d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c2a1d-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2a1d-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c2a1d-116">標頭</span><span class="sxs-lookup"><span data-stu-id="c2a1d-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2a1d-117"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="c2a1d-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="c2a1d-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="c2a1d-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2a1d-119"><dt>Mfuuid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2a1d-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="c2a1d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2a1d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2a1d-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="c2a1d-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




