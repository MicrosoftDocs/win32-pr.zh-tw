---
description: 當非同步 Put 作業完成時，就會觸發 SWbemSink 物件的 OnObjectPut 事件。 此事件會傳回實例或已儲存類別的物件路徑。
ms.assetid: 2046dd03-ac2c-49fa-b1ad-a458967709e5
ms.tgt_platform: multiple
title: 'ISWbemSinkEvents：： OnObjectPut 事件 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectPut
- ISWbemSinkEvents.OnObjectPut
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c6ed42105efe407558d80cd108e657e396e88763
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195224"
---
# <a name="iswbemsinkeventsonobjectput-event"></a><span data-ttu-id="78319-104">ISWbemSinkEvents：： OnObjectPut 事件</span><span class="sxs-lookup"><span data-stu-id="78319-104">ISWbemSinkEvents::OnObjectPut event</span></span>

<span data-ttu-id="78319-105">當非同步 Put 作業完成時，就會觸發 [**SWbemSink**](swbemsink.md)物件的 **OnObjectPut** 事件。</span><span class="sxs-lookup"><span data-stu-id="78319-105">The **OnObjectPut** event of an [**SWbemSink**](swbemsink.md) object is triggered when an asynchronous Put operation is complete.</span></span> <span data-ttu-id="78319-106">此事件會傳回實例或已儲存類別的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="78319-106">This event returns the object path of the instance or the saved class.</span></span>

<span data-ttu-id="78319-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="78319-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="78319-108">語法</span><span class="sxs-lookup"><span data-stu-id="78319-108">Syntax</span></span>


```VB
SWbemSink.OnObjectPut( _
  ByVal objWbemObjectPath, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="78319-109">參數</span><span class="sxs-lookup"><span data-stu-id="78319-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78319-110">*objWbemObjectPath*</span><span class="sxs-lookup"><span data-stu-id="78319-110">*objWbemObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="78319-111">[**SWbemObjectPath**](swbemobjectpath.md)物件，其中包含 put 作業寫入至 WMI 之實例或類別的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="78319-111">An [**SWbemObjectPath**](swbemobjectpath.md) object, that contains the object path of the instance or class that the put operation writes to WMI.</span></span>

</dd> <dt>

<span data-ttu-id="78319-112">*objWbemAsyncCoNtext*</span><span class="sxs-lookup"><span data-stu-id="78319-112">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="78319-113">傳遞至原始非同步呼叫的 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="78319-113">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="78319-114">使用這個參數來識別非同步呼叫的來源，此呼叫會在使用這個物件接收進行多個非同步呼叫時觸發這個事件。</span><span class="sxs-lookup"><span data-stu-id="78319-114">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78319-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="78319-115">Return value</span></span>

<span data-ttu-id="78319-116">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="78319-116">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="78319-117">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="78319-117">Error codes</span></span>

<span data-ttu-id="78319-118">**OnObjectPut** 事件完成之後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="78319-118">After the completion of the **OnObjectPut** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="78319-119">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="78319-119">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="78319-120">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="78319-120">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="78319-121">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="78319-121">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="78319-122">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="78319-122">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="78319-123">**wbemErrTransportFailure** -2147749909 (0x80041015) </span><span class="sxs-lookup"><span data-stu-id="78319-123">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="78319-124">發生網路錯誤，導致無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="78319-124">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78319-125">備註</span><span class="sxs-lookup"><span data-stu-id="78319-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="78319-126">非同步回呼可讓未經驗證的使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="78319-126">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="78319-127">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="78319-127">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="78319-128">若要消除風險，請使用半同步通訊或同步通訊。</span><span class="sxs-lookup"><span data-stu-id="78319-128">To eliminate the risks, use either semi-synchronous communication or synchronous communication.</span></span> <span data-ttu-id="78319-129">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="78319-129">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="78319-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="78319-130">Requirements</span></span>



| <span data-ttu-id="78319-131">需求</span><span class="sxs-lookup"><span data-stu-id="78319-131">Requirement</span></span> | <span data-ttu-id="78319-132">值</span><span class="sxs-lookup"><span data-stu-id="78319-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78319-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78319-133">Minimum supported client</span></span><br/> | <span data-ttu-id="78319-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78319-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="78319-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78319-135">Minimum supported server</span></span><br/> | <span data-ttu-id="78319-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78319-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="78319-137">標頭</span><span class="sxs-lookup"><span data-stu-id="78319-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="78319-138"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="78319-138"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="78319-139">Idl</span><span class="sxs-lookup"><span data-stu-id="78319-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="78319-140"><dt>>wbemdisp.tlb .idl</dt></span><span class="sxs-lookup"><span data-stu-id="78319-140"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="78319-141">DLL</span><span class="sxs-lookup"><span data-stu-id="78319-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78319-142"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78319-142"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="78319-143">CLSID</span><span class="sxs-lookup"><span data-stu-id="78319-143">CLSID</span></span><br/>                    | <span data-ttu-id="78319-144">CLSID \_ SWbemSink</span><span class="sxs-lookup"><span data-stu-id="78319-144">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="78319-145">IID</span><span class="sxs-lookup"><span data-stu-id="78319-145">IID</span></span><br/>                      | <span data-ttu-id="78319-146">IID \_ ISWbemSinkEvents</span><span class="sxs-lookup"><span data-stu-id="78319-146">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="78319-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78319-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78319-148">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="78319-148">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

