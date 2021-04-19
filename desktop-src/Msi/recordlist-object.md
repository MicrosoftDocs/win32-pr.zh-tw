---
description: RecordList 物件是記錄物件的集合。 您必須確認 RecordList 物件存在，而且在參考其屬性之前不是空的。
ms.assetid: 7f5ac153-8da1-4dc8-9bb7-defd4e821142
title: RecordList 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b3f09887333d8ddbf83de4bea2b2e654411883e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991142"
---
# <a name="recordlist-object"></a><span data-ttu-id="c551e-104">RecordList 物件</span><span class="sxs-lookup"><span data-stu-id="c551e-104">RecordList object</span></span>

<span data-ttu-id="c551e-105">**RecordList** 物件是 [**記錄**](record-object.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="c551e-105">The **RecordList** object is a collection of [**Record**](record-object.md) objects.</span></span> <span data-ttu-id="c551e-106">您必須確認 **RecordList** 物件存在，而且在參考其屬性之前不是空的。</span><span class="sxs-lookup"><span data-stu-id="c551e-106">You must verify that the **RecordList** object exists and is not empty before referencing its properties.</span></span>

## <a name="members"></a><span data-ttu-id="c551e-107">成員</span><span class="sxs-lookup"><span data-stu-id="c551e-107">Members</span></span>

<span data-ttu-id="c551e-108">**RecordList** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c551e-108">The **RecordList** object has these types of members:</span></span>

-   [<span data-ttu-id="c551e-109">屬性</span><span class="sxs-lookup"><span data-stu-id="c551e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c551e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="c551e-110">Properties</span></span>

<span data-ttu-id="c551e-111">**RecordList** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c551e-111">The **RecordList** object has these properties.</span></span>



| <span data-ttu-id="c551e-112">屬性</span><span class="sxs-lookup"><span data-stu-id="c551e-112">Property</span></span>                                     | <span data-ttu-id="c551e-113">描述</span><span class="sxs-lookup"><span data-stu-id="c551e-113">Description</span></span>                                                          |
|:---------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="c551e-114">**計數**</span><span class="sxs-lookup"><span data-stu-id="c551e-114">**Count**</span></span>](recordlist-count.md)<br/> | <span data-ttu-id="c551e-115">傳回 **RecordList** 物件中的專案數。</span><span class="sxs-lookup"><span data-stu-id="c551e-115">Returns the number of items in the **RecordList** object.</span></span><br/> |
| [<span data-ttu-id="c551e-116">**項目**</span><span class="sxs-lookup"><span data-stu-id="c551e-116">**Item**</span></span>](recordlist-item.md)<br/>   | <span data-ttu-id="c551e-117">傳回 **RecordList** 物件集合中的記錄。</span><span class="sxs-lookup"><span data-stu-id="c551e-117">Returns a record in a **RecordList** object collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="c551e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c551e-118">Requirements</span></span>



| <span data-ttu-id="c551e-119">需求</span><span class="sxs-lookup"><span data-stu-id="c551e-119">Requirement</span></span> | <span data-ttu-id="c551e-120">值</span><span class="sxs-lookup"><span data-stu-id="c551e-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c551e-121">版本</span><span class="sxs-lookup"><span data-stu-id="c551e-121">Version</span></span><br/> | <span data-ttu-id="c551e-122">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="c551e-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c551e-123">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="c551e-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c551e-124">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="c551e-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c551e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c551e-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="c551e-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c551e-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c551e-127">IID</span><span class="sxs-lookup"><span data-stu-id="c551e-127">IID</span></span><br/>     | <span data-ttu-id="c551e-128">IID \_ IRecordList 定義為000C1096-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c551e-128">IID\_IRecordList is defined as 000C1096-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="c551e-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c551e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c551e-130">**Record**</span><span class="sxs-lookup"><span data-stu-id="c551e-130">**Record**</span></span>](record-object.md)
</dt> <dt>

[<span data-ttu-id="c551e-131">Windows Installer 腳本範例</span><span class="sxs-lookup"><span data-stu-id="c551e-131">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




