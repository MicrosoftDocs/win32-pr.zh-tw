---
description: 要求快取指定框架的離線分析報表。
MS-HAID: vspixengine.IOfflineAnalysisCacheRequest\_RequestOfflineAnalysisReportAvailabilityAsync\_DWORD\_DWORD\_arr\_IOfflineAnalysisCacheCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IOfflineAnalysisCacheRequest：： RequestOfflineAnalysisReportAvailabilityAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 10FA71F8-813D-4788-92C8-00B30A9AE5CC
api_name:
- IOfflineAnalysisCacheRequest.RequestOfflineAnalysisReportAvailabilityAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6e2dfdb1e2a2cc113f9585a818550dd60aa73ae2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510347"
---
# <a name="span-idvspixengineiofflineanalysiscacherequest_requestofflineanalysisreportavailabilityasync_dword_dword_arr_iofflineanalysiscachecallback_ptrspaniofflineanalysiscacherequestrequestofflineanalysisreportavailabilityasync-method"></a><span data-ttu-id="e6f04-103"><span id="vspixengine.iofflineanalysiscacherequest_requestofflineanalysisreportavailabilityasync_dword_dword_arr_iofflineanalysiscachecallback_ptr"></span>IOfflineAnalysisCacheRequest：： RequestOfflineAnalysisReportAvailabilityAsync 方法</span><span class="sxs-lookup"><span data-stu-id="e6f04-103"><span id="vspixengine.iofflineanalysiscacherequest_requestofflineanalysisreportavailabilityasync_dword_dword_arr_iofflineanalysiscachecallback_ptr"></span>IOfflineAnalysisCacheRequest::RequestOfflineAnalysisReportAvailabilityAsync method</span></span>

<span data-ttu-id="e6f04-104">要求快取指定框架的離線分析報表。</span><span class="sxs-lookup"><span data-stu-id="e6f04-104">Requests to cache offline analysis report of the specified frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6f04-105">語法</span><span class="sxs-lookup"><span data-stu-id="e6f04-105">Syntax</span></span>


```C++
HRESULT RequestOfflineAnalysisReportAvailabilityAsync(
   DWORD                           numFrames,
   DWORD []                        count0_frameNumbers,
   IOfflineAnalysisCacheCallback * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="e6f04-106">參數</span><span class="sxs-lookup"><span data-stu-id="e6f04-106">Parameters</span></span>

<span data-ttu-id="e6f04-107">*numFrames* </span><span class="sxs-lookup"><span data-stu-id="e6f04-107">*numFrames* </span></span>  
<span data-ttu-id="e6f04-108">要為其產生分析報表的框架數目。</span><span class="sxs-lookup"><span data-stu-id="e6f04-108">The number of frames to generate analysis reports for.</span></span>

<span data-ttu-id="e6f04-109">*count0 \_ frameNumbers* </span><span class="sxs-lookup"><span data-stu-id="e6f04-109">*count0\_frameNumbers* </span></span>  
<span data-ttu-id="e6f04-110">指定的框架。</span><span class="sxs-lookup"><span data-stu-id="e6f04-110">The specified frames.</span></span>

<span data-ttu-id="e6f04-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="e6f04-111">*requestCallback* </span></span>  
<span data-ttu-id="e6f04-112">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="e6f04-112">The address of a callback used to notify the host of results.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6f04-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e6f04-113">Return value</span></span>

<span data-ttu-id="e6f04-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e6f04-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e6f04-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e6f04-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6f04-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6f04-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e6f04-117">標頭</span><span class="sxs-lookup"><span data-stu-id="e6f04-117">Header</span></span></p></td><td><span data-ttu-id="e6f04-118">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="e6f04-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e6f04-119"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6f04-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e6f04-120">**IOfflineAnalysisCacheRequest**</span><span class="sxs-lookup"><span data-stu-id="e6f04-120">**IOfflineAnalysisCacheRequest**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscacherequest)

 

 
