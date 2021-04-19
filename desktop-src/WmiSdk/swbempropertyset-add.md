---
description: 內含物件的 Add 方法會將 Swbempropertyset 物件加入至內含集合。 如果集合中已經有相同名稱的屬性，則會將其內容取代為新的定義。
ms.assetid: 52a5f964-3d53-441b-9a58-650afdc5b1b9
ms.tgt_platform: multiple
title: '內含： Add 方法 (>wbemdisp.tlb. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Add
- ISWbemPropertySet.Add
- ISWbemPropertySet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1ad5b40d31d162b287bdb1a387cd0602e0be1ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975488"
---
# <a name="swbempropertysetadd-method"></a><span data-ttu-id="fe1fa-104">內含新增方法</span><span class="sxs-lookup"><span data-stu-id="fe1fa-104">SWbemPropertySet.Add method</span></span>

<span data-ttu-id="fe1fa-105">[**內含**](swbempropertyset.md)物件的 **Add** 方法會將 [**swbempropertyset**](swbemproperty.md)物件加入至 **內含** 集合。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-105">The **Add** method of the [**SWbemPropertySet**](swbempropertyset.md) object adds an [**SWbemProperty**](swbemproperty.md) object to the **SWbemPropertySet** collection.</span></span> <span data-ttu-id="fe1fa-106">如果集合中已經有相同名稱的屬性，則會將其內容取代為新的定義。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-106">If a property with the same name already exists in the collection, its contents are replaced with the new definition.</span></span>

> [!Note]  
> <span data-ttu-id="fe1fa-107">在這項作業之後，已加入的屬性值為 **Null** (未指派) 。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-107">The value of the added property is **NULL** (unassigned) after this operation.</span></span> <span data-ttu-id="fe1fa-108">若要設定或變更 WMI 屬性的值，您必須設定所傳回之 [**swbempropertyset**](swbemproperty.md)物件的 [**value**](swbemdatetime-value.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-108">To set or change the value of a WMI property, you must set the [**Value**](swbemdatetime-value.md) property of the returned [**SWbemProperty**](swbemproperty.md) object.</span></span>

 

<span data-ttu-id="fe1fa-109">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fe1fa-110">語法</span><span class="sxs-lookup"><span data-stu-id="fe1fa-110">Syntax</span></span>


