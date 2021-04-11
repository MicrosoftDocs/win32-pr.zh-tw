---
description: Swbempropertyset 物件的 CIMType 屬性是一個整數，可用來判斷這個屬性的 CIM 型別。 這是唯讀的屬性。
ms.assetid: fb570ba4-6ce3-4131-8088-2761110033ba
ms.tgt_platform: multiple
title: 'Swbempropertyset. CIMType 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.CIMType
- ISWbemProperty.CIMType
- ISWbemProperty.get_CIMType
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 416101df1c3ae8542d3d2cd170b873407f007c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944400"
---
# <a name="swbempropertycimtype-property"></a><span data-ttu-id="5a5cc-104">Swbempropertyset. CIMType 屬性</span><span class="sxs-lookup"><span data-stu-id="5a5cc-104">SWbemProperty.CIMType property</span></span>

<span data-ttu-id="5a5cc-105">[**Swbempropertyset**](swbemproperty.md)物件的 **CIMType** 屬性是一個整數，可用來判斷這個屬性的 CIM 型別。</span><span class="sxs-lookup"><span data-stu-id="5a5cc-105">The **CIMType** property of the [**SWbemProperty**](swbemproperty.md) object is an integer that can be used to determine the CIM type of this property.</span></span> <span data-ttu-id="5a5cc-106">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="5a5cc-106">This property is read-only.</span></span>

<span data-ttu-id="5a5cc-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="5a5cc-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="5a5cc-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="5a5cc-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a5cc-109">語法</span><span class="sxs-lookup"><span data-stu-id="5a5cc-109">Syntax</span></span>


```VB
SWbemProperty.CIMType As Integer
```



## <a name="property-value"></a><span data-ttu-id="5a5cc-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="5a5cc-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="5a5cc-111">備註</span><span class="sxs-lookup"><span data-stu-id="5a5cc-111">Remarks</span></span>

<span data-ttu-id="5a5cc-112">如需這個屬性之有效類型的詳細資訊，請參閱 [**WbemCimtypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)。</span><span class="sxs-lookup"><span data-stu-id="5a5cc-112">For more information about valid types for this property, see [**WbemCimtypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span></span>

<span data-ttu-id="5a5cc-113">内嵌物件的實例會儲存在綜合物件中，做為 **CIM \_ 物件** 類型的屬性。</span><span class="sxs-lookup"><span data-stu-id="5a5cc-113">Instances of embedded objects are stored in composite objects as properties of type **CIM\_OBJECT**.</span></span> <span data-ttu-id="5a5cc-114">若要在複合類別的實例中判斷内嵌物件的類別，您必須檢查 **CIM \_ 物件** 類型屬性的 **CIMType** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="5a5cc-114">To determine the class of an embedded object in an instance of a composite class, you must examine the **CIMType** qualifier of the **CIM\_OBJECT** type property.</span></span>

<span data-ttu-id="5a5cc-115">關聯類別中的物件參考會儲存在 **CIM \_ 參考** 類型的屬性中。</span><span class="sxs-lookup"><span data-stu-id="5a5cc-115">The object references in an association class are stored in properties of type **CIM\_REFERENCE**.</span></span> <span data-ttu-id="5a5cc-116">若要判斷實際的物件路徑，您必須檢查 **CIM \_ 參考** 型別屬性的 **CIMType** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="5a5cc-116">To determine the actual object paths you must examine the **CIMType** qualifier of the **CIM\_REFERENCE** type property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a5cc-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a5cc-117">Requirements</span></span>



| <span data-ttu-id="5a5cc-118">需求</span><span class="sxs-lookup"><span data-stu-id="5a5cc-118">Requirement</span></span> | <span data-ttu-id="5a5cc-119">值</span><span class="sxs-lookup"><span data-stu-id="5a5cc-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a5cc-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a5cc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5a5cc-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a5cc-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5a5cc-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a5cc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5a5cc-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a5cc-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5a5cc-124">標頭</span><span class="sxs-lookup"><span data-stu-id="5a5cc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a5cc-125"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="5a5cc-125"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a5cc-126">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5a5cc-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="5a5cc-127"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5a5cc-127"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5a5cc-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5a5cc-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a5cc-129"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a5cc-129"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5a5cc-130">CLSID</span><span class="sxs-lookup"><span data-stu-id="5a5cc-130">CLSID</span></span><br/>                    | <span data-ttu-id="5a5cc-131">CLSID \_ swbempropertyset</span><span class="sxs-lookup"><span data-stu-id="5a5cc-131">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="5a5cc-132">IID</span><span class="sxs-lookup"><span data-stu-id="5a5cc-132">IID</span></span><br/>                      | <span data-ttu-id="5a5cc-133">IID \_ ISWbemProperty</span><span class="sxs-lookup"><span data-stu-id="5a5cc-133">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




