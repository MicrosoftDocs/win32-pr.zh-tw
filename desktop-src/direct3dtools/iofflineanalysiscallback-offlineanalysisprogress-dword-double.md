---
description: 用來通知主機離線分析進度的回呼函數。
MS-HAID: vspixengine.IOfflineAnalysisCallback\_OfflineAnalysisProgress\_DWORD\_DOUBLE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IOfflineAnalysisCallback：： OfflineAnalysisProgress 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 17847FD7-A10A-4E52-90AD-ADE446D87E73
api_name:
- IOfflineAnalysisCallback.OfflineAnalysisProgress
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4184be5d8d40b0ef46fe5e0029e9e4b1f38cf120
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385825"
---
# <a name="span-idvspixengineiofflineanalysiscallback_offlineanalysisprogress_dword_doublespaniofflineanalysiscallbackofflineanalysisprogress-method"></a><span data-ttu-id="11ee2-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysisprogress_dword_double"></span>IOfflineAnalysisCallback：： OfflineAnalysisProgress 方法</span><span class="sxs-lookup"><span data-stu-id="11ee2-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysisprogress_dword_double"></span>IOfflineAnalysisCallback::OfflineAnalysisProgress method</span></span>

<span data-ttu-id="11ee2-104">用來通知主機離線分析進度的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="11ee2-104">A callback function used to notify the host of offline analysis progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="11ee2-105">語法</span><span class="sxs-lookup"><span data-stu-id="11ee2-105">Syntax</span></span>


```C++
HRESULT OfflineAnalysisComplete(
   DWORD   cookie,
   HRESULT result,
   BSTR    outputFullFileName
);
```

## <a name="parameters"></a><span data-ttu-id="11ee2-106">參數</span><span class="sxs-lookup"><span data-stu-id="11ee2-106">Parameters</span></span>

<span data-ttu-id="11ee2-107">*餅乾* </span><span class="sxs-lookup"><span data-stu-id="11ee2-107">*cookie* </span></span>  
<span data-ttu-id="11ee2-108">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="11ee2-108">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="11ee2-109">*進展* </span><span class="sxs-lookup"><span data-stu-id="11ee2-109">*progress* </span></span>  
<span data-ttu-id="11ee2-110">進度百分比。</span><span class="sxs-lookup"><span data-stu-id="11ee2-110">The progress percentage.</span></span>

## <a name="return-value"></a><span data-ttu-id="11ee2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="11ee2-111">Return value</span></span>

<span data-ttu-id="11ee2-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="11ee2-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="11ee2-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="11ee2-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="11ee2-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="11ee2-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="11ee2-115">標頭</span><span class="sxs-lookup"><span data-stu-id="11ee2-115">Header</span></span></p></td><td><span data-ttu-id="11ee2-116">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="11ee2-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="11ee2-117"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="11ee2-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="11ee2-118">**IOfflineAnalysisCallback**</span><span class="sxs-lookup"><span data-stu-id="11ee2-118">**IOfflineAnalysisCallback**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscallback)

 

 
