---
description: 您可以使用 SWbemMethod 物件的屬性來檢查 WMI 物件的單一方法定義。 VBScript CreateObject 呼叫無法建立這個物件。
ms.assetid: 461d5c41-4930-40cf-96e2-bc8cae335b60
ms.tgt_platform: multiple
title: 'SWbemMethod 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod
- ISWbemMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 055957bf2774fc1e5c2e1f0149b00ece7b0a1bea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512985"
---
# <a name="swbemmethod-object"></a><span data-ttu-id="56a48-104">SWbemMethod 物件</span><span class="sxs-lookup"><span data-stu-id="56a48-104">SWbemMethod object</span></span>

<span data-ttu-id="56a48-105">您可以使用 **SWbemMethod** 物件的屬性來檢查 WMI 物件的單一方法定義。</span><span class="sxs-lookup"><span data-stu-id="56a48-105">You can use the properties of the **SWbemMethod** object to inspect a single method definition of a WMI object.</span></span> <span data-ttu-id="56a48-106">VBScript **CreateObject** 呼叫無法建立這個物件。</span><span class="sxs-lookup"><span data-stu-id="56a48-106">This object cannot be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="56a48-107">此物件可以用來檢查方法的定義。</span><span class="sxs-lookup"><span data-stu-id="56a48-107">This object can be used to inspect the definitions of methods.</span></span> <span data-ttu-id="56a48-108">若要叫用方法，您應該使用直接存取 (參閱在 [**SWbemObject**](swbemobject.md) (上 [操作類別和實例資訊](manipulating-class-and-instance-information.md)) 這是建議的機制) 物件或 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)呼叫。</span><span class="sxs-lookup"><span data-stu-id="56a48-108">To invoke the methods, you should use either direct access (see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md)) on an [**SWbemObject**](swbemobject.md) (which is the recommended mechanism) object, or the [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) call.</span></span>

