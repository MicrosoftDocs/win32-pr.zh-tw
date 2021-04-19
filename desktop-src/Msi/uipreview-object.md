---
description: UIPreview 物件是用來在撰寫期間，用來查看使用者介面對話方塊和公告欄。 此物件是由 Database 物件的 EnableUIPreview 方法所建立。
ms.assetid: 5df2a4f3-6352-4575-b822-1811150a86be
title: UIPreview 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6650dc9bcc66a24d0e8a9d7f0d971884a2379f60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995295"
---
# <a name="uipreview-object"></a><span data-ttu-id="864ab-104">UIPreview 物件</span><span class="sxs-lookup"><span data-stu-id="864ab-104">UIPreview object</span></span>

<span data-ttu-id="864ab-105">**UIPreview** 物件是用來在撰寫期間，用來查看使用者介面對話方塊和公告欄。</span><span class="sxs-lookup"><span data-stu-id="864ab-105">The **UIPreview** object is used to view user interface dialog boxes and billboards during authoring.</span></span> <span data-ttu-id="864ab-106">此物件是由 [**Database**](database-object.md)物件的 [**EnableUIPreview**](database-enableuipreview.md)方法所建立。</span><span class="sxs-lookup"><span data-stu-id="864ab-106">This object is created by the [**EnableUIPreview**](database-enableuipreview.md) method of the [**Database**](database-object.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="864ab-107">成員</span><span class="sxs-lookup"><span data-stu-id="864ab-107">Members</span></span>

<span data-ttu-id="864ab-108">**UIPreview** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="864ab-108">The **UIPreview** object has these types of members:</span></span>

-   [<span data-ttu-id="864ab-109">方法</span><span class="sxs-lookup"><span data-stu-id="864ab-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="864ab-110">屬性</span><span class="sxs-lookup"><span data-stu-id="864ab-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="864ab-111">方法</span><span class="sxs-lookup"><span data-stu-id="864ab-111">Methods</span></span>

<span data-ttu-id="864ab-112">**UIPreview** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="864ab-112">The **UIPreview** object has these methods.</span></span>



| <span data-ttu-id="864ab-113">方法</span><span class="sxs-lookup"><span data-stu-id="864ab-113">Method</span></span>                                           | <span data-ttu-id="864ab-114">描述</span><span class="sxs-lookup"><span data-stu-id="864ab-114">Description</span></span>                                                                                             |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="864ab-115">**ViewBillboard**</span><span class="sxs-lookup"><span data-stu-id="864ab-115">**ViewBillboard**</span></span>](uipreview-viewbillboard.md) | <span data-ttu-id="864ab-116">使用目前顯示之對話方塊中的主控制項，顯示撰寫的佈告欄。</span><span class="sxs-lookup"><span data-stu-id="864ab-116">Displays an authored billboard using the host control in the currently displayed dialog box.</span></span><br/> |
| [<span data-ttu-id="864ab-117">**ViewDialog**</span><span class="sxs-lookup"><span data-stu-id="864ab-117">**ViewDialog**</span></span>](uipreview-viewdialog.md)       | <span data-ttu-id="864ab-118">顯示儲存在目前資料庫中的撰寫 UI 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="864ab-118">Displays an authored UI dialog box stored in the current database.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="864ab-119">屬性</span><span class="sxs-lookup"><span data-stu-id="864ab-119">Properties</span></span>

<span data-ttu-id="864ab-120">**UIPreview** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="864ab-120">The **UIPreview** object has these properties.</span></span>



| <span data-ttu-id="864ab-121">屬性</span><span class="sxs-lookup"><span data-stu-id="864ab-121">Property</span></span>                                          | <span data-ttu-id="864ab-122">存取類型</span><span class="sxs-lookup"><span data-stu-id="864ab-122">Access type</span></span>           | <span data-ttu-id="864ab-123">Description</span><span class="sxs-lookup"><span data-stu-id="864ab-123">Description</span></span>                                                                                                                                                                       |
|:--------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="864ab-124">**屬性**</span><span class="sxs-lookup"><span data-stu-id="864ab-124">**Property**</span></span>](uipreview-property.md)<br/> | <span data-ttu-id="864ab-125">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="864ab-125">Read/write</span></span><br/> | <span data-ttu-id="864ab-126">表示指定之安裝程式屬性的字串值，如果前面加上百分比符號 (% ) ，則為目前進程的系統內容變數值。</span><span class="sxs-lookup"><span data-stu-id="864ab-126">Represents the string value of a named installer property or, if prefixed with a percent sign (%), the value of a system environment variable for the current process.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="864ab-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="864ab-127">Requirements</span></span>



| <span data-ttu-id="864ab-128">需求</span><span class="sxs-lookup"><span data-stu-id="864ab-128">Requirement</span></span> | <span data-ttu-id="864ab-129">值</span><span class="sxs-lookup"><span data-stu-id="864ab-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="864ab-130">版本</span><span class="sxs-lookup"><span data-stu-id="864ab-130">Version</span></span><br/> | <span data-ttu-id="864ab-131">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="864ab-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="864ab-132">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="864ab-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="864ab-133">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="864ab-133">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="864ab-134">DLL</span><span class="sxs-lookup"><span data-stu-id="864ab-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="864ab-135"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="864ab-135"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="864ab-136">IID</span><span class="sxs-lookup"><span data-stu-id="864ab-136">IID</span></span><br/>     | <span data-ttu-id="864ab-137">IID \_ IUIPreview 定義為 000C109A-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="864ab-137">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="864ab-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="864ab-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="864ab-139">Windows Installer 腳本範例</span><span class="sxs-lookup"><span data-stu-id="864ab-139">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




