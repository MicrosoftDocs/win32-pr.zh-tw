---
description: 當非同步呼叫傳回進行中之呼叫的狀態時，就會觸發 SWbemSink 的 OnProgress 事件。
ms.assetid: abb43916-f952-41fe-a5ba-0428864c0685
ms.tgt_platform: multiple
title: 'ISWbemSinkEvents：： OnProgress 事件 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnProgress
- ISWbemSinkEvents.OnProgress
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0d322309adcfad33b1c303d7efd6af28db1cac80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980059"
---
# <a name="iswbemsinkeventsonprogress-event"></a><span data-ttu-id="216bf-103">ISWbemSinkEvents：： OnProgress 事件</span><span class="sxs-lookup"><span data-stu-id="216bf-103">ISWbemSinkEvents::OnProgress event</span></span>

<span data-ttu-id="216bf-104">當非同步呼叫傳回進行中之呼叫的狀態時，就會觸發 [**SWbemSink**](swbemsink.md)的 **OnProgress** 事件。</span><span class="sxs-lookup"><span data-stu-id="216bf-104">The **OnProgress** event of [**SWbemSink**](swbemsink.md) is triggered when an asynchronous call returns the status of a call that is in progress.</span></span> <span data-ttu-id="216bf-105">如果從支援狀態更新的提供者產生事件、實例或類別，您可以將程式碼放在這個事件中，為使用者提供非同步作業狀態的相關意見反應。</span><span class="sxs-lookup"><span data-stu-id="216bf-105">If the events, instances, or classes are produced from a provider that supports status updates, you can place code in this event to provide users with feedback about the status of an asynchronous operation.</span></span> <span data-ttu-id="216bf-106">如果您想要接收狀態更新，您必須將非同步呼叫的 *iFlags* 參數設定為 **wbemFlagSendStatus** (128/0x80) ，否則就不會觸發此事件。</span><span class="sxs-lookup"><span data-stu-id="216bf-106">You must set the *iFlags* parameter of the asynchronous call to **wbemFlagSendStatus** (128/0x80) if you want to receive status updates, otherwise this event is not triggered.</span></span>

<span data-ttu-id="216bf-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="216bf-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="216bf-108">語法</span><span class="sxs-lookup"><span data-stu-id="216bf-108">Syntax</span></span>


