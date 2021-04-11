---
description: SWbemNamedValue 物件的 Value 屬性會傳回 SWbemNamedValue 專案的變異值。
ms.assetid: f9609bd2-893a-48c3-9faa-93cd033c4109
ms.tgt_platform: multiple
title: 'SWbemNamedValue： Value 屬性 (>wbemdisp.tlb. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValue.Value
- ISWbemNamedValue.Value
- ISWbemNamedValue.get_Value
- ISWbemNamedValue.put_Value
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4bf63b15a27c1149341200f29e938bdba6cd7bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114872"
---
# <a name="swbemnamedvaluevalue-property"></a><span data-ttu-id="c332e-103">SWbemNamedValue。 Value 屬性</span><span class="sxs-lookup"><span data-stu-id="c332e-103">SWbemNamedValue.Value property</span></span>

<span data-ttu-id="c332e-104">[**SWbemNamedValue**](swbemnamedvalue.md)物件的 **Value** 屬性會傳回 **SWbemNamedValue** 專案的變異值。</span><span class="sxs-lookup"><span data-stu-id="c332e-104">The **Value** property of the [**SWbemNamedValue**](swbemnamedvalue.md) object returns the variant value of an **SWbemNamedValue** item.</span></span> <span data-ttu-id="c332e-105">這是 **SWbemNamedValue** 物件的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="c332e-105">This is the default property for **SWbemNamedValue** objects.</span></span> <span data-ttu-id="c332e-106">對 value 屬性所做的變更會自動反映在 **SWbemNamedValue** 物件所屬的 [**SWbemNamedValueSet**](swbemnamedvalueset.md)集合中。</span><span class="sxs-lookup"><span data-stu-id="c332e-106">Changes made to the value property are reflected automatically in the [**SWbemNamedValueSet**](swbemnamedvalueset.md) collection to which the **SWbemNamedValue** object belongs.</span></span>

<span data-ttu-id="c332e-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="c332e-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="c332e-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="c332e-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c332e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c332e-109">Syntax</span></span>


```VB
SWbemNamedValue.Value As Variant
```



## <a name="property-value"></a><span data-ttu-id="c332e-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="c332e-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="c332e-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="c332e-111">Requirements</span></span>



| <span data-ttu-id="c332e-112">需求</span><span class="sxs-lookup"><span data-stu-id="c332e-112">Requirement</span></span> | <span data-ttu-id="c332e-113">值</span><span class="sxs-lookup"><span data-stu-id="c332e-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c332e-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c332e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c332e-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c332e-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c332e-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c332e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c332e-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c332e-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c332e-118">標頭</span><span class="sxs-lookup"><span data-stu-id="c332e-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c332e-119"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="c332e-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c332e-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c332e-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="c332e-121"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c332e-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c332e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c332e-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c332e-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c332e-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c332e-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="c332e-124">CLSID</span></span><br/>                    | <span data-ttu-id="c332e-125">CLSID \_ SWbemNamedValue</span><span class="sxs-lookup"><span data-stu-id="c332e-125">CLSID\_SWbemNamedValue</span></span><br/>                                                       |
| <span data-ttu-id="c332e-126">IID</span><span class="sxs-lookup"><span data-stu-id="c332e-126">IID</span></span><br/>                      | <span data-ttu-id="c332e-127">IID \_ ISWbemNamedValue</span><span class="sxs-lookup"><span data-stu-id="c332e-127">IID\_ISWbemNamedValue</span></span><br/>                                                        |



 

 




