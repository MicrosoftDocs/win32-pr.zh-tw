---
description: 取得圖形記錄相關摘要資訊的非同步要求。
MS-HAID: vspixengine.ISummaryRequest\_RequestAsync\_iSummaryCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ISummaryRequest：： RequestAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A33798E3-7332-4582-A7B1-B0F9FB694872
api_name:
- ISummaryRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c716545de275250efcae56a6be39c8b620ed014a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972945"
---
# <a name="span-idvspixengineisummaryrequest_requestasync_isummarycallback_ptr_dword_dwordspanisummaryrequestrequestasync-method"></a><span data-ttu-id="a1b72-103"><span id="vspixengine.isummaryrequest_requestasync_isummarycallback_ptr_dword_dword"></span>ISummaryRequest：： RequestAsync 方法</span><span class="sxs-lookup"><span data-stu-id="a1b72-103"><span id="vspixengine.isummaryrequest_requestasync_isummarycallback_ptr_dword_dword"></span>ISummaryRequest::RequestAsync method</span></span>

<span data-ttu-id="a1b72-104">取得圖形記錄相關摘要資訊的非同步要求。</span><span class="sxs-lookup"><span data-stu-id="a1b72-104">An asynchronous request to get summary information about a graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1b72-105">語法</span><span class="sxs-lookup"><span data-stu-id="a1b72-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   iSummaryCallback * requestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="a1b72-106">參數</span><span class="sxs-lookup"><span data-stu-id="a1b72-106">Parameters</span></span>

<span data-ttu-id="a1b72-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="a1b72-107">*requestCallback* </span></span>  
<span data-ttu-id="a1b72-108">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="a1b72-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="a1b72-109">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="a1b72-109">*requestCookie* </span></span>  
<span data-ttu-id="a1b72-110">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="a1b72-110">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="a1b72-111">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="a1b72-111">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="a1b72-112">未使用。</span><span class="sxs-lookup"><span data-stu-id="a1b72-112">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="a1b72-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1b72-113">Return value</span></span>

<span data-ttu-id="a1b72-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a1b72-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a1b72-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a1b72-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1b72-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1b72-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a1b72-117">標頭</span><span class="sxs-lookup"><span data-stu-id="a1b72-117">Header</span></span></p></td><td><span data-ttu-id="a1b72-118">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="a1b72-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a1b72-119"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1b72-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a1b72-120">**ISummaryRequest**</span><span class="sxs-lookup"><span data-stu-id="a1b72-120">**ISummaryRequest**</span></span>](/windows/desktop/direct3dtools/isummaryrequest)

 

 
