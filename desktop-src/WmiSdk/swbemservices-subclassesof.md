---
description: 傳回 Swbemobjectset 搭配使用物件。
ms.assetid: cfe08956-7215-4e2e-a279-6e86f14e5c27
ms.tgt_platform: multiple
title: 'SWbemServices. SubclassesOf 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.SubclassesOf
- ISWbemServices.SubclassesOf
- ISWbemServices.SubclassesOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e8c23dee5ee3f0a1cf5babe37d0ccb6aa0a3ac7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992016"
---
# <a name="swbemservicessubclassesof-method"></a><span data-ttu-id="f26cf-103">SWbemServices. SubclassesOf 方法</span><span class="sxs-lookup"><span data-stu-id="f26cf-103">SWbemServices.SubclassesOf method</span></span>

<span data-ttu-id="f26cf-104">[**SWbemServices**](swbemservices.md)物件的 **SubclassesOf** 方法會傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md)物件。</span><span class="sxs-lookup"><span data-stu-id="f26cf-104">The **SubclassesOf** method of the [**SWbemServices**](swbemservices.md) object returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span> <span data-ttu-id="f26cf-105">此物件是指定類別的子類別集合。</span><span class="sxs-lookup"><span data-stu-id="f26cf-105">This object is a collection of subclasses of a specified class.</span></span> <span data-ttu-id="f26cf-106">傳回之集合中的專案可以使用標準的收集方法來取得。</span><span class="sxs-lookup"><span data-stu-id="f26cf-106">Items in the returned collection can be obtained using standard collection methods.</span></span> <span data-ttu-id="f26cf-107">如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。</span><span class="sxs-lookup"><span data-stu-id="f26cf-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="f26cf-108">這個方法僅適用于類別物件。</span><span class="sxs-lookup"><span data-stu-id="f26cf-108">This method only works for class objects.</span></span>

<span data-ttu-id="f26cf-109">方法會在半同步模式中呼叫。</span><span class="sxs-lookup"><span data-stu-id="f26cf-109">The method is called in the semisynchronous mode.</span></span> <span data-ttu-id="f26cf-110">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="f26cf-110">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="f26cf-111">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="f26cf-111">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f26cf-112">語法</span><span class="sxs-lookup"><span data-stu-id="f26cf-112">Syntax</span></span>


