---
description: 根據物件路徑，抓取屬於類別定義或實例的物件。
ms.assetid: 3071aeb2-adab-47aa-a10c-9796766bb630
ms.tgt_platform: multiple
title: 'SWbemServices： Get 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Get
- ISWbemServices.Get
- ISWbemServices.Get
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c8998a1ca04206362fcc0e7405fccf8c923d74d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981609"
---
# <a name="swbemservicesget-method"></a><span data-ttu-id="9ebe1-103">SWbemServices. Get 方法</span><span class="sxs-lookup"><span data-stu-id="9ebe1-103">SWbemServices.Get method</span></span>

<span data-ttu-id="9ebe1-104">[**SWbemServices**](swbemservices.md)物件的 **Get** 方法會根據物件路徑，來抓取物件（也就是類別定義或實例）。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-104">The **Get** method of the [**SWbemServices**](swbemservices.md) object retrieves an object, that is either a class definition or an instance, based on the object path.</span></span> <span data-ttu-id="9ebe1-105">這個方法只會從與目前 **SWbemServices** 物件相關聯的命名空間中，抓取物件。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-105">This method retrieves only objects from the namespace that is associated with the current **SWbemServices** object.</span></span>

<span data-ttu-id="9ebe1-106">方法是在同步模式中呼叫。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-106">The method is called in the synchronous mode.</span></span> <span data-ttu-id="9ebe1-107">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="9ebe1-108">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9ebe1-109">語法</span><span class="sxs-lookup"><span data-stu-id="9ebe1-109">Syntax</span></span>


```VB
objWbemObject = .Get( _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9ebe1-110">參數</span><span class="sxs-lookup"><span data-stu-id="9ebe1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ebe1-111">*strObjectPath* \[選\]</span><span class="sxs-lookup"><span data-stu-id="9ebe1-111">*strObjectPath* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9ebe1-112">字串，包含要取得之物件的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-112">String that contains the object path of the object to retrieve.</span></span> <span data-ttu-id="9ebe1-113">如果這個值是空的，則傳回的空物件可以成為新的類別。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-113">If this value is empty, the empty object that is returned can become a new class.</span></span> <span data-ttu-id="9ebe1-114">如需詳細資訊，請參閱 [描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-114">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ebe1-115">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="9ebe1-115">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9ebe1-116">判斷查詢行為的整數。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-116">Integer that determines the behavior of the query.</span></span> <span data-ttu-id="9ebe1-117">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-117">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="9ebe1-118"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="9ebe1-118"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="9ebe1-119">讓 WMI 以基類定義傳回類別修訂資料。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-119">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="9ebe1-120">如需修改過的限定詞的詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-120">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9ebe1-121">*objWbemNamedValueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="9ebe1-121">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9ebe1-122">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-122">Typically, this is undefined.</span></span> <span data-ttu-id="9ebe1-123">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-123">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="9ebe1-124">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-124">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ebe1-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="9ebe1-125">Return value</span></span>

<span data-ttu-id="9ebe1-126">如果成功，這個方法會傳回代表所要求之物件的 [**SWbemObject**](swbemobject.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-126">If successful, this method returns an [**SWbemObject**](swbemobject.md) object that represents the requested object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9ebe1-127">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="9ebe1-127">Error codes</span></span>

<span data-ttu-id="9ebe1-128">完成 **Get** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-128">Upon the completion of the **Get** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="9ebe1-129">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="9ebe1-129">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="9ebe1-130">目前的使用者沒有存取該物件的許可權。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-130">Current user does not have the permission to access the object.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe1-131">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="9ebe1-131">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="9ebe1-132">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-132">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe1-133">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="9ebe1-133">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="9ebe1-134">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-134">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe1-135">**wbemErrInvalidObjectPath** -2147749946 (0x8004103A) </span><span class="sxs-lookup"><span data-stu-id="9ebe1-135">**wbemErrInvalidObjectPath** - 2147749946 (0x8004103A)</span></span>
</dt> <dd>

<span data-ttu-id="9ebe1-136">指定的路徑無效。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-136">Specified path was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe1-137">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="9ebe1-137">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="9ebe1-138">找不到要求的物件。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-138">Requested object could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe1-139">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="9ebe1-139">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="9ebe1-140">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-140">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ebe1-141">備註</span><span class="sxs-lookup"><span data-stu-id="9ebe1-141">Remarks</span></span>

<span data-ttu-id="9ebe1-142">不同于 [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) 和 [**InstancesOf**](swbemservices-instancesof.md) 方法，Get 方法一律會傳回代表受 WMI 管理之資源的特定實例的 [**SWbemObject**](swbemobject.md) 。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-142">Unlike the [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) and [**InstancesOf**](swbemservices-instancesof.md) methods, the Get method always returns an [**SWbemObject**](swbemobject.md) representing a specific instance of a WMI-managed resource.</span></span> <span data-ttu-id="9ebe1-143">若要使用 Get 方法取得受 WMI 管理之資源的特定實例，您必須藉由將方法傳遞給物件路徑，來指示要取得的實例，如下列腳本所示。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-143">To obtain a specific instance of a WMI-managed resource using the Get method, you must tell Get the instance to retrieve by passing the method the object path, as shown in the following script.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set objSWbemObject = objSWbemServices.Get("Win32_Service.Name='Messenger'")
Wscript.Echo "Name:         " & objSWbemObject.Name        & vbCrLf & _
             "Display Name: " & objSWbemObject.DisplayName & vbCrLf & _
             "Start Mode:   " & objSWbemObject.StartMode   & vbCrLf & _
             "State:        " & objSWbemObject.State
```



