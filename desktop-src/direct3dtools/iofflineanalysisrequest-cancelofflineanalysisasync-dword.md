---
description: 在離線分析要求中取消離線分析的要求。
MS-HAID: vspixengine.IOfflineAnalysisRequest\_CancelOfflineAnalysisAsync\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IOfflineAnalysisRequest：： CancelOfflineAnalysisAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 20107890-DF7B-4483-9D2C-1D9164366504
api_name:
- IOfflineAnalysisRequest.CancelOfflineAnalysisAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 79329d27aff74efb7d08c7cc182ddb6e21f96cba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467636"
---
# <a name="span-idvspixengineiofflineanalysisrequest_cancelofflineanalysisasync_dwordspaniofflineanalysisrequestcancelofflineanalysisasync-method"></a><span data-ttu-id="5b0f2-103"><span id="vspixengine.iofflineanalysisrequest_cancelofflineanalysisasync_dword"></span>IOfflineAnalysisRequest：： CancelOfflineAnalysisAsync 方法</span><span class="sxs-lookup"><span data-stu-id="5b0f2-103"><span id="vspixengine.iofflineanalysisrequest_cancelofflineanalysisasync_dword"></span>IOfflineAnalysisRequest::CancelOfflineAnalysisAsync method</span></span>

<span data-ttu-id="5b0f2-104">在離線分析要求中取消離線分析的要求。</span><span class="sxs-lookup"><span data-stu-id="5b0f2-104">Requests to cancel offline analysis in an offline analysis request.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b0f2-105">語法</span><span class="sxs-lookup"><span data-stu-id="5b0f2-105">Syntax</span></span>


```C++
HRESULT CancelOfflineAnalysisAsync(
   DWORD cookie
);
```

## <a name="parameters"></a><span data-ttu-id="5b0f2-106">參數</span><span class="sxs-lookup"><span data-stu-id="5b0f2-106">Parameters</span></span>

<span data-ttu-id="5b0f2-107">*餅乾* </span><span class="sxs-lookup"><span data-stu-id="5b0f2-107">*cookie* </span></span>  
<span data-ttu-id="5b0f2-108">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="5b0f2-108">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

## <a name="return-value"></a><span data-ttu-id="5b0f2-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b0f2-109">Return value</span></span>

<span data-ttu-id="5b0f2-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5b0f2-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5b0f2-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5b0f2-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b0f2-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b0f2-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5b0f2-113">標頭</span><span class="sxs-lookup"><span data-stu-id="5b0f2-113">Header</span></span></p></td><td><span data-ttu-id="5b0f2-114">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="5b0f2-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5b0f2-115"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b0f2-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5b0f2-116">**IOfflineAnalysisRequest**</span><span class="sxs-lookup"><span data-stu-id="5b0f2-116">**IOfflineAnalysisRequest**</span></span>](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
