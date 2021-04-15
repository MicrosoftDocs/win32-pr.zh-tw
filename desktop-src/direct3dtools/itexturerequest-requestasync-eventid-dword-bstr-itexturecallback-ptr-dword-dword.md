---
description: 要求將材質的內容取得為。DDS (DirectDraw 介面) 檔。
MS-HAID: vspixengine.ITextureRequest\_RequestAsync\_EventID\_DWORD\_BSTR\_ITextureCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ITextureRequest：： RequestAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 89A9F230-D296-43CD-A2A6-747057750EED
api_name:
- ITextureRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5abfee1b26fd2145aef8e01239cc0b874ee54e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467903"
---
# <a name="span-idvspixengineitexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dwordspanitexturerequestrequestasync-method"></a><span data-ttu-id="fe4df-103"><span id="vspixengine.itexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dword"></span>ITextureRequest：： RequestAsync 方法</span><span class="sxs-lookup"><span data-stu-id="fe4df-103"><span id="vspixengine.itexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dword"></span>ITextureRequest::RequestAsync method</span></span>

<span data-ttu-id="fe4df-104">要求將材質的內容取得為。DDS (DirectDraw 介面) 檔。</span><span class="sxs-lookup"><span data-stu-id="fe4df-104">Requests to get the contents of a texture as a .DDS (DirectDraw Surface) file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe4df-105">語法</span><span class="sxs-lookup"><span data-stu-id="fe4df-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID            eventID,
   DWORD              textureFileptr,
   BSTR               ddsFilename,
   ITextureCallback * pRequestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="fe4df-106">參數</span><span class="sxs-lookup"><span data-stu-id="fe4df-106">Parameters</span></span>

<span data-ttu-id="fe4df-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="fe4df-107">*eventID* </span></span>  
<span data-ttu-id="fe4df-108">指定要比對緩衝區內容的事件 (例如，轉譯目標可能會隨著時間而變更) 。</span><span class="sxs-lookup"><span data-stu-id="fe4df-108">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="fe4df-109">*textureFileptr* </span><span class="sxs-lookup"><span data-stu-id="fe4df-109">*textureFileptr* </span></span>  
<span data-ttu-id="fe4df-110">材質物件的位址。</span><span class="sxs-lookup"><span data-stu-id="fe4df-110">The address of the texture object.</span></span>

<span data-ttu-id="fe4df-111">*ddsFilename* </span><span class="sxs-lookup"><span data-stu-id="fe4df-111">*ddsFilename* </span></span>  
<span data-ttu-id="fe4df-112">COM 字串，其中包含寫入結果之 dd 檔案的路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="fe4df-112">A COM string that contains the pathname of the .dds file where results are written.</span></span>

<span data-ttu-id="fe4df-113">*pRequestCallback* </span><span class="sxs-lookup"><span data-stu-id="fe4df-113">*pRequestCallback* </span></span>  
<span data-ttu-id="fe4df-114">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="fe4df-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="fe4df-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="fe4df-115">*requestCookie* </span></span>  
<span data-ttu-id="fe4df-116">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="fe4df-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="fe4df-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="fe4df-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="fe4df-118">未使用。</span><span class="sxs-lookup"><span data-stu-id="fe4df-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="fe4df-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe4df-119">Return value</span></span>

<span data-ttu-id="fe4df-120">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="fe4df-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fe4df-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fe4df-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe4df-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe4df-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fe4df-123">標頭</span><span class="sxs-lookup"><span data-stu-id="fe4df-123">Header</span></span></p></td><td><span data-ttu-id="fe4df-124">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="fe4df-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="fe4df-125"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe4df-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="fe4df-126">**ITextureRequest**</span><span class="sxs-lookup"><span data-stu-id="fe4df-126">**ITextureRequest**</span></span>](/windows/desktop/direct3dtools/itexturerequest)

 

 
