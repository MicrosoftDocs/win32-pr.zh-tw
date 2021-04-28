---
description: SWbemServices.ExecQuery 方法-執行查詢來取出物件。
ms.assetid: 06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f
ms.tgt_platform: multiple
title: " (>wbemdisp.tlb 的 SWbemServices.ExecQuery 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQuery
- ISWbemServices.ExecQuery
- ISWbemServices.ExecQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3009d2dc88e9987a3559da91eed1aa5aa1b248f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098329"
---
# <a name="swbemservicesexecquery-method"></a><span data-ttu-id="2350a-103">SWbemServices.ExecQuery 方法</span><span class="sxs-lookup"><span data-stu-id="2350a-103">SWbemServices.ExecQuery method</span></span>

<span data-ttu-id="2350a-104">[**SWbemServices**](swbemservices.md)物件的 **ExecQuery** 方法會執行查詢來取出物件。</span><span class="sxs-lookup"><span data-stu-id="2350a-104">The **ExecQuery** method of the [**SWbemServices**](swbemservices.md) object executes a query to retrieve objects.</span></span> <span data-ttu-id="2350a-105">您可以透過傳回的 [**swbemobjectset 搭配使用**](swbemobjectset.md) 集合取得這些物件。</span><span class="sxs-lookup"><span data-stu-id="2350a-105">These objects are available through the returned [**SWbemObjectSet**](swbemobjectset.md) collection.</span></span>

<span data-ttu-id="2350a-106">這個方法會在半同步模式中呼叫。</span><span class="sxs-lookup"><span data-stu-id="2350a-106">This method is called in the semisynchronous mode.</span></span> <span data-ttu-id="2350a-107">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="2350a-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="2350a-108">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="2350a-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2350a-109">語法</span><span class="sxs-lookup"><span data-stu-id="2350a-109">Syntax</span></span>