<span data-ttu-id="9ebe1-144">您可以使用這個方法來取得 [*單一*](gloss-s.md)物件（例如 [**\_ \_ CIMOMIdentification**](--cimomidentification.md)），其中包含執行之 WMI 安裝的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-144">You can use this method to obtain [*singleton*](gloss-s.md) objects, such as [**\_\_CIMOMIdentification**](--cimomidentification.md), which contains version information about the WMI installation that is running.</span></span>

<span data-ttu-id="9ebe1-145">您可以使用 [CIM Studio](further-information.md) 之類的查看工具來檢查存放庫，以確認新的類別和實例出現。</span><span class="sxs-lookup"><span data-stu-id="9ebe1-145">You can examine the repository with a viewing tool such as [CIM Studio](further-information.md) to verify that the new class and instance appear.</span></span> <span data-ttu-id="9ebe1-146">如需從存放庫中移除類別和實例的範例，請參閱 [**SWbemServices。刪除**](swbemservices-delete.md)或 [**\_ SWbemObject。**](swbemobject-delete-.md)</span><span class="sxs-lookup"><span data-stu-id="9ebe1-146">For an example of removing a class and instance from the repository, see [**SWbemServices.Delete**](swbemservices-delete.md) or [**SWbemObject.Delete\_**](swbemobject-delete-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ebe1-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ebe1-147">Requirements</span></span>



| <span data-ttu-id="9ebe1-148">需求</span><span class="sxs-lookup"><span data-stu-id="9ebe1-148">Requirement</span></span> | <span data-ttu-id="9ebe1-149">值</span><span class="sxs-lookup"><span data-stu-id="9ebe1-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ebe1-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9ebe1-150">Minimum supported client</span></span><br/> | <span data-ttu-id="9ebe1-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ebe1-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9ebe1-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9ebe1-152">Minimum supported server</span></span><br/> | <span data-ttu-id="9ebe1-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ebe1-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9ebe1-154">標頭</span><span class="sxs-lookup"><span data-stu-id="9ebe1-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ebe1-155"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="9ebe1-155"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ebe1-156">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9ebe1-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="9ebe1-157"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9ebe1-157"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9ebe1-158">DLL</span><span class="sxs-lookup"><span data-stu-id="9ebe1-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ebe1-159"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ebe1-159"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9ebe1-160">CLSID</span><span class="sxs-lookup"><span data-stu-id="9ebe1-160">CLSID</span></span><br/>                    | <span data-ttu-id="9ebe1-161">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="9ebe1-161">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="9ebe1-162">IID</span><span class="sxs-lookup"><span data-stu-id="9ebe1-162">IID</span></span><br/>                      | <span data-ttu-id="9ebe1-163">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="9ebe1-163">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="9ebe1-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ebe1-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ebe1-165">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="9ebe1-165">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="9ebe1-166">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="9ebe1-166">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

 




