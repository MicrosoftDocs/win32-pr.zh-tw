---
description: StringList 物件是字串的集合。 用戶端必須確認 StringList 物件存在，而且在參考其屬性之前不是空的。
ms.assetid: 7021320a-d01a-43e8-90a5-6105a11a4613
title: StringList 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6493b9e1723d46ce290c7472bbcee7eb9ec34725
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993346"
---
# <a name="stringlist-object"></a><span data-ttu-id="2b69b-104">StringList 物件</span><span class="sxs-lookup"><span data-stu-id="2b69b-104">StringList object</span></span>

<span data-ttu-id="2b69b-105">**StringList** 物件是字串的集合。</span><span class="sxs-lookup"><span data-stu-id="2b69b-105">The **StringList** object is a collection of strings.</span></span> <span data-ttu-id="2b69b-106">用戶端必須確認 **StringList** 物件存在，而且在參考其屬性之前不是空的。</span><span class="sxs-lookup"><span data-stu-id="2b69b-106">The client must verify that the **StringList** object exists and is not empty before referencing its properties.</span></span>

## <a name="members"></a><span data-ttu-id="2b69b-107">成員</span><span class="sxs-lookup"><span data-stu-id="2b69b-107">Members</span></span>

<span data-ttu-id="2b69b-108">**StringList** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2b69b-108">The **StringList** object has these types of members:</span></span>

-   [<span data-ttu-id="2b69b-109">屬性</span><span class="sxs-lookup"><span data-stu-id="2b69b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b69b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="2b69b-110">Properties</span></span>

<span data-ttu-id="2b69b-111">**StringList** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2b69b-111">The **StringList** object has these properties.</span></span>



| <span data-ttu-id="2b69b-112">屬性</span><span class="sxs-lookup"><span data-stu-id="2b69b-112">Property</span></span>                                     | <span data-ttu-id="2b69b-113">描述</span><span class="sxs-lookup"><span data-stu-id="2b69b-113">Description</span></span>                                                          |
|:---------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="2b69b-114">**計數**</span><span class="sxs-lookup"><span data-stu-id="2b69b-114">**Count**</span></span>](stringlist-count.md)<br/> | <span data-ttu-id="2b69b-115">傳回 **StringList** 物件中的專案數。</span><span class="sxs-lookup"><span data-stu-id="2b69b-115">Returns the number of items in the **StringList** object.</span></span><br/> |
| [<span data-ttu-id="2b69b-116">**項目**</span><span class="sxs-lookup"><span data-stu-id="2b69b-116">**Item**</span></span>](stringlist-item.md)<br/>   | <span data-ttu-id="2b69b-117">傳回 **StringList** 物件集合中的字串。</span><span class="sxs-lookup"><span data-stu-id="2b69b-117">Returns a string in the **StringList** object collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2b69b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b69b-118">Requirements</span></span>



| <span data-ttu-id="2b69b-119">需求</span><span class="sxs-lookup"><span data-stu-id="2b69b-119">Requirement</span></span> | <span data-ttu-id="2b69b-120">值</span><span class="sxs-lookup"><span data-stu-id="2b69b-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b69b-121">版本</span><span class="sxs-lookup"><span data-stu-id="2b69b-121">Version</span></span><br/> | <span data-ttu-id="2b69b-122">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="2b69b-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2b69b-123">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="2b69b-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2b69b-124">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b69b-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="2b69b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2b69b-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="2b69b-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b69b-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="2b69b-127">IID</span><span class="sxs-lookup"><span data-stu-id="2b69b-127">IID</span></span><br/>     | <span data-ttu-id="2b69b-128">IID \_ IStringList 定義為000C1095-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2b69b-128">IID\_IStringList is defined as 000C1095-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="2b69b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b69b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b69b-130">Windows Installer 腳本範例</span><span class="sxs-lookup"><span data-stu-id="2b69b-130">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




