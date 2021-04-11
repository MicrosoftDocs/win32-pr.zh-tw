---
description: '\_SWbemLastError 物件的 Path 屬性會傳回 SWbemObjectPath 物件，此物件代表目前類別或實例的物件路徑。 這個屬性可以做為參數傳遞給需要物件路徑的方法。'
ms.assetid: 5472e463-54cb-4ba2-8c00-08b70013e38d
ms.tgt_platform: multiple
title: 'SWbemLastError.Path_ 屬性 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Path_
- ISWbemLastError.Path_
- ISWbemLastError.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c979fd76ffb4ee97f62362d53fac4151de17bae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026962"
---
# <a name="swbemlasterrorpath_-property"></a><span data-ttu-id="167a2-104">SWbemLastError 路徑 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="167a2-104">SWbemLastError.Path\_ property</span></span>

<span data-ttu-id="167a2-105">[**SWbemLastError**](swbemlasterror.md)物件的 **Path \_** 屬性會傳回 [**SWbemObjectPath**](swbemobjectpath.md)物件，此物件代表目前類別或實例的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="167a2-105">The **Path\_** property of the [**SWbemLastError**](swbemlasterror.md) object returns an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span> <span data-ttu-id="167a2-106">這個屬性可以做為參數傳遞給需要物件路徑的方法。</span><span class="sxs-lookup"><span data-stu-id="167a2-106">This property can be passed as a parameter to methods that require an object path.</span></span>

<span data-ttu-id="167a2-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="167a2-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="167a2-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="167a2-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="167a2-109">語法</span><span class="sxs-lookup"><span data-stu-id="167a2-109">Syntax</span></span>


```VB
SWbemLastError.Path_ As Object
```



## <a name="property-value"></a><span data-ttu-id="167a2-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="167a2-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="167a2-111">備註</span><span class="sxs-lookup"><span data-stu-id="167a2-111">Remarks</span></span>

<span data-ttu-id="167a2-112">只有傳回之 [**SWbemObjectPath**](swbemobjectpath.md)實例的 [**Class**](swbemobjectpath-class.md)屬性可以修改。</span><span class="sxs-lookup"><span data-stu-id="167a2-112">Only the [**Class**](swbemobjectpath-class.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance can be modified.</span></span> <span data-ttu-id="167a2-113">如果您嘗試修改任何其他屬性，或嘗試呼叫 [**SetAsClass**](swbemobjectpath-setasclass.md) 或 [**SetAsSingleton**](swbemobjectpath-setassingleton.md) 方法，則會出現 **wbemErrReadOnly** 錯誤。</span><span class="sxs-lookup"><span data-stu-id="167a2-113">If you try to modify any other property, or try to call the [**SetAsClass**](swbemobjectpath-setasclass.md) or [**SetAsSingleton**](swbemobjectpath-setassingleton.md) methods, you get an error of **wbemErrReadOnly**.</span></span>

<span data-ttu-id="167a2-114">因此，您無法修改 [**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，此物件是所傳回 [**SWbemObjectPath**](swbemobjectpath.md)實例之索引 [**鍵**](swbemobjectpath-keys.md)屬性的值。</span><span class="sxs-lookup"><span data-stu-id="167a2-114">Because of this, you cannot modify the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is the value of the [**Keys**](swbemobjectpath-keys.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance.</span></span> <span data-ttu-id="167a2-115">如果您嘗試對此值呼叫 [**Add**](swbemnamedvalueset-add.md)、 [**Remove**](swbemnamedvalueset-remove.md)或 [**DeleteAll**](swbemnamedvalueset-deleteall.md) 方法，就會收到 **wbemErrReadOnly** 錯誤。</span><span class="sxs-lookup"><span data-stu-id="167a2-115">If you try to call the [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md), or [**DeleteAll**](swbemnamedvalueset-deleteall.md) methods on this value, you get a **wbemErrReadOnly** error.</span></span> <span data-ttu-id="167a2-116">此外，您無法修改從此集合取得的任何 [**SWbemNamedValue**](swbemnamedvalue.md) 。</span><span class="sxs-lookup"><span data-stu-id="167a2-116">Furthermore, you cannot modify any [**SWbemNamedValue**](swbemnamedvalue.md) obtained from this collection.</span></span> <span data-ttu-id="167a2-117">嘗試修改 [**Value**](swbemnamedvalue-value.md) 屬性會傳回相同的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="167a2-117">Attempts to modify the [**Value**](swbemnamedvalue-value.md) property return the same error code.</span></span>

<span data-ttu-id="167a2-118">但是，如果您呼叫 [**SWbemObject \_**](swbemobject-clone-.md)來建立複本，就可以完全修改複製的 [**Path \_**](swbemobject-path-.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="167a2-118">However, if you call [**SWbemObject.Clone\_**](swbemobject-clone-.md) to create a copy, the [**Path\_**](swbemobject-path-.md) property of the copy is fully modifiable.</span></span>

## <a name="requirements"></a><span data-ttu-id="167a2-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="167a2-119">Requirements</span></span>



| <span data-ttu-id="167a2-120">需求</span><span class="sxs-lookup"><span data-stu-id="167a2-120">Requirement</span></span> | <span data-ttu-id="167a2-121">值</span><span class="sxs-lookup"><span data-stu-id="167a2-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="167a2-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="167a2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="167a2-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="167a2-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="167a2-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="167a2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="167a2-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="167a2-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="167a2-126">標頭</span><span class="sxs-lookup"><span data-stu-id="167a2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="167a2-127"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="167a2-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="167a2-128">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="167a2-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="167a2-129"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="167a2-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="167a2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="167a2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="167a2-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="167a2-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="167a2-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="167a2-132">CLSID</span></span><br/>                    | <span data-ttu-id="167a2-133">CLSID \_ SWbemLastError</span><span class="sxs-lookup"><span data-stu-id="167a2-133">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="167a2-134">IID</span><span class="sxs-lookup"><span data-stu-id="167a2-134">IID</span></span><br/>                      | <span data-ttu-id="167a2-135">IID \_ ISWbemLastError</span><span class="sxs-lookup"><span data-stu-id="167a2-135">IID\_ISWbemLastError</span></span><br/>                                                         |



 

 




