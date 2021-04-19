---
description: '\_SWbemObject 物件的限定詞屬性會傳回 SWbemQualifierSet 物件，該物件為目前類別或實例的限定詞集合。 這是唯讀的屬性。'
ms.assetid: 5ecae751-0d83-4ad6-9840-ef47f76b1ff6
ms.tgt_platform: multiple
title: 'SWbemObject.Qualifiers_ 屬性 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Qualifiers_
- ISWbemObject.Qualifiers_
- ISWbemObject.get_Qualifiers_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f9526596b7ae4a387cd0751ad95aff3b97dcc817
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975011"
---
# <a name="swbemobjectqualifiers_-property"></a><span data-ttu-id="e611f-104">SWbemObject 的限定詞 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="e611f-104">SWbemObject.Qualifiers\_ property</span></span>

<span data-ttu-id="e611f-105">[**SWbemObject**](swbemobject.md)物件的 **限定詞 \_** 屬性會傳回 [**SWbemQualifierSet**](swbemqualifierset.md)物件，該物件為目前類別或實例的限定詞集合。</span><span class="sxs-lookup"><span data-stu-id="e611f-105">The **Qualifiers\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemQualifierSet**](swbemqualifierset.md) object that is a collection of the qualifiers for the current class or instance.</span></span> <span data-ttu-id="e611f-106">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="e611f-106">This property is read-only.</span></span>

<span data-ttu-id="e611f-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="e611f-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="e611f-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e611f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e611f-109">語法</span><span class="sxs-lookup"><span data-stu-id="e611f-109">Syntax</span></span>


```VB
SWbemObject.Qualifiers_ As Object
```



## <a name="property-value"></a><span data-ttu-id="e611f-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="e611f-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="e611f-111">範例</span><span class="sxs-lookup"><span data-stu-id="e611f-111">Examples</span></span>

<span data-ttu-id="e611f-112">TechNet 元件庫上 WMI 類別 VBScript 程式碼範例的 [所有限定詞都](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) 是使用 [辨識符號] \_ 屬性來列出所指定 WMI 類別的類別限定詞。</span><span class="sxs-lookup"><span data-stu-id="e611f-112">The [List All the Qualifiers for a WMI Class](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) VBScript code sample on TechNet Gallery uses the Qualifier\_ property to list the class qualifiers for a specified WMI class.</span></span>

<span data-ttu-id="e611f-113">TechNet 元件庫上 WMI VBScript 程式碼範例 [中的所有抽象類別清單](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) 會列出根 \\ cimv2 命名空間中定義的所有 wmi 抽象類別。</span><span class="sxs-lookup"><span data-stu-id="e611f-113">The [List All Abstract Classes in WMI](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) VBScript code sample on TechNet Gallery lists all WMI abstract classes defined in the root\\cimv2 namespace.</span></span>

<span data-ttu-id="e611f-114">列出 WMI VBScript 程式碼範例 [中的所有動態類別](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) 會使用限定詞 \_ 屬性來列出所有 WMI 動態類別 (包括根 \\ cimv2 命名空間中定義的關聯類別) 。</span><span class="sxs-lookup"><span data-stu-id="e611f-114">The [List All Dynamic Classes in WMI](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) VBScript code sample uses the Qualifier\_ property to list all WMI Dynamic classes (including Association classes) defined in the root\\cimv2 namespace.</span></span>

<span data-ttu-id="e611f-115">TechNet 元件庫上的 [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) PowerShell 程式碼範例會列出指定之命名空間中的所有可寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="e611f-115">The [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) PowerShell code sample on TechNet Gallery lists all writeable properties in the specified namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="e611f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e611f-116">Requirements</span></span>



| <span data-ttu-id="e611f-117">需求</span><span class="sxs-lookup"><span data-stu-id="e611f-117">Requirement</span></span> | <span data-ttu-id="e611f-118">值</span><span class="sxs-lookup"><span data-stu-id="e611f-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e611f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e611f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e611f-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e611f-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e611f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e611f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e611f-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e611f-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e611f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="e611f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e611f-124"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="e611f-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e611f-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e611f-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="e611f-126"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e611f-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e611f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e611f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e611f-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e611f-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e611f-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="e611f-129">CLSID</span></span><br/>                    | <span data-ttu-id="e611f-130">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="e611f-130">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="e611f-131">IID</span><span class="sxs-lookup"><span data-stu-id="e611f-131">IID</span></span><br/>                      | <span data-ttu-id="e611f-132">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="e611f-132">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




