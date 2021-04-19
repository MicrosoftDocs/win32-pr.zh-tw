---
description: 回呼函式，用來通知主機有哪些框架有離線分析報表可用。
MS-HAID: vspixengine.IOfflineAnalysisCacheCallback\_OfflineAnalaysisReportAvailabilityCallback\_DWORD\_DWORD\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IOfflineAnalysisCacheCallback：： OfflineAnalaysisReportAvailabilityCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2061EB62-4CBD-4668-BFCD-6E43014BB406
api_name:
- IOfflineAnalysisCacheCallback.OfflineAnalaysisReportAvailabilityCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: adbffbeb79aaf648c3319cf572dcbc905e9fd307
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106999826"
---
# <a name="span-idvspixengineiofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arrspaniofflineanalysiscachecallbackofflineanalaysisreportavailabilitycallback-method"></a><span data-ttu-id="5da60-103"><span id="vspixengine.iofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arr"></span>IOfflineAnalysisCacheCallback：： OfflineAnalaysisReportAvailabilityCallback 方法</span><span class="sxs-lookup"><span data-stu-id="5da60-103"><span id="vspixengine.iofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arr"></span>IOfflineAnalysisCacheCallback::OfflineAnalaysisReportAvailabilityCallback method</span></span>

<span data-ttu-id="5da60-104">回呼函式，用來通知主機有哪些框架有離線分析報表可用。</span><span class="sxs-lookup"><span data-stu-id="5da60-104">A callback function used to notify the host about which frames have offline analysis reports available.</span></span>

## <a name="syntax"></a><span data-ttu-id="5da60-105">語法</span><span class="sxs-lookup"><span data-stu-id="5da60-105">Syntax</span></span>


```C++
HRESULT OfflineAnalaysisReportAvailabilityCallback(
   DWORD    numFramesWithReports,
   DWORD [] count0_framesWithReports
);
```

## <a name="parameters"></a><span data-ttu-id="5da60-106">參數</span><span class="sxs-lookup"><span data-stu-id="5da60-106">Parameters</span></span>

<span data-ttu-id="5da60-107">*numFramesWithReports* </span><span class="sxs-lookup"><span data-stu-id="5da60-107">*numFramesWithReports* </span></span>  
<span data-ttu-id="5da60-108">Count0 framesWithReports 中的框架數目 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5da60-108">The number of frames in count0\_framesWithReports.</span></span>

<span data-ttu-id="5da60-109">*count0 \_ framesWithReports* </span><span class="sxs-lookup"><span data-stu-id="5da60-109">*count0\_framesWithReports* </span></span>  
<span data-ttu-id="5da60-110">陣列，其中包含具有可用離線分析報表之框架的框架編號。</span><span class="sxs-lookup"><span data-stu-id="5da60-110">An array containing the frame numbers of the frames that have offline analysis reports available.</span></span>

## <a name="return-value"></a><span data-ttu-id="5da60-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5da60-111">Return value</span></span>

<span data-ttu-id="5da60-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5da60-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5da60-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5da60-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5da60-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="5da60-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5da60-115">標頭</span><span class="sxs-lookup"><span data-stu-id="5da60-115">Header</span></span></p></td><td><span data-ttu-id="5da60-116">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="5da60-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5da60-117"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="5da60-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5da60-118">**IOfflineAnalysisCacheCallback**</span><span class="sxs-lookup"><span data-stu-id="5da60-118">**IOfflineAnalysisCacheCallback**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscachecallback)

 

 