> [!Note]  
> <span data-ttu-id="56a48-109">在此版本的 API 中，不支援方法資訊的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="56a48-109">In this version of the API, write access to method information is not supported.</span></span> <span data-ttu-id="56a48-110">如果您想要定義方法或修改現有的方法定義，可以在 MOF 檔案中定義方法變更，然後使用 [MOF 編譯器](compiling-mof-files.md)來提交變更。</span><span class="sxs-lookup"><span data-stu-id="56a48-110">If you want to define methods or modify existing method definitions, you can define the method changes in a MOF file and submit the changes using the [MOF Compiler](compiling-mof-files.md).</span></span> <span data-ttu-id="56a48-111">或者，使用 [適用于 WMI 的 COM API](com-api-for-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="56a48-111">Alternatively, use the [COM API for WMI](com-api-for-wmi.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="56a48-112">成員</span><span class="sxs-lookup"><span data-stu-id="56a48-112">Members</span></span>

<span data-ttu-id="56a48-113">**SWbemMethod** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="56a48-113">The **SWbemMethod** object has these types of members:</span></span>

-   [<span data-ttu-id="56a48-114">屬性</span><span class="sxs-lookup"><span data-stu-id="56a48-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="56a48-115">屬性</span><span class="sxs-lookup"><span data-stu-id="56a48-115">Properties</span></span>

<span data-ttu-id="56a48-116">**SWbemMethod** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="56a48-116">The **SWbemMethod** object has these properties.</span></span>



| <span data-ttu-id="56a48-117">屬性</span><span class="sxs-lookup"><span data-stu-id="56a48-117">Property</span></span>                                                      | <span data-ttu-id="56a48-118">存取類型</span><span class="sxs-lookup"><span data-stu-id="56a48-118">Access type</span></span>          | <span data-ttu-id="56a48-119">Description</span><span class="sxs-lookup"><span data-stu-id="56a48-119">Description</span></span>                                                                                                                        |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="56a48-120">**InParameters**</span><span class="sxs-lookup"><span data-stu-id="56a48-120">**InParameters**</span></span>](swbemmethod-inparameters.md)<br/>   | <span data-ttu-id="56a48-121">唯讀</span><span class="sxs-lookup"><span data-stu-id="56a48-121">Read-only</span></span><br/> | <span data-ttu-id="56a48-122">[**SWbemObject**](swbemobject.md)物件，其屬性會定義此方法的輸入參數。</span><span class="sxs-lookup"><span data-stu-id="56a48-122">An [**SWbemObject**](swbemobject.md) object whose properties define the input parameters for this method.</span></span><br/>              |
| [<span data-ttu-id="56a48-123">**Name**</span><span class="sxs-lookup"><span data-stu-id="56a48-123">**Name**</span></span>](swbemmethod-name.md)<br/>                   | <span data-ttu-id="56a48-124">唯讀</span><span class="sxs-lookup"><span data-stu-id="56a48-124">Read-only</span></span><br/> | <span data-ttu-id="56a48-125">方法的名稱。</span><span class="sxs-lookup"><span data-stu-id="56a48-125">Name of the method.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="56a48-126">**起源**</span><span class="sxs-lookup"><span data-stu-id="56a48-126">**Origin**</span></span>](swbemmethod-origin.md)<br/>               | <span data-ttu-id="56a48-127">唯讀</span><span class="sxs-lookup"><span data-stu-id="56a48-127">Read-only</span></span><br/> | <span data-ttu-id="56a48-128">方法的原始類別。</span><span class="sxs-lookup"><span data-stu-id="56a48-128">Originating class of the method.</span></span><br/>                                                                                        |
| [<span data-ttu-id="56a48-129">**OutParameters**</span><span class="sxs-lookup"><span data-stu-id="56a48-129">**OutParameters**</span></span>](swbemmethod-outparameters.md)<br/> | <span data-ttu-id="56a48-130">唯讀</span><span class="sxs-lookup"><span data-stu-id="56a48-130">Read-only</span></span><br/> | <span data-ttu-id="56a48-131">[**SWbemObject**](swbemobject.md)物件，其屬性會定義此方法的 out 參數和傳回型別。</span><span class="sxs-lookup"><span data-stu-id="56a48-131">An [**SWbemObject**](swbemobject.md) object whose properties define the out parameters and return type of this method.</span></span><br/> |
| [<span data-ttu-id="56a48-132">**限定詞\_**</span><span class="sxs-lookup"><span data-stu-id="56a48-132">**Qualifiers\_**</span></span>](swbemmethod-qualifiers-.md)<br/>    | <span data-ttu-id="56a48-133">唯讀</span><span class="sxs-lookup"><span data-stu-id="56a48-133">Read-only</span></span><br/> | <span data-ttu-id="56a48-134">[**SWbemQualifierSet**](swbemqualifierset.md)物件，其中包含這個方法的限定詞。</span><span class="sxs-lookup"><span data-stu-id="56a48-134">An [**SWbemQualifierSet**](swbemqualifierset.md) object that contains the qualifiers for this method.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="56a48-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="56a48-135">Requirements</span></span>



| <span data-ttu-id="56a48-136">需求</span><span class="sxs-lookup"><span data-stu-id="56a48-136">Requirement</span></span> | <span data-ttu-id="56a48-137">值</span><span class="sxs-lookup"><span data-stu-id="56a48-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56a48-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56a48-138">Minimum supported client</span></span><br/> | <span data-ttu-id="56a48-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56a48-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="56a48-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56a48-140">Minimum supported server</span></span><br/> | <span data-ttu-id="56a48-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56a48-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="56a48-142">標頭</span><span class="sxs-lookup"><span data-stu-id="56a48-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="56a48-143"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="56a48-143"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="56a48-144">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="56a48-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="56a48-145"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="56a48-145"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="56a48-146">DLL</span><span class="sxs-lookup"><span data-stu-id="56a48-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56a48-147"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56a48-147"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="56a48-148">CLSID</span><span class="sxs-lookup"><span data-stu-id="56a48-148">CLSID</span></span><br/>                    | <span data-ttu-id="56a48-149">CLSID \_ SWbemMethod</span><span class="sxs-lookup"><span data-stu-id="56a48-149">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="56a48-150">IID</span><span class="sxs-lookup"><span data-stu-id="56a48-150">IID</span></span><br/>                      | <span data-ttu-id="56a48-151">IID \_ ISWbemMethod</span><span class="sxs-lookup"><span data-stu-id="56a48-151">IID\_ISWbemMethod</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="56a48-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56a48-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56a48-153">腳本 API 物件</span><span class="sxs-lookup"><span data-stu-id="56a48-153">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




