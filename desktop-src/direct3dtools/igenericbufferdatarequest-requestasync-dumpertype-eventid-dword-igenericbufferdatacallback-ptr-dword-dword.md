---
description: 要求傳回泛型物件資料，此資料會針對指定的事件和指定的格式來描述 vsglog 檔中的物件。
MS-HAID: vspixengine.IGenericBufferDataRequest\_RequestAsync\_DumperType\_EventID\_DWORD\_IGenericBufferDataCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IGenericBufferDataRequest：： RequestAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 542E20F9-B91D-4A05-AEE8-9DD2E80B76DB
api_name:
- IGenericBufferDataRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6d8860b2de7c3dce5c6f8b61467bfe147530ed76
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973555"
---
# <a name="span-idvspixengineigenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dwordspanigenericbufferdatarequestrequestasync-method"></a><span data-ttu-id="0b415-103"><span id="vspixengine.igenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dword"></span>IGenericBufferDataRequest：： RequestAsync 方法</span><span class="sxs-lookup"><span data-stu-id="0b415-103"><span id="vspixengine.igenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dword"></span>IGenericBufferDataRequest::RequestAsync method</span></span>

<span data-ttu-id="0b415-104">要求傳回泛型物件資料，此資料會針對指定的事件和指定的格式來描述 vsglog 檔中的物件。</span><span class="sxs-lookup"><span data-stu-id="0b415-104">Requests to return generic object data that describes an object in the .vsglog file for the specified event and in the specified format.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b415-105">語法</span><span class="sxs-lookup"><span data-stu-id="0b415-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DumperType                   dumperType,
   EventID                      eventID,
   DWORD                        RequestedDataUID,
   IGenericBufferDataCallback * requestCallback,
   DWORD                        requestCookie,
   DWORD                        progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="0b415-106">參數</span><span class="sxs-lookup"><span data-stu-id="0b415-106">Parameters</span></span>

<span data-ttu-id="0b415-107">*dumperType* </span><span class="sxs-lookup"><span data-stu-id="0b415-107">*dumperType* </span></span>  
<span data-ttu-id="0b415-108">物件的文字表示格式指定的格式 (HTML、XML 等等 ) </span><span class="sxs-lookup"><span data-stu-id="0b415-108">The specified format of the textual representation of the object (HTML, XML, etc.)</span></span>

<span data-ttu-id="0b415-109">*eventID* </span><span class="sxs-lookup"><span data-stu-id="0b415-109">*eventID* </span></span>  
<span data-ttu-id="0b415-110">指定要比對緩衝區內容的事件 (例如，轉譯目標可能會隨著時間而變更) 。</span><span class="sxs-lookup"><span data-stu-id="0b415-110">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="0b415-111">*RequestedDataUID* </span><span class="sxs-lookup"><span data-stu-id="0b415-111">*RequestedDataUID* </span></span>  
<span data-ttu-id="0b415-112">指定之物件的位址。</span><span class="sxs-lookup"><span data-stu-id="0b415-112">The address of the specified object.</span></span>

<span data-ttu-id="0b415-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="0b415-113">*requestCallback* </span></span>  
<span data-ttu-id="0b415-114">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="0b415-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="0b415-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="0b415-115">*requestCookie* </span></span>  
<span data-ttu-id="0b415-116">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="0b415-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="0b415-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="0b415-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="0b415-118">未使用。</span><span class="sxs-lookup"><span data-stu-id="0b415-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="0b415-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="0b415-119">Return value</span></span>

<span data-ttu-id="0b415-120">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="0b415-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0b415-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0b415-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b415-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b415-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0b415-123">標頭</span><span class="sxs-lookup"><span data-stu-id="0b415-123">Header</span></span></p></td><td><span data-ttu-id="0b415-124">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="0b415-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="0b415-125"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b415-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="0b415-126">**IGenericBufferDataRequest**</span><span class="sxs-lookup"><span data-stu-id="0b415-126">**IGenericBufferDataRequest**</span></span>](/windows/desktop/direct3dtools/igenericbufferdatarequest)

 

 