```VB
SWbemSink.OnProgress( _
  ByVal iUpperBound, _
  ByVal iCurrent, _
  ByVal strMessage, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="216bf-109">參數</span><span class="sxs-lookup"><span data-stu-id="216bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="216bf-110">*iUpperBound*</span><span class="sxs-lookup"><span data-stu-id="216bf-110">*iUpperBound*</span></span> 
</dt> <dd>

<span data-ttu-id="216bf-111">描述要完成之工作總數的整數。</span><span class="sxs-lookup"><span data-stu-id="216bf-111">Integer that describes the total number of tasks to complete.</span></span>

</dd> <dt>

<span data-ttu-id="216bf-112">*iCurrent*</span><span class="sxs-lookup"><span data-stu-id="216bf-112">*iCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="216bf-113">目前正在處理的專案。</span><span class="sxs-lookup"><span data-stu-id="216bf-113">Current item that is being processed.</span></span>

</dd> <dt>

<span data-ttu-id="216bf-114">*strMessage*</span><span class="sxs-lookup"><span data-stu-id="216bf-114">*strMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="216bf-115">描述目前工作狀態的訊息。</span><span class="sxs-lookup"><span data-stu-id="216bf-115">Message that describes the status of the current task.</span></span>

</dd> <dt>

<span data-ttu-id="216bf-116">*objWbemAsyncCoNtext*</span><span class="sxs-lookup"><span data-stu-id="216bf-116">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="216bf-117">傳遞至原始非同步呼叫的 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="216bf-117">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="216bf-118">使用這個參數來識別非同步呼叫的來源，此呼叫會在使用這個物件接收進行多個非同步呼叫時觸發這個事件。</span><span class="sxs-lookup"><span data-stu-id="216bf-118">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="216bf-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="216bf-119">Return value</span></span>

<span data-ttu-id="216bf-120">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="216bf-120">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="216bf-121">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="216bf-121">Error codes</span></span>

<span data-ttu-id="216bf-122">**OnProgress** 事件完成之後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="216bf-122">After the completion of the **OnProgress** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="216bf-123">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="216bf-123">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="216bf-124">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="216bf-124">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="216bf-125">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="216bf-125">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="216bf-126">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="216bf-126">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="216bf-127">**wbemErrTransportFailure** -2147749909 (0x80041015) </span><span class="sxs-lookup"><span data-stu-id="216bf-127">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="216bf-128">發生網路錯誤，導致無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="216bf-128">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="216bf-129">備註</span><span class="sxs-lookup"><span data-stu-id="216bf-129">Remarks</span></span>

<span data-ttu-id="216bf-130">當非同步呼叫傳回正在進行之呼叫的狀態時，就會觸發 **OnProgress** 事件。</span><span class="sxs-lookup"><span data-stu-id="216bf-130">The **OnProgress** event is triggered when an asynchronous call returns the status of a call that is in progress.</span></span> <span data-ttu-id="216bf-131">如果從支援狀態更新的提供者產生事件、實例或類別，您可以將程式碼放在這個事件中，以提供使用者有關非同步作業狀態的意見反應。</span><span class="sxs-lookup"><span data-stu-id="216bf-131">If the events, instances, or classes are produced from a provider that supports status updates, you can place code in this event to give users feedback about the status of an asynchronous operation.</span></span>

> [!Note]  
> <span data-ttu-id="216bf-132">非同步回呼可讓未經驗證的使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="216bf-132">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="216bf-133">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="216bf-133">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="216bf-134">若要消除風險，請使用半同步或同步通訊。</span><span class="sxs-lookup"><span data-stu-id="216bf-134">To eliminate the risks, use semi-synchronous or synchronous communication.</span></span> <span data-ttu-id="216bf-135">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="216bf-135">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="216bf-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="216bf-136">Requirements</span></span>



| <span data-ttu-id="216bf-137">需求</span><span class="sxs-lookup"><span data-stu-id="216bf-137">Requirement</span></span> | <span data-ttu-id="216bf-138">值</span><span class="sxs-lookup"><span data-stu-id="216bf-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="216bf-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="216bf-139">Minimum supported client</span></span><br/> | <span data-ttu-id="216bf-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="216bf-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="216bf-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="216bf-141">Minimum supported server</span></span><br/> | <span data-ttu-id="216bf-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="216bf-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="216bf-143">標頭</span><span class="sxs-lookup"><span data-stu-id="216bf-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="216bf-144"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="216bf-144"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="216bf-145">Idl</span><span class="sxs-lookup"><span data-stu-id="216bf-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="216bf-146"><dt>>wbemdisp.tlb .idl</dt></span><span class="sxs-lookup"><span data-stu-id="216bf-146"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="216bf-147">DLL</span><span class="sxs-lookup"><span data-stu-id="216bf-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="216bf-148"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="216bf-148"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="216bf-149">CLSID</span><span class="sxs-lookup"><span data-stu-id="216bf-149">CLSID</span></span><br/>                    | <span data-ttu-id="216bf-150">CLSID \_ SWbemSink</span><span class="sxs-lookup"><span data-stu-id="216bf-150">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="216bf-151">IID</span><span class="sxs-lookup"><span data-stu-id="216bf-151">IID</span></span><br/>                      | <span data-ttu-id="216bf-152">IID \_ ISWbemSinkEvents</span><span class="sxs-lookup"><span data-stu-id="216bf-152">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="216bf-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="216bf-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="216bf-154">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="216bf-154">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

