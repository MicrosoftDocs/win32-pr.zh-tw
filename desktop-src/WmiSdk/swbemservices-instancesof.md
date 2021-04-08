---
description: 根據使用者指定的選取準則，建立傳回指定類別之實例的列舉值。
ms.assetid: 6465a981-f98e-4ece-a9b6-9da8ae618bc6
ms.tgt_platform: multiple
title: 'SWbemServices. InstancesOf 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.InstancesOf
- ISWbemServices.InstancesOf
- ISWbemServices.InstancesOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e2386b52160b1e2a08c5a345b67922ed24afc44c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852455"
---
# <a name="swbemservicesinstancesof-method"></a><span data-ttu-id="963c9-103">SWbemServices. InstancesOf 方法</span><span class="sxs-lookup"><span data-stu-id="963c9-103">SWbemServices.InstancesOf method</span></span>

<span data-ttu-id="963c9-104">[**SWbemServices**](swbemservices.md)物件的 **InstancesOf** 方法會根據使用者指定的選取準則，建立傳回指定類別之實例的列舉值。</span><span class="sxs-lookup"><span data-stu-id="963c9-104">The **InstancesOf** method of the [**SWbemServices**](swbemservices.md) object creates an enumerator that returns the instances of a specified class according to the user-specified selection criteria.</span></span> <span data-ttu-id="963c9-105">這個方法會執行簡單的查詢。</span><span class="sxs-lookup"><span data-stu-id="963c9-105">This method implements a simple query.</span></span> <span data-ttu-id="963c9-106">更複雜的查詢可能需要使用 [**SWbemServices.ExecQuery**](swbemservices-execquery.md)。</span><span class="sxs-lookup"><span data-stu-id="963c9-106">More complex queries may require the use of [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="963c9-107">方法會在半同步模式中呼叫。</span><span class="sxs-lookup"><span data-stu-id="963c9-107">The method is called in the semisynchronous mode.</span></span> <span data-ttu-id="963c9-108">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="963c9-108">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="963c9-109">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="963c9-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="963c9-110">語法</span><span class="sxs-lookup"><span data-stu-id="963c9-110">Syntax</span></span>


```VB
objWbemObjectSet = .InstancesOf( _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="963c9-111">參數</span><span class="sxs-lookup"><span data-stu-id="963c9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="963c9-112">*strClass*</span><span class="sxs-lookup"><span data-stu-id="963c9-112">*strClass*</span></span> 
</dt> <dd>

<span data-ttu-id="963c9-113">必要。</span><span class="sxs-lookup"><span data-stu-id="963c9-113">Required.</span></span> <span data-ttu-id="963c9-114">包含需要實例之類別名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="963c9-114">String that contains the name of the class for which instances are desired.</span></span> <span data-ttu-id="963c9-115">此參數不可以是空白。</span><span class="sxs-lookup"><span data-stu-id="963c9-115">This parameter cannot be blank.</span></span>

</dd> <dt>

<span data-ttu-id="963c9-116">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="963c9-116">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="963c9-117">此參數會決定呼叫列舉的詳細資訊，以及此呼叫是否立即傳回。</span><span class="sxs-lookup"><span data-stu-id="963c9-117">This parameter determines how detailed the call enumerates and if this call returns immediately.</span></span> <span data-ttu-id="963c9-118">此參數的預設值為 **wbemFlagReturnImmediately**。</span><span class="sxs-lookup"><span data-stu-id="963c9-118">The default value for this parameter is **wbemFlagReturnImmediately**.</span></span> <span data-ttu-id="963c9-119">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="963c9-119">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="963c9-120"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* (32 (0x20) ) </span><span class="sxs-lookup"><span data-stu-id="963c9-120"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="963c9-121">使順向列舉值傳回。</span><span class="sxs-lookup"><span data-stu-id="963c9-121">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="963c9-122">順向列舉值的速度通常會比傳統列舉值更快，且使用的記憶體較少，但不允許呼叫 [**SWbemObject。 \_**](swbemobject-clone-.md)</span><span class="sxs-lookup"><span data-stu-id="963c9-122">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="963c9-123"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="963c9-123"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="963c9-124">讓 WMI 保留列舉物件的指標，直到用戶端釋放列舉值為止。</span><span class="sxs-lookup"><span data-stu-id="963c9-124">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="963c9-125"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* (16 (0x10) ) </span><span class="sxs-lookup"><span data-stu-id="963c9-125"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="963c9-126">此參數的預設值。</span><span class="sxs-lookup"><span data-stu-id="963c9-126">Default value for this parameter.</span></span> <span data-ttu-id="963c9-127">此旗標會立即傳回呼叫。</span><span class="sxs-lookup"><span data-stu-id="963c9-127">This flag causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="963c9-128"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="963c9-128"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="963c9-129">導致此呼叫封鎖，直到查詢完成為止。</span><span class="sxs-lookup"><span data-stu-id="963c9-129">Causes this call to block until the query has completed.</span></span> <span data-ttu-id="963c9-130">此旗標會在同步模式中呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="963c9-130">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="963c9-131"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="963c9-131"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="963c9-132">強制列舉只包含指定之父類別的直屬子類別。</span><span class="sxs-lookup"><span data-stu-id="963c9-132">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="963c9-133"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="963c9-133"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="963c9-134">此參數的預設值。</span><span class="sxs-lookup"><span data-stu-id="963c9-134">Default value for this parameter.</span></span> <span data-ttu-id="963c9-135">此值會強制列舉包含階層中的所有類別。</span><span class="sxs-lookup"><span data-stu-id="963c9-135">This value forces the enumeration to include all classes in the hierarchy.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="963c9-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="963c9-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="963c9-137">讓 WMI 以基類定義傳回類別修訂資料。</span><span class="sxs-lookup"><span data-stu-id="963c9-137">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="963c9-138">如需詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="963c9-138">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="963c9-139">*objWbemNamedValueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="963c9-139">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="963c9-140">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="963c9-140">Typically, this is undefined.</span></span> <span data-ttu-id="963c9-141">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="963c9-141">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="963c9-142">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="963c9-142">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="963c9-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="963c9-143">Return value</span></span>

<span data-ttu-id="963c9-144">如果成功，方法會傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md)。</span><span class="sxs-lookup"><span data-stu-id="963c9-144">If successful, the method returns an [**SWbemObjectSet**](swbemobjectset.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="963c9-145">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="963c9-145">Error codes</span></span>

<span data-ttu-id="963c9-146">**InstancesOf** 方法完成後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="963c9-146">Upon the completion of the **InstancesOf** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="963c9-147">傳回的列舉值包含零個元素不是錯誤。</span><span class="sxs-lookup"><span data-stu-id="963c9-147">A returned enumerator with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="963c9-148">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="963c9-148">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="963c9-149">目前的使用者沒有許可權可查看指定之類別的實例。</span><span class="sxs-lookup"><span data-stu-id="963c9-149">Current user does not have the permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="963c9-150">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="963c9-150">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="963c9-151">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="963c9-151">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="963c9-152">**wbemErrInvalidClass** -2147749904 (0x80041010) </span><span class="sxs-lookup"><span data-stu-id="963c9-152">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="963c9-153">指定的類別無效。</span><span class="sxs-lookup"><span data-stu-id="963c9-153">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="963c9-154">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="963c9-154">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="963c9-155">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="963c9-155">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="963c9-156">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="963c9-156">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="963c9-157">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="963c9-157">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="963c9-158">備註</span><span class="sxs-lookup"><span data-stu-id="963c9-158">Remarks</span></span>

<span data-ttu-id="963c9-159">**InstancesOf** 方法只適用于類別物件。</span><span class="sxs-lookup"><span data-stu-id="963c9-159">The **InstancesOf** method only works for class objects.</span></span>

<span data-ttu-id="963c9-160">根據預設，InstancesOf 會執行深度抓取。</span><span class="sxs-lookup"><span data-stu-id="963c9-160">By default, InstancesOf performs a deep retrieval.</span></span> <span data-ttu-id="963c9-161">也就是說，InstancesOf 會抓取您識別的 managed 資源的所有實例，以及目標類別下定義之所有子類別的所有實例。</span><span class="sxs-lookup"><span data-stu-id="963c9-161">That is, InstancesOf retrieves all instances of the managed resource you identify and all instances of all the subclasses defined beneath the target class.</span></span> <span data-ttu-id="963c9-162">例如，下列腳本會抓取 CIM 服務抽象類別下定義的所有動態類別所模型化的所有資源 \_ 。</span><span class="sxs-lookup"><span data-stu-id="963c9-162">For example, the following script retrieves all of the resources modeled by all of the dynamic classes defined beneath the CIM\_Service abstract class.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("CIM_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Object Path: " & objSWbemObject.Path_.Path
Next
```



<span data-ttu-id="963c9-163">如果您執行此腳本，就會取回信息。</span><span class="sxs-lookup"><span data-stu-id="963c9-163">If you run this script, you will get information back.</span></span> <span data-ttu-id="963c9-164">不過，這種資訊不會限制在電腦上所安裝的服務。</span><span class="sxs-lookup"><span data-stu-id="963c9-164">However, this information will not be limited to the services installed on a computer.</span></span> <span data-ttu-id="963c9-165">相反地，它會包含 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)的所有子類別的資訊，包括 [**win32 \_ >systemdriver**](/windows/desktop/CIMWin32Prov/win32-systemdriver) 和 [**win32 \_ ApplicationService**](/previous-versions/windows/desktop/legacy/aa394068(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="963c9-165">Instead, it will include information from all child classes of [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), including [**Win32\_SystemDriver**](/windows/desktop/CIMWin32Prov/win32-systemdriver) and [**Win32\_ApplicationService**](/previous-versions/windows/desktop/legacy/aa394068(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="963c9-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="963c9-166">Requirements</span></span>



| <span data-ttu-id="963c9-167">需求</span><span class="sxs-lookup"><span data-stu-id="963c9-167">Requirement</span></span> | <span data-ttu-id="963c9-168">值</span><span class="sxs-lookup"><span data-stu-id="963c9-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="963c9-169">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="963c9-169">Minimum supported client</span></span><br/> | <span data-ttu-id="963c9-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="963c9-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="963c9-171">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="963c9-171">Minimum supported server</span></span><br/> | <span data-ttu-id="963c9-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="963c9-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="963c9-173">標頭</span><span class="sxs-lookup"><span data-stu-id="963c9-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="963c9-174"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="963c9-174"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="963c9-175">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="963c9-175">Type library</span></span><br/>             | <dl> <span data-ttu-id="963c9-176"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="963c9-176"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="963c9-177">DLL</span><span class="sxs-lookup"><span data-stu-id="963c9-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="963c9-178"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="963c9-178"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="963c9-179">CLSID</span><span class="sxs-lookup"><span data-stu-id="963c9-179">CLSID</span></span><br/>                    | <span data-ttu-id="963c9-180">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="963c9-180">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="963c9-181">IID</span><span class="sxs-lookup"><span data-stu-id="963c9-181">IID</span></span><br/>                      | <span data-ttu-id="963c9-182">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="963c9-182">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="963c9-183">另請參閱</span><span class="sxs-lookup"><span data-stu-id="963c9-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="963c9-184">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="963c9-184">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="963c9-185">**Swbemobjectset 搭配使用**</span><span class="sxs-lookup"><span data-stu-id="963c9-185">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

