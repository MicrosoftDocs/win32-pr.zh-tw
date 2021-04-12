---
description: 要求取得物件的原始內容 (緩衝區、材質、轉譯目標視圖等 ) 。
MS-HAID: vspixengine.IBufferObjectDataRequest\_RequestAsync\_EventID\_DWORD\_BSTR\_BSTR\_IBufferObjectDataCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IBufferObjectDataRequest：： RequestAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 899954DC-6196-4F79-AFB4-5E692DAA03EC
api_name:
- IBufferObjectDataRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 97d35f656f373f2f0040d49a78a2c0d376bc4266
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108948"
---
# <a name="span-idvspixengineibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dwordspanibufferobjectdatarequestrequestasync-method"></a><span data-ttu-id="b81b7-103"><span id="vspixengine.ibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dword"></span>IBufferObjectDataRequest：： RequestAsync 方法</span><span class="sxs-lookup"><span data-stu-id="b81b7-103"><span id="vspixengine.ibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dword"></span>IBufferObjectDataRequest::RequestAsync method</span></span>

<span data-ttu-id="b81b7-104">要求取得物件的原始內容 (緩衝區、材質、轉譯目標視圖等） ) </span><span class="sxs-lookup"><span data-stu-id="b81b7-104">Requests to get the raw contents of an object (buffer, texture, render target view, etc.)</span></span>

## <a name="syntax"></a><span data-ttu-id="b81b7-105">語法</span><span class="sxs-lookup"><span data-stu-id="b81b7-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID                     eventID,
   DWORD                       RequestedDataUID,
   BSTR                        File,
   BSTR                        Format,
   IBufferObjectDataCallback * requestCallback,
   DWORD                       requestCookie,
   DWORD                       progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="b81b7-106">參數</span><span class="sxs-lookup"><span data-stu-id="b81b7-106">Parameters</span></span>

<span data-ttu-id="b81b7-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="b81b7-107">*eventID* </span></span>  
<span data-ttu-id="b81b7-108">指定要比對緩衝區內容的事件 (例如，轉譯目標可能會隨著時間而變更) 。</span><span class="sxs-lookup"><span data-stu-id="b81b7-108">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="b81b7-109">*RequestedDataUID* </span><span class="sxs-lookup"><span data-stu-id="b81b7-109">*RequestedDataUID* </span></span>  
<span data-ttu-id="b81b7-110">指定之物件的位址。</span><span class="sxs-lookup"><span data-stu-id="b81b7-110">The address of the specified object.</span></span>

<span data-ttu-id="b81b7-111">*檔* </span><span class="sxs-lookup"><span data-stu-id="b81b7-111">*File* </span></span>  
<span data-ttu-id="b81b7-112">COM 字串，其中包含寫入結果之檔案的路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="b81b7-112">A COM string that contains the pathname of the file where results are written.</span></span>

<span data-ttu-id="b81b7-113">*格式* </span><span class="sxs-lookup"><span data-stu-id="b81b7-113">*Format* </span></span>  
<span data-ttu-id="b81b7-114">目前無法使用。</span><span class="sxs-lookup"><span data-stu-id="b81b7-114">Not currently used.</span></span> <span data-ttu-id="b81b7-115">指定輸出格式的 COM 字串。</span><span class="sxs-lookup"><span data-stu-id="b81b7-115">A COM string that specifies the output format.</span></span>

<span data-ttu-id="b81b7-116">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="b81b7-116">*requestCallback* </span></span>  
<span data-ttu-id="b81b7-117">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="b81b7-117">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="b81b7-118">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="b81b7-118">*requestCookie* </span></span>  
<span data-ttu-id="b81b7-119">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="b81b7-119">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="b81b7-120">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="b81b7-120">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="b81b7-121">未使用。</span><span class="sxs-lookup"><span data-stu-id="b81b7-121">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="b81b7-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="b81b7-122">Return value</span></span>

<span data-ttu-id="b81b7-123">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b81b7-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b81b7-124">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b81b7-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b81b7-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b81b7-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b81b7-126">標頭</span><span class="sxs-lookup"><span data-stu-id="b81b7-126">Header</span></span></p></td><td><span data-ttu-id="b81b7-127">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="b81b7-127">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b81b7-128"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="b81b7-128"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b81b7-129">**IBufferObjectDataRequest**</span><span class="sxs-lookup"><span data-stu-id="b81b7-129">**IBufferObjectDataRequest**</span></span>](/windows/desktop/direct3dtools/ibufferobjectdatarequest)

 

 