```VB
objWbemObjectSet = .ExecQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="2350a-110">參數</span><span class="sxs-lookup"><span data-stu-id="2350a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2350a-111">*strQuery*</span><span class="sxs-lookup"><span data-stu-id="2350a-111">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="2350a-112">必要。</span><span class="sxs-lookup"><span data-stu-id="2350a-112">Required.</span></span> <span data-ttu-id="2350a-113">包含查詢文字的字串。</span><span class="sxs-lookup"><span data-stu-id="2350a-113">String that contains the text of the query.</span></span> <span data-ttu-id="2350a-114">此參數不可以是空白。</span><span class="sxs-lookup"><span data-stu-id="2350a-114">This parameter cannot be blank.</span></span> <span data-ttu-id="2350a-115">如需建立 WMI 查詢字串的詳細資訊，請參閱 [使用 Wql 查詢](querying-with-wql.md) 和 [wql](wql-sql-for-wmi.md) 參考。</span><span class="sxs-lookup"><span data-stu-id="2350a-115">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="2350a-116">*strQueryLanguage* \[選\]</span><span class="sxs-lookup"><span data-stu-id="2350a-116">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2350a-117">字串，包含要使用的查詢語言。</span><span class="sxs-lookup"><span data-stu-id="2350a-117">String that contains the query language to be used.</span></span> <span data-ttu-id="2350a-118">如果有指定，此值必須是 "WQL"。</span><span class="sxs-lookup"><span data-stu-id="2350a-118">If specified, this value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="2350a-119">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="2350a-119">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2350a-120">判斷查詢行為的整數，並判斷此呼叫是否立即傳回。</span><span class="sxs-lookup"><span data-stu-id="2350a-120">Integer that determines the behavior of the query and determines whether this call returns immediately.</span></span> <span data-ttu-id="2350a-121">此參數的預設值為 **wbemFlagReturnImmediately**。</span><span class="sxs-lookup"><span data-stu-id="2350a-121">The default value for this parameter is **wbemFlagReturnImmediately**.</span></span> <span data-ttu-id="2350a-122">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="2350a-122">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="2350a-123"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* (32 (0x20) ) </span><span class="sxs-lookup"><span data-stu-id="2350a-123"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="2350a-124">使順向列舉值傳回。</span><span class="sxs-lookup"><span data-stu-id="2350a-124">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="2350a-125">順向列舉值的速度通常會比傳統列舉值更快，且使用的記憶體較少，但不允許呼叫 [**SWbemObject。 \_**](swbemobject-clone-.md)</span><span class="sxs-lookup"><span data-stu-id="2350a-125">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="2350a-126"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="2350a-126"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="2350a-127">讓 WMI 保留列舉物件的指標，直到用戶端釋放列舉值為止。</span><span class="sxs-lookup"><span data-stu-id="2350a-127">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="2350a-128"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* (16 (0x10) ) </span><span class="sxs-lookup"><span data-stu-id="2350a-128"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="2350a-129">導致呼叫立即返回。</span><span class="sxs-lookup"><span data-stu-id="2350a-129">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="2350a-130"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="2350a-130"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="2350a-131">導致此呼叫封鎖，直到查詢完成為止。</span><span class="sxs-lookup"><span data-stu-id="2350a-131">Causes this call to block until the query is complete.</span></span> <span data-ttu-id="2350a-132">此旗標會在同步模式中呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="2350a-132">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span data-ttu-id="2350a-133"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemQueryFlagPrototype \* \* \* (2 (0x2) ) </span><span class="sxs-lookup"><span data-stu-id="2350a-133"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>\*\*\*\*wbemQueryFlagPrototype\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="2350a-134">用於原型設計。</span><span class="sxs-lookup"><span data-stu-id="2350a-134">Used for prototyping.</span></span> <span data-ttu-id="2350a-135">此旗標會停止進行查詢，並傳回看起來像一般結果物件的物件。</span><span class="sxs-lookup"><span data-stu-id="2350a-135">This flag stops the query from happening and returns an object that looks like a typical result object.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="2350a-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="2350a-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="2350a-137">讓 WMI 以基類定義傳回類別修訂資料。</span><span class="sxs-lookup"><span data-stu-id="2350a-137">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="2350a-138">如需詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="2350a-138">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2350a-139">*objWbemNamedValueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="2350a-139">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2350a-140">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="2350a-140">Typically, this is undefined.</span></span> <span data-ttu-id="2350a-141">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="2350a-141">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="2350a-142">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="2350a-142">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2350a-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="2350a-143">Return value</span></span>

<span data-ttu-id="2350a-144">如果沒有發生錯誤，這個方法會傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="2350a-144">If no error occurs, this method returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span> <span data-ttu-id="2350a-145">這是包含查詢結果集的物件集合。</span><span class="sxs-lookup"><span data-stu-id="2350a-145">This is an object collection that contains the result set of the query.</span></span> <span data-ttu-id="2350a-146">呼叫端可以使用您所使用之程式設計語言的集合執行來檢查集合。</span><span class="sxs-lookup"><span data-stu-id="2350a-146">The caller can examine the collection using the implementation of collections for the programming language you are using.</span></span> <span data-ttu-id="2350a-147">如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。</span><span class="sxs-lookup"><span data-stu-id="2350a-147">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="2350a-148">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="2350a-148">Error codes</span></span>

<span data-ttu-id="2350a-149">**ExecQuery** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可以包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2350a-149">After the completion of the **ExecQuery** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object can contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="2350a-150">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="2350a-150">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="2350a-151">目前的使用者沒有許可權可查看結果集。</span><span class="sxs-lookup"><span data-stu-id="2350a-151">Current user does not have the permission to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="2350a-152">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="2350a-152">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="2350a-153">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2350a-153">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="2350a-154">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="2350a-154">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="2350a-155">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="2350a-155">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="2350a-156">**wbemErrInvalidQuery** -2147749911 (0x80041017) </span><span class="sxs-lookup"><span data-stu-id="2350a-156">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="2350a-157">查詢語法無效。</span><span class="sxs-lookup"><span data-stu-id="2350a-157">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2350a-158">**wbemErrInvalidQueryType** -2147749912 (0x80041018) </span><span class="sxs-lookup"><span data-stu-id="2350a-158">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="2350a-159">不支援要求的查詢語言。</span><span class="sxs-lookup"><span data-stu-id="2350a-159">Requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="2350a-160">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="2350a-160">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="2350a-161">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="2350a-161">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2350a-162">備註</span><span class="sxs-lookup"><span data-stu-id="2350a-162">Remarks</span></span>

<span data-ttu-id="2350a-163">**ExecQuery** 是抓取 WMI 資訊最常使用的其中一項呼叫。</span><span class="sxs-lookup"><span data-stu-id="2350a-163">**ExecQuery** is one of the most commonly-used calls to retrieve WMI information.</span></span> <span data-ttu-id="2350a-164">**ExecQuery** 的標準呼叫看起來如下所示：</span><span class="sxs-lookup"><span data-stu-id="2350a-164">A standard call to **ExecQuery** looks like the following:</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```



