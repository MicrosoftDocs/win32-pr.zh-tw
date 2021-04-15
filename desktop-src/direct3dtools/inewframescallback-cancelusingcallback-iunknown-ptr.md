---
description: 通知主機已取消要求的回呼。
MS-HAID: vspixengine.INewFramesCallback\_CancelUsingCallback\_IUnknown\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: INewFramesCallback：： CancelUsingCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 291B2F85-1437-4704-8971-4B7C25B693F8
api_name:
- INewFramesCallback.CancelUsingCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 863219cd37078fbde1e7ef8b2da7677a31e12872
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467925"
---
# <a name="span-idvspixengineinewframescallback_cancelusingcallback_iunknown_ptrspaninewframescallbackcancelusingcallback-method"></a><span data-ttu-id="b15c5-103"><span id="vspixengine.inewframescallback_cancelusingcallback_iunknown_ptr"></span>INewFramesCallback：： CancelUsingCallback 方法</span><span class="sxs-lookup"><span data-stu-id="b15c5-103"><span id="vspixengine.inewframescallback_cancelusingcallback_iunknown_ptr"></span>INewFramesCallback::CancelUsingCallback method</span></span>

<span data-ttu-id="b15c5-104">通知主機已取消要求的回呼。</span><span class="sxs-lookup"><span data-stu-id="b15c5-104">A callback that notifies the host of a canceled request.</span></span>

## <a name="syntax"></a><span data-ttu-id="b15c5-105">語法</span><span class="sxs-lookup"><span data-stu-id="b15c5-105">Syntax</span></span>


```C++
HRESULT CancelUsingCallback(
   IUnknown * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="b15c5-106">參數</span><span class="sxs-lookup"><span data-stu-id="b15c5-106">Parameters</span></span>

<span data-ttu-id="b15c5-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="b15c5-107">*requestCallback* </span></span>  
<span data-ttu-id="b15c5-108">取消之要求的位址。</span><span class="sxs-lookup"><span data-stu-id="b15c5-108">The address of the cancelled request.</span></span>

## <a name="return-value"></a><span data-ttu-id="b15c5-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="b15c5-109">Return value</span></span>

<span data-ttu-id="b15c5-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b15c5-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b15c5-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b15c5-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b15c5-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="b15c5-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b15c5-113">標頭</span><span class="sxs-lookup"><span data-stu-id="b15c5-113">Header</span></span></p></td><td><span data-ttu-id="b15c5-114">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="b15c5-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b15c5-115"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="b15c5-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b15c5-116">**INewFramesCallback**</span><span class="sxs-lookup"><span data-stu-id="b15c5-116">**INewFramesCallback**</span></span>](/windows/desktop/direct3dtools/inewframescallback)

 

 
