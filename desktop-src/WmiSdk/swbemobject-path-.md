---
description: '\_SWbemObject 物件的 Path 屬性會傳回 SWbemObjectPath 物件，此物件代表目前類別或實例的物件路徑。 這個屬性可以做為參數傳遞給需要物件路徑的方法。'
ms.assetid: 85a55159-5f10-49b5-bc37-39d7b4dfccd7
ms.tgt_platform: multiple
title: 'SWbemObject.Path_ 屬性 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Path_
- ISWbemObject.Path_
- ISWbemObject.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 773f6f9bb04aa31290bc351550a45d849d74e06f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193446"
---
# <a name="swbemobjectpath_-property"></a><span data-ttu-id="77725-104">SWbemObject 路徑 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="77725-104">SWbemObject.Path\_ property</span></span>

<span data-ttu-id="77725-105">[**SWbemObject**](swbemobject.md)物件的 **Path \_** 屬性會傳回 [**SWbemObjectPath**](swbemobjectpath.md)物件，此物件代表目前類別或實例的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="77725-105">The **Path\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span> <span data-ttu-id="77725-106">這個屬性可以做為參數傳遞給需要物件路徑的方法。</span><span class="sxs-lookup"><span data-stu-id="77725-106">This property can be passed as a parameter to methods that require an object path.</span></span>

<span data-ttu-id="77725-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="77725-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="77725-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="77725-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="77725-109">語法</span><span class="sxs-lookup"><span data-stu-id="77725-109">Syntax</span></span>


```VB
SWbemObject.Path_ As Object
```



## <a name="property-value"></a><span data-ttu-id="77725-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="77725-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="77725-111">備註</span><span class="sxs-lookup"><span data-stu-id="77725-111">Remarks</span></span>

<span data-ttu-id="77725-112">只有傳回之 [**SWbemObjectPath**](swbemobjectpath.md)實例的 [**Class**](swbemobjectpath-class.md)屬性可以修改。</span><span class="sxs-lookup"><span data-stu-id="77725-112">Only the [**Class**](swbemobjectpath-class.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance can be modified.</span></span> <span data-ttu-id="77725-113">如果您嘗試修改任何其他屬性，或嘗試呼叫 [**SetAsClass**](swbemobjectpath-setasclass.md) 或 [**SetAsSingleton**](swbemobjectpath-setassingleton.md)方法，您將會收到 **wbemErrReadOnly** 錯誤。</span><span class="sxs-lookup"><span data-stu-id="77725-113">If you try to modify any other property, or try to call the methods [**SetAsClass**](swbemobjectpath-setasclass.md) or [**SetAsSingleton**](swbemobjectpath-setassingleton.md), you will get a **wbemErrReadOnly** error.</span></span>

<span data-ttu-id="77725-114">因此，您無法修改 [**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，此物件是所傳回 [**SWbemObjectPath**](swbemobjectpath.md)實例之索引 [**鍵**](swbemobjectpath-keys.md)屬性的值。</span><span class="sxs-lookup"><span data-stu-id="77725-114">Because of this, you cannot modify the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is the value of the [**Keys**](swbemobjectpath-keys.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance.</span></span> <span data-ttu-id="77725-115">如果您嘗試對此值呼叫 [**Add**](swbemnamedvalueset-add.md)、 [**Remove**](swbemnamedvalueset-remove.md)或 [**DeleteAll**](swbemnamedvalueset-deleteall.md) 方法，將會收到 wbemErrReadOnly 錯誤。</span><span class="sxs-lookup"><span data-stu-id="77725-115">If you try to call the [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md), or [**DeleteAll**](swbemnamedvalueset-deleteall.md) methods on this value, you will get a wbemErrReadOnly error.</span></span> <span data-ttu-id="77725-116">此外，您無法修改從此集合取得的任何 [**SWbemNamedValue**](swbemnamedvalue.md) 。</span><span class="sxs-lookup"><span data-stu-id="77725-116">Furthermore, you cannot modify any [**SWbemNamedValue**](swbemnamedvalue.md) obtained from this collection.</span></span> <span data-ttu-id="77725-117">嘗試修改 **Value** 屬性會傳回相同的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="77725-117">Attempts to modify the **Value** property return the same error code.</span></span>

<span data-ttu-id="77725-118">但是，如果您呼叫 [**SWbemObject \_**](swbemobject-clone-.md)來建立複本，則複本的 [**SWbemObjectPath. Path**](swbemobjectpath-path.md)屬性可完全修改。</span><span class="sxs-lookup"><span data-stu-id="77725-118">However, if you call [**SWbemObject.Clone\_**](swbemobject-clone-.md) to create a copy, the [**SWbemObjectPath.Path**](swbemobjectpath-path.md) property of the copy is fully modifiable.</span></span>

## <a name="examples"></a><span data-ttu-id="77725-119">範例</span><span class="sxs-lookup"><span data-stu-id="77725-119">Examples</span></span>

<span data-ttu-id="77725-120">下列程式碼範例取自 TechNet 資源庫中的 [所有 Wmi Cimv2 類別](https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517) ，並使用 Path \_ 屬性列出所有 wmi cimv2 類別。</span><span class="sxs-lookup"><span data-stu-id="77725-120">The following code sample, taken from [List All the WMI cimV2 Classes](https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517) in the TechNet Gallery, uses the Path\_ property to list all the WMI cimV2 classes.</span></span>


```VB
strComputer = "." 
Set objWMIService=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\root\cimv2") 
  
For Each objclass in objWMIService.SubclassesOf() 
    Wscript.Echo objClass.Path_.Class 
Next 
```



## <a name="requirements"></a><span data-ttu-id="77725-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="77725-121">Requirements</span></span>



| <span data-ttu-id="77725-122">需求</span><span class="sxs-lookup"><span data-stu-id="77725-122">Requirement</span></span> | <span data-ttu-id="77725-123">值</span><span class="sxs-lookup"><span data-stu-id="77725-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77725-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="77725-124">Minimum supported client</span></span><br/> | <span data-ttu-id="77725-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77725-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="77725-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="77725-126">Minimum supported server</span></span><br/> | <span data-ttu-id="77725-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77725-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="77725-128">標頭</span><span class="sxs-lookup"><span data-stu-id="77725-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="77725-129"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="77725-129"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="77725-130">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="77725-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="77725-131"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="77725-131"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="77725-132">DLL</span><span class="sxs-lookup"><span data-stu-id="77725-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77725-133"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77725-133"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="77725-134">CLSID</span><span class="sxs-lookup"><span data-stu-id="77725-134">CLSID</span></span><br/>                    | <span data-ttu-id="77725-135">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="77725-135">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="77725-136">IID</span><span class="sxs-lookup"><span data-stu-id="77725-136">IID</span></span><br/>                      | <span data-ttu-id="77725-137">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="77725-137">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




