---
description: 回呼，會通知主機相關聯的要求所傳回的圖元歷程記錄基本作業資訊。
MS-HAID: vspixengine.IPixelHistoryCallback2\_PrimitivesCallback\_DWORD\_PixelHistoryOperation\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixelHistoryCallback2：:P rimitivesCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2A67EC3B-72F2-4347-AD23-961CDE0D456F
api_name:
- IPixelHistoryCallback2.PrimitivesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8512bde1acd96ebbe132eeb91872d04ce043b44f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510251"
---
# <a name="span-idvspixengineipixelhistorycallback2_primitivescallback_dword_pixelhistoryoperation_arrspanipixelhistorycallback2primitivescallback-method"></a><span data-ttu-id="b270c-103"><span id="vspixengine.ipixelhistorycallback2_primitivescallback_dword_pixelhistoryoperation_arr"></span>IPixelHistoryCallback2：:P rimitivesCallback 方法</span><span class="sxs-lookup"><span data-stu-id="b270c-103"><span id="vspixengine.ipixelhistorycallback2_primitivescallback_dword_pixelhistoryoperation_arr"></span>IPixelHistoryCallback2::PrimitivesCallback method</span></span>

<span data-ttu-id="b270c-104">回呼，會通知主機相關聯的要求所傳回的圖元歷程記錄基本作業資訊。</span><span class="sxs-lookup"><span data-stu-id="b270c-104">A callback that notifies the host of pixel history primitive operation information returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="b270c-105">語法</span><span class="sxs-lookup"><span data-stu-id="b270c-105">Syntax</span></span>


```C++
HRESULT PrimitivesCallback(
   DWORD                    count,
   PixelHistoryOperation [] count0_primitives
);
```

## <a name="parameters"></a><span data-ttu-id="b270c-106">參數</span><span class="sxs-lookup"><span data-stu-id="b270c-106">Parameters</span></span>

<span data-ttu-id="b270c-107">*計數* </span><span class="sxs-lookup"><span data-stu-id="b270c-107">*count* </span></span>  
<span data-ttu-id="b270c-108">基本類型的數目。</span><span class="sxs-lookup"><span data-stu-id="b270c-108">The number of primitives.</span></span>

<span data-ttu-id="b270c-109">*count0 \_ 基本專案* </span><span class="sxs-lookup"><span data-stu-id="b270c-109">*count0\_primitives* </span></span>  
<span data-ttu-id="b270c-110">基本類型。</span><span class="sxs-lookup"><span data-stu-id="b270c-110">The primitives.</span></span>

## <a name="return-value"></a><span data-ttu-id="b270c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b270c-111">Return value</span></span>

<span data-ttu-id="b270c-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b270c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b270c-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b270c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b270c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b270c-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b270c-115">標頭</span><span class="sxs-lookup"><span data-stu-id="b270c-115">Header</span></span></p></td><td><span data-ttu-id="b270c-116">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="b270c-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b270c-117"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="b270c-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b270c-118">**IPixelHistoryCallback2**</span><span class="sxs-lookup"><span data-stu-id="b270c-118">**IPixelHistoryCallback2**</span></span>](/windows/desktop/direct3dtools/ipixelhistorycallback2)

 

 
