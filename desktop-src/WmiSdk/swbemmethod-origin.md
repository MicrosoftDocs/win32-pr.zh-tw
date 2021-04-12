---
description: SWbemMethod 物件的原始屬性會傳回這個方法引進的類別名稱。
ms.assetid: da98393b-af95-47ad-b589-663063f65afb
ms.tgt_platform: multiple
title: 'SWbemMethod：屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.Origin
- ISWbemMethod.Origin
- ISWbemMethod.get_Origin
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c1b903a2c55bbd571a9cd1f36a51812a70c123cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192067"
---
# <a name="swbemmethodorigin-property"></a><span data-ttu-id="83fa0-103">SWbemMethod 屬性</span><span class="sxs-lookup"><span data-stu-id="83fa0-103">SWbemMethod.Origin property</span></span>

<span data-ttu-id="83fa0-104">[**SWbemMethod**](swbemmethod.md)物件的 **原始** 屬性會傳回這個方法引進的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="83fa0-104">The **Origin** property of the [**SWbemMethod**](swbemmethod.md) object returns the name of the class in which this method was introduced.</span></span> <span data-ttu-id="83fa0-105">針對具有深度繼承階層的類別，通常需要知道哪些方法已在哪些類別中宣告。</span><span class="sxs-lookup"><span data-stu-id="83fa0-105">For classes with deep inheritance hierarchies, it is often desirable to know which methods were declared in which classes.</span></span> <span data-ttu-id="83fa0-106">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="83fa0-106">This property is read-only.</span></span>

<span data-ttu-id="83fa0-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="83fa0-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="83fa0-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="83fa0-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="83fa0-109">語法</span><span class="sxs-lookup"><span data-stu-id="83fa0-109">Syntax</span></span>


```VB
SWbemMethod.Origin As String
```



## <a name="property-value"></a><span data-ttu-id="83fa0-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="83fa0-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="83fa0-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="83fa0-111">Requirements</span></span>



| <span data-ttu-id="83fa0-112">需求</span><span class="sxs-lookup"><span data-stu-id="83fa0-112">Requirement</span></span> | <span data-ttu-id="83fa0-113">值</span><span class="sxs-lookup"><span data-stu-id="83fa0-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83fa0-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="83fa0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="83fa0-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83fa0-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="83fa0-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="83fa0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="83fa0-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83fa0-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="83fa0-118">標頭</span><span class="sxs-lookup"><span data-stu-id="83fa0-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="83fa0-119"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="83fa0-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="83fa0-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="83fa0-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="83fa0-121"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="83fa0-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="83fa0-122">DLL</span><span class="sxs-lookup"><span data-stu-id="83fa0-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83fa0-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83fa0-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="83fa0-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="83fa0-124">CLSID</span></span><br/>                    | <span data-ttu-id="83fa0-125">CLSID \_ SWbemMethod</span><span class="sxs-lookup"><span data-stu-id="83fa0-125">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="83fa0-126">IID</span><span class="sxs-lookup"><span data-stu-id="83fa0-126">IID</span></span><br/>                      | <span data-ttu-id="83fa0-127">IID \_ ISWbemMethod</span><span class="sxs-lookup"><span data-stu-id="83fa0-127">IID\_ISWbemMethod</span></span><br/>                                                            |



 

 




