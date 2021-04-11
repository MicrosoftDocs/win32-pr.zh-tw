---
description: 回呼，會通知主機圖元歷程記錄要求的結果。
MS-HAID: vspixengine.IPixelHistoryCallback\_ResultCallback\_DWORD\_PixelHistoryOperation\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixelHistoryCallback：： ResultCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1F7D0EA5-402A-49C4-A83E-91596AE9536B
api_name:
- IPixelHistoryCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c43947148e2eb8139f3ad46157f19b1621a6c91e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317767"
---
# <a name="span-idvspixengineipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arrspanipixelhistorycallbackresultcallback-method"></a><span data-ttu-id="ec547-103"><span id="vspixengine.ipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arr"></span>IPixelHistoryCallback：： ResultCallback 方法</span><span class="sxs-lookup"><span data-stu-id="ec547-103"><span id="vspixengine.ipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arr"></span>IPixelHistoryCallback::ResultCallback method</span></span>

<span data-ttu-id="ec547-104">回呼，會通知主機圖元歷程記錄要求的結果。</span><span class="sxs-lookup"><span data-stu-id="ec547-104">A callback that notifies the host of pixel history request results.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec547-105">語法</span><span class="sxs-lookup"><span data-stu-id="ec547-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD                    count,
   PixelHistoryOperation [] count0_pixelHistoryOperation
);
```

## <a name="parameters"></a><span data-ttu-id="ec547-106">參數</span><span class="sxs-lookup"><span data-stu-id="ec547-106">Parameters</span></span>

<span data-ttu-id="ec547-107">*計數* </span><span class="sxs-lookup"><span data-stu-id="ec547-107">*count* </span></span>  
<span data-ttu-id="ec547-108">結果數目。</span><span class="sxs-lookup"><span data-stu-id="ec547-108">The number of results.</span></span>

<span data-ttu-id="ec547-109">*count0 \_ pixelHistoryOperation* </span><span class="sxs-lookup"><span data-stu-id="ec547-109">*count0\_pixelHistoryOperation* </span></span>  
<span data-ttu-id="ec547-110">結果。</span><span class="sxs-lookup"><span data-stu-id="ec547-110">The results.</span></span>

## <a name="return-value"></a><span data-ttu-id="ec547-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec547-111">Return value</span></span>

<span data-ttu-id="ec547-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ec547-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ec547-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ec547-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec547-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec547-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ec547-115">標頭</span><span class="sxs-lookup"><span data-stu-id="ec547-115">Header</span></span></p></td><td><span data-ttu-id="ec547-116">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="ec547-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="ec547-117"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec547-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="ec547-118">**IPixelHistoryCallback**</span><span class="sxs-lookup"><span data-stu-id="ec547-118">**IPixelHistoryCallback**</span></span>](/windows/desktop/direct3dtools/ipixelhistorycallback)

 

 
