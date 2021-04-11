---
description: SWbemSink 物件的 Cancel 方法會取消與這個物件接收相關聯的所有未完成非同步作業。
ms.assetid: dbe1eb24-5d9d-407a-b7c6-c58ec6891d7a
ms.tgt_platform: multiple
title: 'ISWbemSink：： Cancel 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.Cancel
- ISWbemSink.Cancel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 37bb44e8c34aa3cd7f9d491656461097e5a2bb5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195225"
---
# <a name="iswbemsinkcancel-method"></a><span data-ttu-id="d4cae-103">ISWbemSink：： Cancel 方法</span><span class="sxs-lookup"><span data-stu-id="d4cae-103">ISWbemSink::Cancel method</span></span>

<span data-ttu-id="d4cae-104">[**SWbemSink**](swbemsink.md)物件的 **Cancel** 方法會取消與這個物件接收相關聯的所有未完成非同步作業。</span><span class="sxs-lookup"><span data-stu-id="d4cae-104">The **Cancel** method of the [**SWbemSink**](swbemsink.md) object cancels all outstanding asynchronous operations that are associated with this object sink.</span></span>

<span data-ttu-id="d4cae-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="d4cae-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d4cae-106">語法</span><span class="sxs-lookup"><span data-stu-id="d4cae-106">Syntax</span></span>


```VB
SWbemSink.Cancel()
```



## <a name="parameters"></a><span data-ttu-id="d4cae-107">參數</span><span class="sxs-lookup"><span data-stu-id="d4cae-107">Parameters</span></span>

<span data-ttu-id="d4cae-108">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d4cae-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d4cae-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4cae-109">Return value</span></span>

<span data-ttu-id="d4cae-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d4cae-110">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d4cae-111">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d4cae-111">Error codes</span></span>

<span data-ttu-id="d4cae-112">完成 **取消** 方法之後， [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件可能會包含下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d4cae-112">After the completion of the **Cancel** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="d4cae-113">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="d4cae-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d4cae-114">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d4cae-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="d4cae-115">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="d4cae-115">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d4cae-116">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="d4cae-116">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d4cae-117">**wbemErrTransportFailure** -2147749909 (0x80041015) </span><span class="sxs-lookup"><span data-stu-id="d4cae-117">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="d4cae-118">發生網路錯誤，導致無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="d4cae-118">Networking error occurred, preventing normal operation.</span></span>

</dd> <dt>

<span data-ttu-id="d4cae-119">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="d4cae-119">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="d4cae-120">目前或指定的使用者名稱和密碼無效或已獲授權，無法進行連接。</span><span class="sxs-lookup"><span data-stu-id="d4cae-120">Current or specified user name and password are not valid or authorized to make the connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4cae-121">備註</span><span class="sxs-lookup"><span data-stu-id="d4cae-121">Remarks</span></span>

<span data-ttu-id="d4cae-122">您無法只取消一個非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="d4cae-122">You cannot cancel only one asynchronous call.</span></span> <span data-ttu-id="d4cae-123">如果有多個非同步呼叫暫止，而使用這個物件接收，則此方法會使用這個物件接收來取消所有的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="d4cae-123">If multiple asynchronous calls are pending that use this object sink, then this method cancels all the asynchronous calls using this object sink.</span></span> <span data-ttu-id="d4cae-124">與其他物件接收器相關聯的非同步呼叫會繼續受到影響。</span><span class="sxs-lookup"><span data-stu-id="d4cae-124">Asynchronous calls that are associated with other object sinks continue unaffected.</span></span>

<span data-ttu-id="d4cae-125">您無法將此接收指派給 **任何** 專案，以取消非同步作業。</span><span class="sxs-lookup"><span data-stu-id="d4cae-125">You cannot assign this sink to **Nothing** to cancel an asynchronous operation.</span></span> <span data-ttu-id="d4cae-126">您必須呼叫 **Cancel** 方法，讓 WMI 中止作業並釋放相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="d4cae-126">You must call the **Cancel** method to make WMI discontinue the operation and free the associated resources.</span></span> <span data-ttu-id="d4cae-127">這對於冗長的非同步作業（例如查詢或永遠不會完成的作業，例如 [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)）非常重要。</span><span class="sxs-lookup"><span data-stu-id="d4cae-127">This is very important with lengthy asynchronous operations, such as queries, or operations that never complete, such as [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span></span>

> [!Note]  
> <span data-ttu-id="d4cae-128">非同步回呼可讓未經驗證的使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="d4cae-128">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="d4cae-129">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="d4cae-129">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="d4cae-130">若要消除風險，請使用最半同步或同步通訊。</span><span class="sxs-lookup"><span data-stu-id="d4cae-130">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="d4cae-131">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="d4cae-131">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="d4cae-132">下列範例說明如何取消非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="d4cae-132">The following example shows you how to cancel an asynchronous call.</span></span>


```VB
objwbemsink.Cancel()
set objwbemsink= Nothing
```



## <a name="requirements"></a><span data-ttu-id="d4cae-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4cae-133">Requirements</span></span>



| <span data-ttu-id="d4cae-134">需求</span><span class="sxs-lookup"><span data-stu-id="d4cae-134">Requirement</span></span> | <span data-ttu-id="d4cae-135">值</span><span class="sxs-lookup"><span data-stu-id="d4cae-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4cae-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4cae-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d4cae-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4cae-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d4cae-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4cae-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d4cae-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4cae-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d4cae-140">標頭</span><span class="sxs-lookup"><span data-stu-id="d4cae-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4cae-141"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="d4cae-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4cae-142">Idl</span><span class="sxs-lookup"><span data-stu-id="d4cae-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d4cae-143"><dt>>wbemdisp.tlb .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d4cae-143"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="d4cae-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d4cae-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4cae-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4cae-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d4cae-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="d4cae-146">CLSID</span></span><br/>                    | <span data-ttu-id="d4cae-147">CLSID \_ SWbemSink</span><span class="sxs-lookup"><span data-stu-id="d4cae-147">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="d4cae-148">IID</span><span class="sxs-lookup"><span data-stu-id="d4cae-148">IID</span></span><br/>                      | <span data-ttu-id="d4cae-149">IID \_ ISWbemSink</span><span class="sxs-lookup"><span data-stu-id="d4cae-149">IID\_ISWbemSink</span></span><br/>                                                              |



## <a name="see-also"></a><span data-ttu-id="d4cae-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4cae-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4cae-151">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="d4cae-151">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

