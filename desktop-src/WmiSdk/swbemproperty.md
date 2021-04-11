---
description: Swbempropertyset 物件代表 managed 物件的單一 WMI 屬性。 VBScript CreateObject 呼叫無法建立這個物件。
ms.assetid: 2ddcfffa-a7b4-4fd6-926d-411de27f6212
ms.tgt_platform: multiple
title: 'Swbempropertyset 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty
- ISWbemProperty
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9c71db4063f5de6b48b2e8213f21ca1320a880fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195226"
---
# <a name="swbemproperty-object"></a><span data-ttu-id="32121-104">Swbempropertyset 物件</span><span class="sxs-lookup"><span data-stu-id="32121-104">SWbemProperty object</span></span>

<span data-ttu-id="32121-105">**Swbempropertyset** 物件代表 managed 物件的單一 WMI 屬性。</span><span class="sxs-lookup"><span data-stu-id="32121-105">The **SWbemProperty** object represents a single WMI property of a managed object.</span></span> <span data-ttu-id="32121-106">VBScript [CreateObject](creating-an-object-using-vbscript.md) 呼叫無法建立這個物件。</span><span class="sxs-lookup"><span data-stu-id="32121-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

## <a name="members"></a><span data-ttu-id="32121-107">成員</span><span class="sxs-lookup"><span data-stu-id="32121-107">Members</span></span>

<span data-ttu-id="32121-108">**Swbempropertyset** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="32121-108">The **SWbemProperty** object has these types of members:</span></span>

