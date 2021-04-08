---
description: 要求從物件資料表取得指定之事件的指定資訊。
MS-HAID: vspixengine.IObjectTableRequest\_RequestAsync\_DWORD\_DWORD\_DWORD\_arr\_IObjectTableCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IObjectTableRequest：： RequestAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: EE40F584-CDDE-465D-B4CB-A98B917DD0EE
api_name:
- IObjectTableRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2c9108708475b27a7a1882051c7f0177e14470f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688040"
---
# <a name="span-idvspixengineiobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dwordspaniobjecttablerequestrequestasync-method"></a><span data-ttu-id="e3594-103"><span id="vspixengine.iobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dword"></span>IObjectTableRequest：： RequestAsync 方法</span><span class="sxs-lookup"><span data-stu-id="e3594-103"><span id="vspixengine.iobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dword"></span>IObjectTableRequest::RequestAsync method</span></span>

<span data-ttu-id="e3594-104">要求從物件資料表取得指定之事件的指定資訊。</span><span class="sxs-lookup"><span data-stu-id="e3594-104">Requests to get specified information from the object table for the specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3594-105">語法</span><span class="sxs-lookup"><span data-stu-id="e3594-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  eventID,
   DWORD                  numColumns,
   DWORD []               count1_columns,
   IObjectTableCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="e3594-106">參數</span><span class="sxs-lookup"><span data-stu-id="e3594-106">Parameters</span></span>

<span data-ttu-id="e3594-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="e3594-107">*eventID* </span></span>  
<span data-ttu-id="e3594-108">指定的事件。</span><span class="sxs-lookup"><span data-stu-id="e3594-108">The specified event.</span></span>

<span data-ttu-id="e3594-109">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="e3594-109">*numColumns* </span></span>  
<span data-ttu-id="e3594-110"> (欄位的資料行數目) 要取得的資訊。</span><span class="sxs-lookup"><span data-stu-id="e3594-110">The number of columns (fields) of information to get.</span></span>

<span data-ttu-id="e3594-111">*count1 資料 \_ 行* </span><span class="sxs-lookup"><span data-stu-id="e3594-111">*count1\_columns* </span></span>  
<span data-ttu-id="e3594-112">指定的資料行 (欄位) 。</span><span class="sxs-lookup"><span data-stu-id="e3594-112">The specified columns (fields).</span></span>

<span data-ttu-id="e3594-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="e3594-113">*requestCallback* </span></span>  
<span data-ttu-id="e3594-114">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="e3594-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="e3594-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="e3594-115">*requestCookie* </span></span>  
<span data-ttu-id="e3594-116">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="e3594-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="e3594-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="e3594-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="e3594-118">未使用。</span><span class="sxs-lookup"><span data-stu-id="e3594-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="e3594-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="e3594-119">Return value</span></span>

<span data-ttu-id="e3594-120">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e3594-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e3594-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e3594-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3594-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3594-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e3594-123">標頭</span><span class="sxs-lookup"><span data-stu-id="e3594-123">Header</span></span></p></td><td><span data-ttu-id="e3594-124">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="e3594-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e3594-125"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3594-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e3594-126">**IObjectTableRequest**</span><span class="sxs-lookup"><span data-stu-id="e3594-126">**IObjectTableRequest**</span></span>](/windows/desktop/direct3dtools/iobjecttablerequest)

 

 
