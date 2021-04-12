---
description: Swbempropertyset 物件的 [原始] 屬性會抓取引入這個屬性之 WMI 類別的名稱。 針對具有深度繼承階層的類別，通常需要知道哪些屬性已在哪些類別中宣告。
ms.assetid: 25bc0303-43b8-42da-a194-82213c1009d9
ms.tgt_platform: multiple
title: 'Swbempropertyset：屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.Origin
- ISWbemProperty.Origin
- ISWbemProperty.get_Origin
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f0aef6c1041e14d65ee3cbacaa40255421a1b064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193061"
---
# <a name="swbempropertyorigin-property"></a><span data-ttu-id="9053e-104">Swbempropertyset 屬性</span><span class="sxs-lookup"><span data-stu-id="9053e-104">SWbemProperty.Origin property</span></span>

<span data-ttu-id="9053e-105">[**Swbempropertyset**](swbemproperty.md)物件的 [**原始**] 屬性會抓取引入這個屬性之 WMI 類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="9053e-105">The **Origin** property of the [**SWbemProperty**](swbemproperty.md) object retrieves the name of the WMI class in which this property was introduced.</span></span> <span data-ttu-id="9053e-106">針對具有深度繼承階層的類別，通常需要知道哪些屬性已在哪些類別中宣告。</span><span class="sxs-lookup"><span data-stu-id="9053e-106">For classes with deep inheritance hierarchies, it is often desirable to know which properties were declared in which classes.</span></span>

<span data-ttu-id="9053e-107">如果屬性為 local (請參閱 [**SWbemQualifier. IsLocal**](swbemqualifier-islocal.md)) ，此值與擁有類別相同。</span><span class="sxs-lookup"><span data-stu-id="9053e-107">If the property is local (see [**SWbemQualifier.IsLocal**](swbemqualifier-islocal.md)), this value is the same as the owning class.</span></span> <span data-ttu-id="9053e-108">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="9053e-108">This property is read-only.</span></span>

<span data-ttu-id="9053e-109">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="9053e-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="9053e-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="9053e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9053e-111">語法</span><span class="sxs-lookup"><span data-stu-id="9053e-111">Syntax</span></span>


```VB
SWbemProperty.Origin As String
```



## <a name="property-value"></a><span data-ttu-id="9053e-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="9053e-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="9053e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9053e-113">Requirements</span></span>



| <span data-ttu-id="9053e-114">需求</span><span class="sxs-lookup"><span data-stu-id="9053e-114">Requirement</span></span> | <span data-ttu-id="9053e-115">值</span><span class="sxs-lookup"><span data-stu-id="9053e-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9053e-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9053e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9053e-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9053e-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9053e-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9053e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9053e-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9053e-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9053e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="9053e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9053e-121"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="9053e-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9053e-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9053e-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="9053e-123"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9053e-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9053e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9053e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9053e-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9053e-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9053e-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="9053e-126">CLSID</span></span><br/>                    | <span data-ttu-id="9053e-127">CLSID \_ swbempropertyset</span><span class="sxs-lookup"><span data-stu-id="9053e-127">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="9053e-128">IID</span><span class="sxs-lookup"><span data-stu-id="9053e-128">IID</span></span><br/>                      | <span data-ttu-id="9053e-129">IID \_ ISWbemProperty</span><span class="sxs-lookup"><span data-stu-id="9053e-129">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




