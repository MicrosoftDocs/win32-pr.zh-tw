---
description: IMFMediaEventGenerator：： BeginGetEvent 方法的可遠端執行版本。
ms.assetid: 96a16fd3-10bc-4cd9-967a-ceb92e26ccc8
title: 'RemoteBeginGetEvent (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d728653df99baf0e816c53d8d22d7720c9aefac9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848440"
---
# <a name="remotebegingetevent"></a><span data-ttu-id="3a2b7-103">RemoteBeginGetEvent</span><span class="sxs-lookup"><span data-stu-id="3a2b7-103">RemoteBeginGetEvent</span></span>

<span data-ttu-id="3a2b7-104">[**IMFMediaEventGenerator：： BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)方法的可遠端執行版本。</span><span class="sxs-lookup"><span data-stu-id="3a2b7-104">Remotable version of the [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method.</span></span>

``` syntax
[call_as(BeginGetEvent)]
HRESULT RemoteBeginGetEvent(
    IMFRemoteAsyncCallback* pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="3a2b7-105">備註</span><span class="sxs-lookup"><span data-stu-id="3a2b7-105">Remarks</span></span>

<span data-ttu-id="3a2b7-106">應用程式無法直接呼叫這個方法，而物件也不會執行此方法。</span><span class="sxs-lookup"><span data-stu-id="3a2b7-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="3a2b7-107">方法不會出現在介面的 vtable 中。</span><span class="sxs-lookup"><span data-stu-id="3a2b7-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="3a2b7-108">如果跨進程界限呼叫 [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) ，媒體基礎 proxy/stub DLL 會將呼叫轉譯為遠端方法的呼叫，然後再將它轉譯回來。</span><span class="sxs-lookup"><span data-stu-id="3a2b7-108">If [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a2b7-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a2b7-109">Requirements</span></span>



| <span data-ttu-id="3a2b7-110">需求</span><span class="sxs-lookup"><span data-stu-id="3a2b7-110">Requirement</span></span> | <span data-ttu-id="3a2b7-111">值</span><span class="sxs-lookup"><span data-stu-id="3a2b7-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a2b7-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a2b7-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3a2b7-113">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a2b7-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="3a2b7-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a2b7-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3a2b7-115">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a2b7-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="3a2b7-116">標頭</span><span class="sxs-lookup"><span data-stu-id="3a2b7-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a2b7-117"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="3a2b7-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="3a2b7-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="3a2b7-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="3a2b7-119"><dt>Mfuuid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a2b7-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="3a2b7-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a2b7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a2b7-121">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="3a2b7-121">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 