```VB
objWbemObjectSet = .SubclassesOf( _
  [ ByVal strSuperclass ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f26cf-113">參數</span><span class="sxs-lookup"><span data-stu-id="f26cf-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f26cf-114">*strSuperclass* \[選\]</span><span class="sxs-lookup"><span data-stu-id="f26cf-114">*strSuperclass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f26cf-115">指定父類別名稱。</span><span class="sxs-lookup"><span data-stu-id="f26cf-115">Specifies a parent class name.</span></span> <span data-ttu-id="f26cf-116">只有這個類別的子類別會在列舉值中傳回。</span><span class="sxs-lookup"><span data-stu-id="f26cf-116">Only subclasses of this class return in the enumerator.</span></span> <span data-ttu-id="f26cf-117">如果您將此參數保留空白，而且如果 *iFlags* 為 **wbemQueryFlagShallow**，則只會傳回最上層類別 (也就是沒有父類別的類別) 。</span><span class="sxs-lookup"><span data-stu-id="f26cf-117">If you leave this parameter blank, and if *iFlags* is **wbemQueryFlagShallow**, only the top-level classes are returned (that is, classes that have no parent class).</span></span> <span data-ttu-id="f26cf-118">如果這個參數是空白的，而且 *iFlags* 是 **wbemQueryFlagDeep** ，則會傳回命名空間內的所有類別。</span><span class="sxs-lookup"><span data-stu-id="f26cf-118">If this parameter is blank and *iFlags* is **wbemQueryFlagDeep** all classes within the namespace are returned.</span></span>

</dd> <dt>

<span data-ttu-id="f26cf-119">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="f26cf-119">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f26cf-120">決定呼叫列舉的詳細程度。</span><span class="sxs-lookup"><span data-stu-id="f26cf-120">Determines how detailed the call enumerates.</span></span> <span data-ttu-id="f26cf-121">此參數的預設值為 **wbemFlagReturnImmediately** 和 **wbemQueryFlagDeep**。</span><span class="sxs-lookup"><span data-stu-id="f26cf-121">The default values for this parameter are **wbemFlagReturnImmediately** and **wbemQueryFlagDeep**.</span></span> <span data-ttu-id="f26cf-122">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="f26cf-122">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="f26cf-123"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="f26cf-123"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="f26cf-124">強制列舉只包含指定之父類別的直屬子類別。</span><span class="sxs-lookup"><span data-stu-id="f26cf-124">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="f26cf-125"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="f26cf-125"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="f26cf-126">此參數的預設值。</span><span class="sxs-lookup"><span data-stu-id="f26cf-126">Default for this parameter.</span></span> <span data-ttu-id="f26cf-127">此值會強制遞迴列舉至所有衍生自指定父類別的子類別。</span><span class="sxs-lookup"><span data-stu-id="f26cf-127">This value forces recursive enumeration into all subclasses that are derived from the specified parent class.</span></span> <span data-ttu-id="f26cf-128">列舉中不會傳回父類別。</span><span class="sxs-lookup"><span data-stu-id="f26cf-128">The parent class is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="f26cf-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* (16 (0x10) ) </span><span class="sxs-lookup"><span data-stu-id="f26cf-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="f26cf-130">導致呼叫立即返回。</span><span class="sxs-lookup"><span data-stu-id="f26cf-130">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="f26cf-131"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="f26cf-131"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="f26cf-132">導致此呼叫封鎖，直到呼叫完成為止。</span><span class="sxs-lookup"><span data-stu-id="f26cf-132">Causes this call to block until the call has completed.</span></span> <span data-ttu-id="f26cf-133">此旗標會在同步模式中呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="f26cf-133">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="f26cf-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="f26cf-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="f26cf-135">讓 WMI 以基類定義傳回類別修訂資料。</span><span class="sxs-lookup"><span data-stu-id="f26cf-135">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="f26cf-136">如需詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="f26cf-136">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f26cf-137">*objWbemNamedValueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="f26cf-137">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f26cf-138">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="f26cf-138">Typically, this is undefined.</span></span> <span data-ttu-id="f26cf-139">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表可由提供者服務來處理要求的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="f26cf-139">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider servicing the request.</span></span> <span data-ttu-id="f26cf-140">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="f26cf-140">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f26cf-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="f26cf-141">Return value</span></span>

<span data-ttu-id="f26cf-142">如果方法成功，則會傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="f26cf-142">If the method is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f26cf-143">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="f26cf-143">Error codes</span></span>

<span data-ttu-id="f26cf-144">**SubclassesOf** 方法完成後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f26cf-144">After the completion of the **SubclassesOf** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="f26cf-145">具有零個元素的傳回集合不是錯誤。</span><span class="sxs-lookup"><span data-stu-id="f26cf-145">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="f26cf-146">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="f26cf-146">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="f26cf-147">目前的使用者沒有許可權可查看呼叫所傳回的一或多個類別。</span><span class="sxs-lookup"><span data-stu-id="f26cf-147">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="f26cf-148">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="f26cf-148">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="f26cf-149">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f26cf-149">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="f26cf-150">**wbemErrInvalidClass** -2147749904 (0x80041010) </span><span class="sxs-lookup"><span data-stu-id="f26cf-150">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="f26cf-151">指定的類別不存在。</span><span class="sxs-lookup"><span data-stu-id="f26cf-151">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="f26cf-152">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="f26cf-152">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="f26cf-153">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="f26cf-153">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="f26cf-154">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="f26cf-154">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="f26cf-155">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="f26cf-155">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f26cf-156">範例</span><span class="sxs-lookup"><span data-stu-id="f26cf-156">Examples</span></span>

<span data-ttu-id="f26cf-157">下列 PowerShell 範例示範如何在遠端系統上取出類別的子類別。</span><span class="sxs-lookup"><span data-stu-id="f26cf-157">The following PowerShell sample shows how to retrieve the subclasses of a class on a remote system.</span></span>


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a><span data-ttu-id="f26cf-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="f26cf-158">Requirements</span></span>



| <span data-ttu-id="f26cf-159">需求</span><span class="sxs-lookup"><span data-stu-id="f26cf-159">Requirement</span></span> | <span data-ttu-id="f26cf-160">值</span><span class="sxs-lookup"><span data-stu-id="f26cf-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f26cf-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f26cf-161">Minimum supported client</span></span><br/> | <span data-ttu-id="f26cf-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f26cf-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f26cf-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f26cf-163">Minimum supported server</span></span><br/> | <span data-ttu-id="f26cf-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f26cf-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f26cf-165">標頭</span><span class="sxs-lookup"><span data-stu-id="f26cf-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="f26cf-166"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="f26cf-166"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f26cf-167">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f26cf-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="f26cf-168"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f26cf-168"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f26cf-169">DLL</span><span class="sxs-lookup"><span data-stu-id="f26cf-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f26cf-170"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f26cf-170"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f26cf-171">CLSID</span><span class="sxs-lookup"><span data-stu-id="f26cf-171">CLSID</span></span><br/>                    | <span data-ttu-id="f26cf-172">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="f26cf-172">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="f26cf-173">IID</span><span class="sxs-lookup"><span data-stu-id="f26cf-173">IID</span></span><br/>                      | <span data-ttu-id="f26cf-174">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="f26cf-174">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="f26cf-175">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f26cf-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f26cf-176">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="f26cf-176">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="f26cf-177">**Swbemobjectset 搭配使用**</span><span class="sxs-lookup"><span data-stu-id="f26cf-177">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

 