-   [<span data-ttu-id="32121-109">屬性</span><span class="sxs-lookup"><span data-stu-id="32121-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32121-110">屬性</span><span class="sxs-lookup"><span data-stu-id="32121-110">Properties</span></span>

<span data-ttu-id="32121-111">**Swbempropertyset** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="32121-111">The **SWbemProperty** object has these properties.</span></span>



| <span data-ttu-id="32121-112">屬性</span><span class="sxs-lookup"><span data-stu-id="32121-112">Property</span></span>                                                     | <span data-ttu-id="32121-113">存取類型</span><span class="sxs-lookup"><span data-stu-id="32121-113">Access type</span></span>           | <span data-ttu-id="32121-114">Description</span><span class="sxs-lookup"><span data-stu-id="32121-114">Description</span></span>                                                                                                                   |
|:-------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32121-115">**CIMType**</span><span class="sxs-lookup"><span data-stu-id="32121-115">**CIMType**</span></span>](swbemproperty-cimtype.md)<br/>          | <span data-ttu-id="32121-116">唯讀</span><span class="sxs-lookup"><span data-stu-id="32121-116">Read-only</span></span><br/>  | <span data-ttu-id="32121-117">這個屬性的型別。</span><span class="sxs-lookup"><span data-stu-id="32121-117">Type of this property.</span></span><br/>                                                                                             |
| [<span data-ttu-id="32121-118">**IsArray**</span><span class="sxs-lookup"><span data-stu-id="32121-118">**IsArray**</span></span>](swbemproperty-isarray.md)<br/>          | <span data-ttu-id="32121-119">唯讀</span><span class="sxs-lookup"><span data-stu-id="32121-119">Read-only</span></span><br/>  | <span data-ttu-id="32121-120">指出此屬性是否有陣列類型的布林值。</span><span class="sxs-lookup"><span data-stu-id="32121-120">Boolean value that indicates if this property has an array type.</span></span><br/>                                                   |
| [<span data-ttu-id="32121-121">**IsLocal**</span><span class="sxs-lookup"><span data-stu-id="32121-121">**IsLocal**</span></span>](swbemproperty-islocal.md)<br/>          | <span data-ttu-id="32121-122">唯讀</span><span class="sxs-lookup"><span data-stu-id="32121-122">Read-only</span></span><br/>  | <span data-ttu-id="32121-123">指出此屬性是否為本機的布林值。</span><span class="sxs-lookup"><span data-stu-id="32121-123">Boolean value that indicates if this property is local.</span></span><br/>                                                            |
| [<span data-ttu-id="32121-124">**Name**</span><span class="sxs-lookup"><span data-stu-id="32121-124">**Name**</span></span>](swbemproperty-name.md)<br/>                | <span data-ttu-id="32121-125">唯讀</span><span class="sxs-lookup"><span data-stu-id="32121-125">Read-only</span></span><br/>  | <span data-ttu-id="32121-126">此 WMI 屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="32121-126">Name of this WMI property.</span></span><br/>                                                                                         |
| [<span data-ttu-id="32121-127">**起源**</span><span class="sxs-lookup"><span data-stu-id="32121-127">**Origin**</span></span>](swbemproperty-origin.md)<br/>            | <span data-ttu-id="32121-128">唯讀</span><span class="sxs-lookup"><span data-stu-id="32121-128">Read-only</span></span><br/>  | <span data-ttu-id="32121-129">包含這個屬性的原始類別。</span><span class="sxs-lookup"><span data-stu-id="32121-129">Contains the originating class of this property.</span></span><br/>                                                                   |
| [<span data-ttu-id="32121-130">**限定詞\_**</span><span class="sxs-lookup"><span data-stu-id="32121-130">**Qualifiers\_**</span></span>](swbemproperty-qualifiers-.md)<br/> | <span data-ttu-id="32121-131">唯讀</span><span class="sxs-lookup"><span data-stu-id="32121-131">Read-only</span></span><br/>  | <span data-ttu-id="32121-132">[**SWbemQualifierSet**](swbemqualifierset.md)物件，這個物件是這個屬性的限定詞集合。</span><span class="sxs-lookup"><span data-stu-id="32121-132">An [**SWbemQualifierSet**](swbemqualifierset.md) object, which is the collection of qualifiers for this property.</span></span><br/> |
| [<span data-ttu-id="32121-133">**值**</span><span class="sxs-lookup"><span data-stu-id="32121-133">**Value**</span></span>](swbemproperty-value.md)<br/>              | <span data-ttu-id="32121-134">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="32121-134">Read/write</span></span><br/> | <span data-ttu-id="32121-135">這個屬性的實際值。</span><span class="sxs-lookup"><span data-stu-id="32121-135">Actual value of this property.</span></span> <span data-ttu-id="32121-136">這是此物件的預設 automation 屬性。</span><span class="sxs-lookup"><span data-stu-id="32121-136">This is the default automation property of this object.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="32121-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="32121-137">Requirements</span></span>



| <span data-ttu-id="32121-138">需求</span><span class="sxs-lookup"><span data-stu-id="32121-138">Requirement</span></span> | <span data-ttu-id="32121-139">值</span><span class="sxs-lookup"><span data-stu-id="32121-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32121-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32121-140">Minimum supported client</span></span><br/> | <span data-ttu-id="32121-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32121-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="32121-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32121-142">Minimum supported server</span></span><br/> | <span data-ttu-id="32121-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32121-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="32121-144">標頭</span><span class="sxs-lookup"><span data-stu-id="32121-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="32121-145"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="32121-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="32121-146">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="32121-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="32121-147"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="32121-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="32121-148">DLL</span><span class="sxs-lookup"><span data-stu-id="32121-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32121-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32121-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="32121-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="32121-150">CLSID</span></span><br/>                    | <span data-ttu-id="32121-151">CLSID \_ swbempropertyset</span><span class="sxs-lookup"><span data-stu-id="32121-151">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="32121-152">IID</span><span class="sxs-lookup"><span data-stu-id="32121-152">IID</span></span><br/>                      | <span data-ttu-id="32121-153">IID \_ ISWbemProperty</span><span class="sxs-lookup"><span data-stu-id="32121-153">IID\_ISWbemProperty</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="32121-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32121-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32121-155">腳本 API 物件</span><span class="sxs-lookup"><span data-stu-id="32121-155">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




