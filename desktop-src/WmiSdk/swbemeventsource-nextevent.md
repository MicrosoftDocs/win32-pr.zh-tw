---
description: 如果有可用的事件，SWbemEventSource 物件的 NextEvent 方法就會從事件查詢中抓取事件。
ms.assetid: ff2d54d4-b8ee-4bb8-b6f7-081a1ca20489
ms.tgt_platform: multiple
title: 'SWbemEventSource. NextEvent 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 02fbc32557ab29c66849a4249d26cc2ca41564e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997968"
---
# <a name="swbemeventsourcenextevent-method"></a><span data-ttu-id="66e42-103">SWbemEventSource. NextEvent 方法</span><span class="sxs-lookup"><span data-stu-id="66e42-103">SWbemEventSource.NextEvent method</span></span>

<span data-ttu-id="66e42-104">如果有可用的事件， [**SWbemEventSource**](swbemeventsource.md)物件的 **NextEvent** 方法就會從事件查詢中抓取事件。</span><span class="sxs-lookup"><span data-stu-id="66e42-104">If an event is available, the **NextEvent** method of the [**SWbemEventSource**](swbemeventsource.md) object retrieves the event from an event query.</span></span>

<span data-ttu-id="66e42-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="66e42-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="66e42-106">語法</span><span class="sxs-lookup"><span data-stu-id="66e42-106">Syntax</span></span>


```VB
objWbemObject = .NextEvent( _
  [ ByVal iTimeoutMs ] _
)
```



## <a name="parameters"></a><span data-ttu-id="66e42-107">參數</span><span class="sxs-lookup"><span data-stu-id="66e42-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66e42-108">*iTimeoutMs* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="66e42-108">*iTimeoutMs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="66e42-109">在傳回逾時錯誤之前，呼叫等候事件的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="66e42-109">Number of milliseconds the call waits for an event before returning a time-out error.</span></span> <span data-ttu-id="66e42-110">這個參數的預設值是 **wbemTimeoutInfinite** (-1) ，它會將呼叫指示無限期等候。</span><span class="sxs-lookup"><span data-stu-id="66e42-110">The default value for this parameter is **wbemTimeoutInfinite** (-1), which directs the call to wait indefinitely.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66e42-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="66e42-111">Return value</span></span>

<span data-ttu-id="66e42-112">如果 **NextEvent** 方法成功，它會傳回 [**SWbemObject**](swbemobject.md) 物件，其中包含所要求的事件。</span><span class="sxs-lookup"><span data-stu-id="66e42-112">If the **NextEvent** method is successful, it returns an [**SWbemObject**](swbemobject.md) object that contains the requested event.</span></span> <span data-ttu-id="66e42-113">如果呼叫超時，傳回的物件會是 **Null** ，並引發錯誤。</span><span class="sxs-lookup"><span data-stu-id="66e42-113">If the call times out, the returned object is **NULL** and an error is raised.</span></span>

## <a name="error-codes"></a><span data-ttu-id="66e42-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="66e42-114">Error codes</span></span>

<span data-ttu-id="66e42-115">**NextEvent** 方法完成後， **Err** 物件可能會包含下列清單中的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="66e42-115">Upon the completion of the **NextEvent** method, the **Err** object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="66e42-116">**wbemErrTimedOut** -0x80043001</span><span class="sxs-lookup"><span data-stu-id="66e42-116">**wbemErrTimedOut** - 0x80043001</span></span>
</dt> <dd>

<span data-ttu-id="66e42-117">要求的事件未在 ITimeoutMs 中指定的時間量內到達 *。*</span><span class="sxs-lookup"><span data-stu-id="66e42-117">Requested event did not arrive in the amount of time specified in *iTimeoutMs.*</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66e42-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="66e42-118">Requirements</span></span>



| <span data-ttu-id="66e42-119">需求</span><span class="sxs-lookup"><span data-stu-id="66e42-119">Requirement</span></span> | <span data-ttu-id="66e42-120">值</span><span class="sxs-lookup"><span data-stu-id="66e42-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66e42-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66e42-121">Minimum supported client</span></span><br/> | <span data-ttu-id="66e42-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66e42-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="66e42-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66e42-123">Minimum supported server</span></span><br/> | <span data-ttu-id="66e42-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66e42-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="66e42-125">標頭</span><span class="sxs-lookup"><span data-stu-id="66e42-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="66e42-126"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="66e42-126"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="66e42-127">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="66e42-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="66e42-128"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="66e42-128"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="66e42-129">DLL</span><span class="sxs-lookup"><span data-stu-id="66e42-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66e42-130"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66e42-130"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="66e42-131">CLSID</span><span class="sxs-lookup"><span data-stu-id="66e42-131">CLSID</span></span><br/>                    | <span data-ttu-id="66e42-132">CLSID \_ SWbemEventSource</span><span class="sxs-lookup"><span data-stu-id="66e42-132">CLSID\_SWbemEventSource</span></span><br/>                                                      |
| <span data-ttu-id="66e42-133">IID</span><span class="sxs-lookup"><span data-stu-id="66e42-133">IID</span></span><br/>                      | <span data-ttu-id="66e42-134">IID \_ ISWbemEventSource</span><span class="sxs-lookup"><span data-stu-id="66e42-134">IID\_ISWbemEventSource</span></span><br/>                                                       |



 

 




