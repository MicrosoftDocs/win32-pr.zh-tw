---
description: 非同步要求，以取得在圖形記錄檔中所捕捉的清單方塊架。
MS-HAID: vspixengine.IFrameListRequest\_RequestAsync\_IFrameListCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFrameListRequest：： RequestAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 309C28F2-CE01-49E7-9A21-5053E3ED7721
api_name:
- IFrameListRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3627fc5ef3a425ae7607009b4ad382080ea99192
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025649"
---
# <a name="span-idvspixengineiframelistrequest_requestasync_iframelistcallback_ptr_dword_dwordspaniframelistrequestrequestasync-method"></a><span data-ttu-id="a3a82-103"><span id="vspixengine.iframelistrequest_requestasync_iframelistcallback_ptr_dword_dword"></span>IFrameListRequest：： RequestAsync 方法</span><span class="sxs-lookup"><span data-stu-id="a3a82-103"><span id="vspixengine.iframelistrequest_requestasync_iframelistcallback_ptr_dword_dword"></span>IFrameListRequest::RequestAsync method</span></span>

<span data-ttu-id="a3a82-104">非同步要求，以取得在圖形記錄檔中所捕捉的清單方塊架。</span><span class="sxs-lookup"><span data-stu-id="a3a82-104">An asynchronous request to get the list frames captured in the graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3a82-105">語法</span><span class="sxs-lookup"><span data-stu-id="a3a82-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   IFrameListCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="a3a82-106">參數</span><span class="sxs-lookup"><span data-stu-id="a3a82-106">Parameters</span></span>

<span data-ttu-id="a3a82-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="a3a82-107">*requestCallback* </span></span>  
<span data-ttu-id="a3a82-108">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="a3a82-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="a3a82-109">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="a3a82-109">*requestCookie* </span></span>  
<span data-ttu-id="a3a82-110">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="a3a82-110">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="a3a82-111">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="a3a82-111">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="a3a82-112">未使用。</span><span class="sxs-lookup"><span data-stu-id="a3a82-112">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="a3a82-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a3a82-113">Return value</span></span>

<span data-ttu-id="a3a82-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a3a82-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a3a82-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a3a82-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3a82-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3a82-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a3a82-117">標頭</span><span class="sxs-lookup"><span data-stu-id="a3a82-117">Header</span></span></p></td><td><span data-ttu-id="a3a82-118">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="a3a82-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a3a82-119"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3a82-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a3a82-120">**IFrameListRequest**</span><span class="sxs-lookup"><span data-stu-id="a3a82-120">**IFrameListRequest**</span></span>](/windows/desktop/direct3dtools/iframelistrequest)

 

 
