---
description: 用來通知主機圖形記錄摘要資訊的回呼函數。
MS-HAID: vspixengine.ISummaryCallback\_ResultCallback\_DWORD\_SummaryItem\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ISummaryCallback：： ResultCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 07569D26-45A6-41A5-868D-8038BAB9079B
api_name:
- ISummaryCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c4ea46550628ec9701ab6b0e6bb3af9ab71a2499
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972752"
---
# <a name="span-idvspixengineisummarycallback_resultcallback_dword_summaryitem_arrspanisummarycallbackresultcallback-method"></a><span data-ttu-id="8e628-103"><span id="vspixengine.isummarycallback_resultcallback_dword_summaryitem_arr"></span>ISummaryCallback：： ResultCallback 方法</span><span class="sxs-lookup"><span data-stu-id="8e628-103"><span id="vspixengine.isummarycallback_resultcallback_dword_summaryitem_arr"></span>ISummaryCallback::ResultCallback method</span></span>

<span data-ttu-id="8e628-104">用來通知主機圖形記錄摘要資訊的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="8e628-104">A callback function used to notify the host of graphics log summary information.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e628-105">語法</span><span class="sxs-lookup"><span data-stu-id="8e628-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD          count,
   SummaryItem [] count0_summaryItem
);
```

## <a name="parameters"></a><span data-ttu-id="8e628-106">參數</span><span class="sxs-lookup"><span data-stu-id="8e628-106">Parameters</span></span>

<span data-ttu-id="8e628-107">*計數* </span><span class="sxs-lookup"><span data-stu-id="8e628-107">*count* </span></span>  
<span data-ttu-id="8e628-108">傳回的摘要資訊專案數目。</span><span class="sxs-lookup"><span data-stu-id="8e628-108">The number of summary information items returned.</span></span>

<span data-ttu-id="8e628-109">*count0 \_ summaryItem* </span><span class="sxs-lookup"><span data-stu-id="8e628-109">*count0\_summaryItem* </span></span>  
<span data-ttu-id="8e628-110">摘要資訊專案 (的索引鍵/值組) 。</span><span class="sxs-lookup"><span data-stu-id="8e628-110">The summary information items (key-value pairs).</span></span>

## <a name="return-value"></a><span data-ttu-id="8e628-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="8e628-111">Return value</span></span>

<span data-ttu-id="8e628-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="8e628-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8e628-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8e628-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e628-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e628-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8e628-115">標頭</span><span class="sxs-lookup"><span data-stu-id="8e628-115">Header</span></span></p></td><td><span data-ttu-id="8e628-116">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="8e628-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="8e628-117"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e628-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="8e628-118">**ISummaryCallback**</span><span class="sxs-lookup"><span data-stu-id="8e628-118">**ISummaryCallback**</span></span>](/windows/desktop/direct3dtools/isummarycallback)

 

 
