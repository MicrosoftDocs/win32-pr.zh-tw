---
description: IMFMediaEventGenerator：： EndGetEvent 方法的可遠端執行版本。
ms.assetid: 5b793760-546c-43d4-8251-d89d8d7152ad
title: 'RemoteEndGetEvent (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f3c4a5fe87dddf5fc1d256d61d8c863c2f1d9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691619"
---
# <a name="remoteendgetevent"></a><span data-ttu-id="74bcf-103">RemoteEndGetEvent</span><span class="sxs-lookup"><span data-stu-id="74bcf-103">RemoteEndGetEvent</span></span>

<span data-ttu-id="74bcf-104">[**IMFMediaEventGenerator：： EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent)方法的可遠端執行版本。</span><span class="sxs-lookup"><span data-stu-id="74bcf-104">Remotable version of the [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) method.</span></span>

``` syntax
[call_as(EndGetEvent)]
HRESULT RemoteEndGetEvent(
    IUnknown *pResult,
    DWORD *pcbEvent,
    BYTE **ppbEvent
);
```

## <a name="remarks"></a><span data-ttu-id="74bcf-105">備註</span><span class="sxs-lookup"><span data-stu-id="74bcf-105">Remarks</span></span>

<span data-ttu-id="74bcf-106">應用程式無法直接呼叫這個方法，而物件也不會執行此方法。</span><span class="sxs-lookup"><span data-stu-id="74bcf-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="74bcf-107">方法不會出現在介面的 vtable 中。</span><span class="sxs-lookup"><span data-stu-id="74bcf-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="74bcf-108">如果跨進程界限呼叫 [**EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) ，媒體基礎 proxy/stub DLL 會將呼叫轉譯為遠端方法的呼叫，然後再將它轉譯回來。</span><span class="sxs-lookup"><span data-stu-id="74bcf-108">If [**EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="74bcf-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="74bcf-109">Requirements</span></span>



| <span data-ttu-id="74bcf-110">需求</span><span class="sxs-lookup"><span data-stu-id="74bcf-110">Requirement</span></span> | <span data-ttu-id="74bcf-111">值</span><span class="sxs-lookup"><span data-stu-id="74bcf-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74bcf-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74bcf-112">Minimum supported client</span></span><br/> | <span data-ttu-id="74bcf-113">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74bcf-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="74bcf-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74bcf-114">Minimum supported server</span></span><br/> | <span data-ttu-id="74bcf-115">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74bcf-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="74bcf-116">標頭</span><span class="sxs-lookup"><span data-stu-id="74bcf-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="74bcf-117"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="74bcf-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="74bcf-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="74bcf-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="74bcf-119"><dt>Mfuuid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="74bcf-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="74bcf-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74bcf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74bcf-121">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="74bcf-121">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 




