---
description: Swbempropertyset 物件的 IsLocal 屬性是一個布林值，可用來判斷這個屬性是否為本機。 值為 FALSE 表示這個屬性已經繼承自另一個類別。 這是唯讀的屬性。
ms.assetid: eda1f962-03b5-4322-bb06-c27aedf94be1
ms.tgt_platform: multiple
title: 'Swbempropertyset. IsLocal 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.IsLocal
- ISWbemProperty.IsLocal
- ISWbemProperty.get_IsLocal
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 187613a0111c7ad482c55e3d294d77fddb5b0941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849560"
---
# <a name="swbempropertyislocal-property"></a><span data-ttu-id="67915-105">Swbempropertyset. IsLocal 屬性</span><span class="sxs-lookup"><span data-stu-id="67915-105">SWbemProperty.IsLocal property</span></span>

<span data-ttu-id="67915-106">[**Swbempropertyset**](swbemproperty.md)物件的 **IsLocal** 屬性是一個布林值，可用來判斷這個屬性是否為本機。</span><span class="sxs-lookup"><span data-stu-id="67915-106">The **IsLocal** property of the [**SWbemProperty**](swbemproperty.md) object is a Boolean value that can be used to determine if this property is local.</span></span> <span data-ttu-id="67915-107">值為 **FALSE** 表示這個屬性已經繼承自另一個類別。</span><span class="sxs-lookup"><span data-stu-id="67915-107">A value of **FALSE** indicates that this property has been inherited from another class.</span></span> <span data-ttu-id="67915-108">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="67915-108">This property is read-only.</span></span>

<span data-ttu-id="67915-109">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="67915-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="67915-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="67915-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="67915-111">語法</span><span class="sxs-lookup"><span data-stu-id="67915-111">Syntax</span></span>


```VB
SWbemProperty.IsLocal As Boolean
```



## <a name="property-value"></a><span data-ttu-id="67915-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="67915-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="67915-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="67915-113">Requirements</span></span>



| <span data-ttu-id="67915-114">需求</span><span class="sxs-lookup"><span data-stu-id="67915-114">Requirement</span></span> | <span data-ttu-id="67915-115">值</span><span class="sxs-lookup"><span data-stu-id="67915-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67915-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67915-116">Minimum supported client</span></span><br/> | <span data-ttu-id="67915-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67915-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="67915-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67915-118">Minimum supported server</span></span><br/> | <span data-ttu-id="67915-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67915-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="67915-120">標頭</span><span class="sxs-lookup"><span data-stu-id="67915-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="67915-121"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="67915-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="67915-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="67915-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="67915-123"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="67915-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="67915-124">DLL</span><span class="sxs-lookup"><span data-stu-id="67915-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67915-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67915-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="67915-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="67915-126">CLSID</span></span><br/>                    | <span data-ttu-id="67915-127">CLSID \_ swbempropertyset</span><span class="sxs-lookup"><span data-stu-id="67915-127">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="67915-128">IID</span><span class="sxs-lookup"><span data-stu-id="67915-128">IID</span></span><br/>                      | <span data-ttu-id="67915-129">IID \_ ISWbemProperty</span><span class="sxs-lookup"><span data-stu-id="67915-129">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




