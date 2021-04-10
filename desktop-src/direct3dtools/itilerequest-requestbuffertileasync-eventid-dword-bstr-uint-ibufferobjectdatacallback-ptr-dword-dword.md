---
description: 要求取得磚的原始內容。
MS-HAID: vspixengine.ITileRequest_RequestBufferTileAsync_EventID_DWORD_BSTR_UINT_IBufferObjectDataCallback_ptr_DWORD_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ITileRequest：： RequestBufferTileAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2D68766F-1BED-439E-AC51-790471DA4F70
api_name:
- ITileRequest.RequestBufferTileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 83f013b4bc3235ece2850c75324333e4b59d298f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187564"
---
# <a name="span-idvspixengineitilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dwordspanitilerequestrequestbuffertileasync-method"></a><span data-ttu-id="65038-103"><span id="vspixengine.itilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dword"></span>ITileRequest：： RequestBufferTileAsync 方法</span><span class="sxs-lookup"><span data-stu-id="65038-103"><span id="vspixengine.itilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dword"></span>ITileRequest::RequestBufferTileAsync method</span></span>

<span data-ttu-id="65038-104">要求取得磚的原始內容。</span><span class="sxs-lookup"><span data-stu-id="65038-104">Requests to get the raw contents of a tile.</span></span>

## <a name="syntax"></a><span data-ttu-id="65038-105">語法</span><span class="sxs-lookup"><span data-stu-id="65038-105">Syntax</span></span>


```C++
HRESULT RequestBufferTileAsync(
   EventID                     eventID,
   DWORD                       RequestedDataUID,
   BSTR                        File,
   UINT                        tileIndex,
   IBufferObjectDataCallback * requestCallback,
   DWORD                       requestCookie,
   DWORD                       progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="65038-106">參數</span><span class="sxs-lookup"><span data-stu-id="65038-106">Parameters</span></span>

<span data-ttu-id="65038-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="65038-107">*eventID* </span></span>  
<span data-ttu-id="65038-108">指定的事件，以比對磚的內容 (例如，轉譯目標可能會隨著時間而變更) 。</span><span class="sxs-lookup"><span data-stu-id="65038-108">The specified event to match the tile's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="65038-109">*RequestedDataUID* </span><span class="sxs-lookup"><span data-stu-id="65038-109">*RequestedDataUID* </span></span>  
<span data-ttu-id="65038-110">指定之磚的位址。</span><span class="sxs-lookup"><span data-stu-id="65038-110">The address of the specified tile.</span></span>

<span data-ttu-id="65038-111">*檔* </span><span class="sxs-lookup"><span data-stu-id="65038-111">*File* </span></span>  
<span data-ttu-id="65038-112">COM 字串，其中包含寫入結果之檔案的路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="65038-112">A COM string that contains the pathname of the file where results are written.</span></span>

<span data-ttu-id="65038-113">*tileIndex* </span><span class="sxs-lookup"><span data-stu-id="65038-113">*tileIndex* </span></span>  
<span data-ttu-id="65038-114">指定之圖格的索引。</span><span class="sxs-lookup"><span data-stu-id="65038-114">The index of the specified tile.</span></span>

<span data-ttu-id="65038-115">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="65038-115">*requestCallback* </span></span>  
<span data-ttu-id="65038-116">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="65038-116">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="65038-117">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="65038-117">*requestCookie* </span></span>  
<span data-ttu-id="65038-118">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="65038-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="65038-119">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="65038-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="65038-120">未使用。</span><span class="sxs-lookup"><span data-stu-id="65038-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="65038-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="65038-121">Return value</span></span>

<span data-ttu-id="65038-122">如果這個方法成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="65038-122">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="65038-123">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="65038-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="65038-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="65038-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="65038-125">標頭</span><span class="sxs-lookup"><span data-stu-id="65038-125">Header</span></span></p></td><td><span data-ttu-id="65038-126">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="65038-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="65038-127"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="65038-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="65038-128">**ITileRequest**</span><span class="sxs-lookup"><span data-stu-id="65038-128">**ITileRequest**</span></span>](/windows/desktop/direct3dtools/itilerequest)

 

 