<span data-ttu-id="2350a-165">請注意，您會使用表示適當命名空間和安全性的標記來建立 [**SWbemServices**](swbemservices.md) 物件，然後透過服務進行 **ExecQuery** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="2350a-165">Note that you create the [**SWbemServices**](swbemservices.md) object with a moniker that represents the appropriate namespace and security, then make the **ExecQuery** call through the service.</span></span> <span data-ttu-id="2350a-166">如需更完整的討論，請參閱 [建立 Wmi 腳本](creating-a-wmi-script.md) 和 [列舉 wmi](enumerating-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="2350a-166">For a more complete discussion, see [Creating a WMI Script](creating-a-wmi-script.md) and [Enumerating WMI](enumerating-wmi.md).</span></span>

<span data-ttu-id="2350a-167">如同 [**InstancesOf**](swbemservices-instancesof.md) 方法， **ExecQuery** 方法一律會傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="2350a-167">Like the [**InstancesOf**](swbemservices-instancesof.md) method, the **ExecQuery** method always returns an [**SWbemObjectSet**](swbemobjectset.md) collection.</span></span> <span data-ttu-id="2350a-168">因此，您的 WMI 腳本必須列舉集合 ExecQuery 傳回，才能存取集合中的每個受控資源實例，如下所示：</span><span class="sxs-lookup"><span data-stu-id="2350a-168">Thus your WMI script must enumerate the collection ExecQuery returns in order to access each managed resource instance in the collection, as shown here:</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
   ("SELECT * FROM Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



<span data-ttu-id="2350a-169">傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md)的其他 [**SWbemServices**](swbemservices.md)方法包括 [**AssociatorsOf**](swbemservices-associatorsof.md)、 [**ReferencesTo**](swbemservices-referencesto.md)和 [**SubclassesOf**](swbemservices-subclassesof.md)。</span><span class="sxs-lookup"><span data-stu-id="2350a-169">Other [**SWbemServices**](swbemservices.md) methods that return an [**SWbemObjectSet**](swbemobjectset.md) include [**AssociatorsOf**](swbemservices-associatorsof.md), [**ReferencesTo**](swbemservices-referencesto.md), and [**SubclassesOf**](swbemservices-subclassesof.md).</span></span>

<span data-ttu-id="2350a-170">查詢傳回空的結果集並不會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="2350a-170">It is not an error for the query to return an empty result set.</span></span> <span data-ttu-id="2350a-171">**ExecQuery** 方法會傳回索引鍵屬性，不論是否在 *strQuery* 引數中要求索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="2350a-171">The **ExecQuery** method returns key properties whether or not the key property is requested in the *strQuery* argument.</span></span> <span data-ttu-id="2350a-172">如果執行此方法時發生錯誤，而且您未使用 **wbemFlagReturnImmediately** 旗標，則在您嘗試存取傳回的物件集之前，不會設定 [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件。</span><span class="sxs-lookup"><span data-stu-id="2350a-172">If an error occurs when executing this method and you do not use the **wbemFlagReturnImmediately** flag, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object is not set until you attempt to access the returned object set.</span></span> <span data-ttu-id="2350a-173">但是，如果您使用 **wbemFlagReturnWhenComplete** 旗標，則會在呼叫 **ExecQuery** 方法時設定 Err 物件。</span><span class="sxs-lookup"><span data-stu-id="2350a-173">However, if you use the **wbemFlagReturnWhenComplete** flag, the Err object is set when the **ExecQuery** method is called.</span></span>

<span data-ttu-id="2350a-174">WQL 查詢中可使用的 **和** 和 **或** 關鍵字數目有一些限制。</span><span class="sxs-lookup"><span data-stu-id="2350a-174">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="2350a-175">複雜查詢中使用的大量 WQL 關鍵字可能會導致 WMI 將 **WBEM \_ E \_ 配額 \_ 違規** 錯誤碼傳回為 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="2350a-175">Large numbers of WQL keywords that are used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="2350a-176">WQL 關鍵字的限制取決於查詢的複雜程度。</span><span class="sxs-lookup"><span data-stu-id="2350a-176">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="examples"></a><span data-ttu-id="2350a-177">範例</span><span class="sxs-lookup"><span data-stu-id="2350a-177">Examples</span></span>

<span data-ttu-id="2350a-178">下列 VBScript 程式碼範例會尋找本機電腦上的所有磁片磁碟機，並顯示裝置識別碼和磁片磁碟機的類型。</span><span class="sxs-lookup"><span data-stu-id="2350a-178">The following VBScript code example locates all the disk drives on the local computer and displays the device ID and the type of the disk drive.</span></span>


```VB
Set colDisks = GetObject( _
    "Winmgmts:").ExecQuery("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
 
    Select Case objDisk.DriveType
        Case 1
            Wscript.Echo "No root directory. Drive type could not be determined."
        Case 2
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Removable drive" 
        Case 3
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Local hard disk" 
        Case 4
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Network disk" 
        Case 5
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Compact disk" 
        Case 6
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = RAM disk" 
        Case Else
            Wscript.Echo "Drive type could not be determined."
    End Select
Next
```



## <a name="requirements"></a><span data-ttu-id="2350a-179">規格需求</span><span class="sxs-lookup"><span data-stu-id="2350a-179">Requirements</span></span>



| <span data-ttu-id="2350a-180">需求</span><span class="sxs-lookup"><span data-stu-id="2350a-180">Requirement</span></span> | <span data-ttu-id="2350a-181">值</span><span class="sxs-lookup"><span data-stu-id="2350a-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2350a-182">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2350a-182">Minimum supported client</span></span><br/> | <span data-ttu-id="2350a-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2350a-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2350a-184">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2350a-184">Minimum supported server</span></span><br/> | <span data-ttu-id="2350a-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2350a-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2350a-186">標頭</span><span class="sxs-lookup"><span data-stu-id="2350a-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="2350a-187"><dt>>Wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="2350a-187"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2350a-188">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2350a-188">Type library</span></span><br/>             | <dl> <span data-ttu-id="2350a-189"><dt>>Wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2350a-189"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2350a-190">DLL</span><span class="sxs-lookup"><span data-stu-id="2350a-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2350a-191"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2350a-191"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2350a-192">CLSID</span><span class="sxs-lookup"><span data-stu-id="2350a-192">CLSID</span></span><br/>                    | <span data-ttu-id="2350a-193">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="2350a-193">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="2350a-194">IID</span><span class="sxs-lookup"><span data-stu-id="2350a-194">IID</span></span><br/>                      | <span data-ttu-id="2350a-195">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="2350a-195">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="2350a-196">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2350a-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2350a-197">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="2350a-197">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="2350a-198">**SWbemServices。 Get**</span><span class="sxs-lookup"><span data-stu-id="2350a-198">**SWbemServices.Get**</span></span>](swbemservices-get.md)
</dt> <dt>

[<span data-ttu-id="2350a-199">使用 WQL 查詢</span><span class="sxs-lookup"><span data-stu-id="2350a-199">Querying with WQL</span></span>](querying-with-wql.md)
</dt> <dt>

[<span data-ttu-id="2350a-200">建立 WMI 腳本</span><span class="sxs-lookup"><span data-stu-id="2350a-200">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
</dt> <dt>

[<span data-ttu-id="2350a-201">列舉 WMI</span><span class="sxs-lookup"><span data-stu-id="2350a-201">Enumerating WMI</span></span>](enumerating-wmi.md)
</dt> </dl>

 

