---
description: 回呼函數，用來通知主機事件清單中事件的相關資訊。
MS-HAID: vspixengine.IFrameEventsCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_VARIANT\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFrameEventsCallback：： ResultCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5AB67A11-00C1-47AF-8C8C-8B2FDD095BCF
api_name:
- IFrameEventsCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e746c54f2a82adb5042cd479e4ca04299c1b7402
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187488"
---
# <a name="span-idvspixengineiframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arrspaniframeeventscallbackresultcallback-method"></a><span data-ttu-id="368c8-103"><span id="vspixengine.iframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arr"></span>IFrameEventsCallback：： ResultCallback 方法</span><span class="sxs-lookup"><span data-stu-id="368c8-103"><span id="vspixengine.iframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arr"></span>IFrameEventsCallback::ResultCallback method</span></span>

<span data-ttu-id="368c8-104">回呼函數，用來通知主機事件清單中事件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="368c8-104">A callback function used to notify the host of information about events in the event list.</span></span>

## <a name="syntax"></a><span data-ttu-id="368c8-105">語法</span><span class="sxs-lookup"><span data-stu-id="368c8-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD      frameNumber,
   DWORD      numElements,
   DWORD      numRows,
   DWORD      numColumns,
   VARIANT [] count1_pRowData
);
```

## <a name="parameters"></a><span data-ttu-id="368c8-106">參數</span><span class="sxs-lookup"><span data-stu-id="368c8-106">Parameters</span></span>

<span data-ttu-id="368c8-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="368c8-107">*frameNumber* </span></span>  
<span data-ttu-id="368c8-108">與事件相關聯的框架編號。</span><span class="sxs-lookup"><span data-stu-id="368c8-108">The frame number associated with the events.</span></span>

<span data-ttu-id="368c8-109">*numElements* </span><span class="sxs-lookup"><span data-stu-id="368c8-109">*numElements* </span></span>  
<span data-ttu-id="368c8-110">所有事件的所有資料行中的總欄位數。</span><span class="sxs-lookup"><span data-stu-id="368c8-110">The total number of fields in all columns of all events.</span></span>

<span data-ttu-id="368c8-111">*numRows* </span><span class="sxs-lookup"><span data-stu-id="368c8-111">*numRows* </span></span>  
<span data-ttu-id="368c8-112">結果中的事件數目。</span><span class="sxs-lookup"><span data-stu-id="368c8-112">The number of events in the result.</span></span>

<span data-ttu-id="368c8-113">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="368c8-113">*numColumns* </span></span>  
<span data-ttu-id="368c8-114">每個資料列中 (欄位) 的資料行數目。</span><span class="sxs-lookup"><span data-stu-id="368c8-114">The number of columns (fields) in each row.</span></span>

<span data-ttu-id="368c8-115">*count1 \_ pRowData* </span><span class="sxs-lookup"><span data-stu-id="368c8-115">*count1\_pRowData* </span></span>  
<span data-ttu-id="368c8-116">事件的相關資訊;每個事件的每個欄位都有一個專案。</span><span class="sxs-lookup"><span data-stu-id="368c8-116">Information about the events; one item for each field of each event.</span></span>

## <a name="return-value"></a><span data-ttu-id="368c8-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="368c8-117">Return value</span></span>

<span data-ttu-id="368c8-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="368c8-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="368c8-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="368c8-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="368c8-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="368c8-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="368c8-121">標頭</span><span class="sxs-lookup"><span data-stu-id="368c8-121">Header</span></span></p></td><td><span data-ttu-id="368c8-122">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="368c8-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="368c8-123"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="368c8-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="368c8-124">**IFrameEventsCallback**</span><span class="sxs-lookup"><span data-stu-id="368c8-124">**IFrameEventsCallback**</span></span>](/windows/desktop/direct3dtools/iframeeventscallback)

 

 