```VB
objProperty = .Add( _
  ByVal strName, _
  ByVal iCIMType, _
  [ ByVal bIsArray ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="fe1fa-111">參數</span><span class="sxs-lookup"><span data-stu-id="fe1fa-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe1fa-112">*strName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe1fa-112">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe1fa-113">必要。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-113">Required.</span></span> <span data-ttu-id="fe1fa-114">新屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-114">Name of the new property.</span></span>

</dd> <dt>

<span data-ttu-id="fe1fa-115">*iCIMType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe1fa-115">*iCIMType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe1fa-116">必要。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-116">Required.</span></span> <span data-ttu-id="fe1fa-117">整數，表示新屬性的 **CIMType** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-117">An integer that represents the **CIMType** qualifier of the new property.</span></span> <span data-ttu-id="fe1fa-118">如需 **CIMType** 辨識符號及其值的清單，請參閱 [**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum) 。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-118">See [**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum) for the list with the **CIMType** qualifiers and their values.</span></span>

</dd> <dt>

<span data-ttu-id="fe1fa-119">*bIsArray* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="fe1fa-119">*bIsArray* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe1fa-120">指定屬性是否為數組類型。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-120">Specifies whether the property is an array type.</span></span> <span data-ttu-id="fe1fa-121">此參數的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-121">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fe1fa-122">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="fe1fa-122">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe1fa-123">如果已指定，則必須為零。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-123">Reserved and must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe1fa-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe1fa-124">Return value</span></span>

<span data-ttu-id="fe1fa-125">如果成功，這個方法會傳回代表新屬性的 [**swbempropertyset**](swbemproperty.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-125">If successful, this method returns an [**SWbemProperty**](swbemproperty.md) object that represents the new property.</span></span> <span data-ttu-id="fe1fa-126">否則，會傳回 **null** 物件。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-126">Otherwise, a **null** object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fe1fa-127">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="fe1fa-127">Error codes</span></span>

<span data-ttu-id="fe1fa-128">完成 **Add** 方法之後， **Err** 物件可能會包含下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-128">After completion of the **Add** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="fe1fa-129">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="fe1fa-129">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="fe1fa-130">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-130">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="fe1fa-131">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="fe1fa-131">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="fe1fa-132">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-132">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="fe1fa-133">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="fe1fa-133">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="fe1fa-134">記憶體不足，無法執行此方法。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-134">Not enough memory for this method to execute.</span></span>

</dd> <dt>

<span data-ttu-id="fe1fa-135">**wbemErrInvalidPropertyType** -2147749930</span><span class="sxs-lookup"><span data-stu-id="fe1fa-135">**wbemErrInvalidPropertyType** - 2147749930</span></span>
</dt> <dd>

<span data-ttu-id="fe1fa-136">無法辨識 **CIMType** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-136">The **CIMType** qualifier is not recognized.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="fe1fa-137">範例</span><span class="sxs-lookup"><span data-stu-id="fe1fa-137">Examples</span></span>

<span data-ttu-id="fe1fa-138">如需使用此方法的程式碼範例，請參閱 [**內含**](swbempropertyset.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-138">For a code example that uses this method, see the [**SWbemPropertySet**](swbempropertyset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe1fa-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe1fa-139">Requirements</span></span>



| <span data-ttu-id="fe1fa-140">需求</span><span class="sxs-lookup"><span data-stu-id="fe1fa-140">Requirement</span></span> | <span data-ttu-id="fe1fa-141">值</span><span class="sxs-lookup"><span data-stu-id="fe1fa-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe1fa-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe1fa-142">Minimum supported client</span></span><br/> | <span data-ttu-id="fe1fa-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe1fa-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fe1fa-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe1fa-144">Minimum supported server</span></span><br/> | <span data-ttu-id="fe1fa-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe1fa-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fe1fa-146">標頭</span><span class="sxs-lookup"><span data-stu-id="fe1fa-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe1fa-147"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="fe1fa-147"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fe1fa-148">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="fe1fa-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="fe1fa-149"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fe1fa-149"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fe1fa-150">DLL</span><span class="sxs-lookup"><span data-stu-id="fe1fa-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe1fa-151"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe1fa-151"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fe1fa-152">CLSID</span><span class="sxs-lookup"><span data-stu-id="fe1fa-152">CLSID</span></span><br/>                    | <span data-ttu-id="fe1fa-153">CLSID \_ 內含</span><span class="sxs-lookup"><span data-stu-id="fe1fa-153">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="fe1fa-154">IID</span><span class="sxs-lookup"><span data-stu-id="fe1fa-154">IID</span></span><br/>                      | <span data-ttu-id="fe1fa-155">IID \_ ISWbemPropertySet</span><span class="sxs-lookup"><span data-stu-id="fe1fa-155">IID\_ISWbemPropertySet</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="fe1fa-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe1fa-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe1fa-157">**內含**</span><span class="sxs-lookup"><span data-stu-id="fe1fa-157">**SWbemPropertySet**</span></span>](swbempropertyset.md)
</dt> <dt>

[<span data-ttu-id="fe1fa-158">**內含。移除**</span><span class="sxs-lookup"><span data-stu-id="fe1fa-158">**SWbemPropertySet.Remove**</span></span>](swbempropertyset-remove.md)
</dt> <dt>

[<span data-ttu-id="fe1fa-159">**Swbempropertyset。值**</span><span class="sxs-lookup"><span data-stu-id="fe1fa-159">**SWbemProperty.Value**</span></span>](swbemproperty-value.md)
</dt> </dl>

 

 




