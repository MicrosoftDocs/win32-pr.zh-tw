---
description: 回呼函式，用來通知主機動作的結果 (例如，捕捉其所要求的框架) 。
MS-HAID: vspixengine.IRunActionCallback\_RequestResult\_IUnknown\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IRunActionCallback：： RequestResult 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5D6B1599-2CF4-46E7-92DB-5D93DD5AD0EE
api_name:
- IRunActionCallback.RequestResult
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8f2d5eea98b167af30bfe0412acb10f83f83d3db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109744"
---
# <a name="span-idvspixengineirunactioncallback_requestresult_iunknown_ptrspanirunactioncallbackrequestresult-method"></a><span data-ttu-id="dc824-103"><span id="vspixengine.irunactioncallback_requestresult_iunknown_ptr"></span>IRunActionCallback：： RequestResult 方法</span><span class="sxs-lookup"><span data-stu-id="dc824-103"><span id="vspixengine.irunactioncallback_requestresult_iunknown_ptr"></span>IRunActionCallback::RequestResult method</span></span>

<span data-ttu-id="dc824-104">回呼函式，用來通知主機動作的結果 (例如，捕捉其所要求的框架) 。</span><span class="sxs-lookup"><span data-stu-id="dc824-104">A callback function used to notify the host of results from an action (for example, capture a frame) that it requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc824-105">語法</span><span class="sxs-lookup"><span data-stu-id="dc824-105">Syntax</span></span>


```C++
HRESULT RequestResult(
   IUnknown * actionResult
);
```

## <a name="parameters"></a><span data-ttu-id="dc824-106">參數</span><span class="sxs-lookup"><span data-stu-id="dc824-106">Parameters</span></span>

<span data-ttu-id="dc824-107">*actionResult* </span><span class="sxs-lookup"><span data-stu-id="dc824-107">*actionResult* </span></span>  
<span data-ttu-id="dc824-108">動作的結果。</span><span class="sxs-lookup"><span data-stu-id="dc824-108">The result of the action.</span></span>

## <a name="return-value"></a><span data-ttu-id="dc824-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="dc824-109">Return value</span></span>

<span data-ttu-id="dc824-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="dc824-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dc824-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dc824-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc824-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc824-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="dc824-113">標頭</span><span class="sxs-lookup"><span data-stu-id="dc824-113">Header</span></span></p></td><td><span data-ttu-id="dc824-114">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="dc824-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="dc824-115"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc824-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="dc824-116">**IRunActionCallback**</span><span class="sxs-lookup"><span data-stu-id="dc824-116">**IRunActionCallback**</span></span>](/windows/desktop/direct3dtools/irunactioncallback)

 

 
