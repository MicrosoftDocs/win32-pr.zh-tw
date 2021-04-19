---
description: 從指定的事件取得網格資料的非同步要求。
MS-HAID: vspixengine.IPipeLineStagesRequest3\_RequestMeshAsync\_EventID\_BSTR\_IPipeLineStagesCallback3\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesRequest3：： RequestMeshAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CAA36C96-3622-4D26-AB26-AD7960700B2A
api_name:
- IPipeLineStagesRequest3.RequestMeshAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 50fc73c803f708284ecef73f89ba74a452816bc9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970682"
---
# <a name="span-idvspixengineipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dwordspanipipelinestagesrequest3requestmeshasync-method"></a><span data-ttu-id="5e378-103"><span id="vspixengine.ipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dword"></span>IPipeLineStagesRequest3：： RequestMeshAsync 方法</span><span class="sxs-lookup"><span data-stu-id="5e378-103"><span id="vspixengine.ipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dword"></span>IPipeLineStagesRequest3::RequestMeshAsync method</span></span>

<span data-ttu-id="5e378-104">從指定的事件取得網格資料的非同步要求。</span><span class="sxs-lookup"><span data-stu-id="5e378-104">An asynchronous request to get mesh data from the specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e378-105">語法</span><span class="sxs-lookup"><span data-stu-id="5e378-105">Syntax</span></span>


```C++
HRESULT RequestMeshAsync(
   EventID                    eventID,
   BSTR                       meshFilename,
   IPipeLineStagesCallback3 * requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="5e378-106">參數</span><span class="sxs-lookup"><span data-stu-id="5e378-106">Parameters</span></span>

<span data-ttu-id="5e378-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="5e378-107">*eventID* </span></span>  
<span data-ttu-id="5e378-108">指定的事件。</span><span class="sxs-lookup"><span data-stu-id="5e378-108">The specified event.</span></span>

<span data-ttu-id="5e378-109">*meshFilename* </span><span class="sxs-lookup"><span data-stu-id="5e378-109">*meshFilename* </span></span>  
<span data-ttu-id="5e378-110">COM 字串，其中包含用來寫入網格資料之檔案的路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="5e378-110">A COM string containing the pathname of the file where the mesh data is written.</span></span>

<span data-ttu-id="5e378-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="5e378-111">*requestCallback* </span></span>  
<span data-ttu-id="5e378-112">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="5e378-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="5e378-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="5e378-113">*requestCookie* </span></span>  
<span data-ttu-id="5e378-114">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="5e378-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="5e378-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="5e378-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="5e378-116">未使用。</span><span class="sxs-lookup"><span data-stu-id="5e378-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="5e378-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="5e378-117">Return value</span></span>

<span data-ttu-id="5e378-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5e378-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5e378-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5e378-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e378-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e378-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5e378-121">標頭</span><span class="sxs-lookup"><span data-stu-id="5e378-121">Header</span></span></p></td><td><span data-ttu-id="5e378-122">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="5e378-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5e378-123"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e378-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5e378-124">**IPipeLineStagesRequest3**</span><span class="sxs-lookup"><span data-stu-id="5e378-124">**IPipeLineStagesRequest3**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest3)

 

 
