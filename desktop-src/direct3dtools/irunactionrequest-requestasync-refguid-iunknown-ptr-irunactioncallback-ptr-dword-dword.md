---
description: 起始動作的非同步要求 (例如，捕捉引擎中) 的畫面格。
MS-HAID: vspixengine.IRunActionRequest\_RequestAsync\_REFGUID\_IUnknown\_ptr\_IRunActionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IRunActionRequest：： RequestAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4A4DF4BE-383D-4B36-9195-61720C3B4D97
api_name:
- IRunActionRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 179abf44231d122ca82527fc5739b876395c327b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109741"
---
# <a name="span-idvspixengineirunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dwordspanirunactionrequestrequestasync-method"></a><span data-ttu-id="9a645-103"><span id="vspixengine.irunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dword"></span>IRunActionRequest：： RequestAsync 方法</span><span class="sxs-lookup"><span data-stu-id="9a645-103"><span id="vspixengine.irunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dword"></span>IRunActionRequest::RequestAsync method</span></span>

<span data-ttu-id="9a645-104">起始動作的非同步要求 (例如，捕捉引擎中) 的畫面格。</span><span class="sxs-lookup"><span data-stu-id="9a645-104">An asynchronous request to initiate an action (for example, capture a frame) in the engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a645-105">語法</span><span class="sxs-lookup"><span data-stu-id="9a645-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   REFGUID              action,
   IUnknown *           actionPayload,
   IRunActionCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="9a645-106">參數</span><span class="sxs-lookup"><span data-stu-id="9a645-106">Parameters</span></span>

<span data-ttu-id="9a645-107">*行動* </span><span class="sxs-lookup"><span data-stu-id="9a645-107">*action* </span></span>  
<span data-ttu-id="9a645-108">指定的動作。</span><span class="sxs-lookup"><span data-stu-id="9a645-108">The specified action.</span></span>

<span data-ttu-id="9a645-109">*actionPayload* </span><span class="sxs-lookup"><span data-stu-id="9a645-109">*actionPayload* </span></span>  
<span data-ttu-id="9a645-110">指定之動作的裝載。</span><span class="sxs-lookup"><span data-stu-id="9a645-110">The payload of the specified action.</span></span>

<span data-ttu-id="9a645-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="9a645-111">*requestCallback* </span></span>  
<span data-ttu-id="9a645-112">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="9a645-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="9a645-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="9a645-113">*requestCookie* </span></span>  
<span data-ttu-id="9a645-114">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="9a645-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="9a645-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="9a645-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="9a645-116">未使用。</span><span class="sxs-lookup"><span data-stu-id="9a645-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a645-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a645-117">Return value</span></span>

<span data-ttu-id="9a645-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9a645-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9a645-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9a645-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a645-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a645-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9a645-121">標頭</span><span class="sxs-lookup"><span data-stu-id="9a645-121">Header</span></span></p></td><td><span data-ttu-id="9a645-122">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="9a645-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="9a645-123"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a645-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="9a645-124">**IRunActionRequest**</span><span class="sxs-lookup"><span data-stu-id="9a645-124">**IRunActionRequest**</span></span>](/windows/desktop/direct3dtools/irunactionrequest)

 

 
