---
description: 要求將磚材質的內容取得為。DDS (DirectDraw 介面) 檔。
MS-HAID: vspixengine.ITileRequest\_RequestTextureTileAsync\_EventID\_DWORD\_UINT\_UINT\_UINT\_UINT\_BSTR\_ITextureCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ITileRequest：： RequestTextureTileAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E3F4FAC2-E7D9-4FDF-BE64-73D3EA175A8F
api_name:
- ITileRequest.RequestTextureTileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e22c3b54c1e04242805d698c37a1d4dd2709fa0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109308"
---
# <a name="span-idvspixengineitilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dwordspanitilerequestrequesttexturetileasync-method"></a><span data-ttu-id="178f3-103"><span id="vspixengine.itilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dword"></span>ITileRequest：： RequestTextureTileAsync 方法</span><span class="sxs-lookup"><span data-stu-id="178f3-103"><span id="vspixengine.itilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dword"></span>ITileRequest::RequestTextureTileAsync method</span></span>

<span data-ttu-id="178f3-104">要求將磚材質的內容取得為。DDS (DirectDraw 介面) 檔。</span><span class="sxs-lookup"><span data-stu-id="178f3-104">Requests to get the contents of a tiled texture as a .DDS (DirectDraw Surface) file.</span></span>

## <a name="syntax"></a><span data-ttu-id="178f3-105">語法</span><span class="sxs-lookup"><span data-stu-id="178f3-105">Syntax</span></span>


```C++
HRESULT RequestTextureTileAsync(
   EventID            eventID,
   DWORD              textureFileptr,
   UINT               tileSubresource,
   UINT               tileX,
   UINT               tileY,
   UINT               tileZ,
   BSTR               ddsFilename,
   ITextureCallback * pRequestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="178f3-106">參數</span><span class="sxs-lookup"><span data-stu-id="178f3-106">Parameters</span></span>

<span data-ttu-id="178f3-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="178f3-107">*eventID* </span></span>  
<span data-ttu-id="178f3-108">指定要比對緩衝區內容的事件 (例如，轉譯目標可能會隨著時間而變更) 。</span><span class="sxs-lookup"><span data-stu-id="178f3-108">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="178f3-109">*textureFileptr* </span><span class="sxs-lookup"><span data-stu-id="178f3-109">*textureFileptr* </span></span>  
<span data-ttu-id="178f3-110">指定之材質物件的位址。</span><span class="sxs-lookup"><span data-stu-id="178f3-110">The address of the specified texture object.</span></span>

<span data-ttu-id="178f3-111">*tileSubresource* </span><span class="sxs-lookup"><span data-stu-id="178f3-111">*tileSubresource* </span></span>  
<span data-ttu-id="178f3-112">磚的指定 subresource。</span><span class="sxs-lookup"><span data-stu-id="178f3-112">The specified subresource of the tile.</span></span>

<span data-ttu-id="178f3-113">*tileX* </span><span class="sxs-lookup"><span data-stu-id="178f3-113">*tileX* </span></span>  
<span data-ttu-id="178f3-114">指定的磚 X 位置。</span><span class="sxs-lookup"><span data-stu-id="178f3-114">The specified tile X position.</span></span>

<span data-ttu-id="178f3-115">*tileY* </span><span class="sxs-lookup"><span data-stu-id="178f3-115">*tileY* </span></span>  
<span data-ttu-id="178f3-116">指定的磚 Y 位置。</span><span class="sxs-lookup"><span data-stu-id="178f3-116">The specified tile Y position.</span></span>

<span data-ttu-id="178f3-117">*tileZ* </span><span class="sxs-lookup"><span data-stu-id="178f3-117">*tileZ* </span></span>  
<span data-ttu-id="178f3-118">指定的磚 Z 位置。</span><span class="sxs-lookup"><span data-stu-id="178f3-118">The specified tile Z position.</span></span>

<span data-ttu-id="178f3-119">*ddsFilename* </span><span class="sxs-lookup"><span data-stu-id="178f3-119">*ddsFilename* </span></span>  
<span data-ttu-id="178f3-120">COM 字串，其中包含寫入結果之 dd 檔案的路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="178f3-120">A COM string that contains the pathname of the .dds file where results are written.</span></span>

<span data-ttu-id="178f3-121">*pRequestCallback* </span><span class="sxs-lookup"><span data-stu-id="178f3-121">*pRequestCallback* </span></span>  
<span data-ttu-id="178f3-122">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="178f3-122">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="178f3-123">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="178f3-123">*requestCookie* </span></span>  
<span data-ttu-id="178f3-124">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="178f3-124">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="178f3-125">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="178f3-125">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="178f3-126">未使用。</span><span class="sxs-lookup"><span data-stu-id="178f3-126">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="178f3-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="178f3-127">Return value</span></span>

<span data-ttu-id="178f3-128">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="178f3-128">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="178f3-129">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="178f3-129">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="178f3-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="178f3-130">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="178f3-131">標頭</span><span class="sxs-lookup"><span data-stu-id="178f3-131">Header</span></span></p></td><td><span data-ttu-id="178f3-132">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="178f3-132">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="178f3-133"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="178f3-133"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="178f3-134">**ITileRequest**</span><span class="sxs-lookup"><span data-stu-id="178f3-134">**ITileRequest**</span></span>](/windows/desktop/direct3dtools/itilerequest)

 

 
