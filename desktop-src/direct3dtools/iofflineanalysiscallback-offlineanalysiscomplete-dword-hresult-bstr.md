---
description: 用來通知主機離線分析已完成的回呼函數。
MS-HAID: vspixengine.IOfflineAnalysisCallback\_OfflineAnalysisComplete\_DWORD\_HRESULT\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IOfflineAnalysisCallback：： OfflineAnalysisComplete 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36E10709-51DC-4657-B184-F1F807ABBBB4
api_name:
- IOfflineAnalysisCallback.OfflineAnalysisComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a1ece7106bee1c49f97238bf06348b049d3f7167
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510345"
---
# <a name="span-idvspixengineiofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstrspaniofflineanalysiscallbackofflineanalysiscomplete-method"></a><span data-ttu-id="982b5-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstr"></span>IOfflineAnalysisCallback：： OfflineAnalysisComplete 方法</span><span class="sxs-lookup"><span data-stu-id="982b5-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstr"></span>IOfflineAnalysisCallback::OfflineAnalysisComplete method</span></span>

<span data-ttu-id="982b5-104">用來通知主機離線分析已完成的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="982b5-104">A callback function used to notify the host that offline analysis has completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="982b5-105">語法</span><span class="sxs-lookup"><span data-stu-id="982b5-105">Syntax</span></span>


```C++
HRESULT OfflineAnalysisComplete(
   DWORD   cookie,
   HRESULT result,
   BSTR    outputFullFileName
);
```

## <a name="parameters"></a><span data-ttu-id="982b5-106">參數</span><span class="sxs-lookup"><span data-stu-id="982b5-106">Parameters</span></span>

<span data-ttu-id="982b5-107">*餅乾* </span><span class="sxs-lookup"><span data-stu-id="982b5-107">*cookie* </span></span>  
<span data-ttu-id="982b5-108">可唯一識別起始離線分析之要求的 cookie。</span><span class="sxs-lookup"><span data-stu-id="982b5-108">A cookie that uniquely identifies the request which initiated offline analysis.</span></span>

<span data-ttu-id="982b5-109">*結果* </span><span class="sxs-lookup"><span data-stu-id="982b5-109">*result* </span></span>  
<span data-ttu-id="982b5-110">指出離線分析是否成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="982b5-110">Indicates whether offline analysis succeeded or failed.</span></span> <span data-ttu-id="982b5-111">如果成功，則會將結果寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="982b5-111">If it succeeded, results were written to a file.</span></span>

<span data-ttu-id="982b5-112">*outputFullFileName* </span><span class="sxs-lookup"><span data-stu-id="982b5-112">*outputFullFileName* </span></span>  
<span data-ttu-id="982b5-113">COM 字串寫入寫入離線分析結果的檔案名。</span><span class="sxs-lookup"><span data-stu-id="982b5-113">A COM string contianing the name of the file where offline analysis results were written.</span></span>

## <a name="return-value"></a><span data-ttu-id="982b5-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="982b5-114">Return value</span></span>

<span data-ttu-id="982b5-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="982b5-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="982b5-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="982b5-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="982b5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="982b5-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="982b5-118">標頭</span><span class="sxs-lookup"><span data-stu-id="982b5-118">Header</span></span></p></td><td><span data-ttu-id="982b5-119">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="982b5-119">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="982b5-120"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="982b5-120"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="982b5-121">**IOfflineAnalysisCallback**</span><span class="sxs-lookup"><span data-stu-id="982b5-121">**IOfflineAnalysisCallback**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscallback)

 

 
