---
description: 安裝程式會將 [上次儲存的摘要] 屬性設定為值，取決於這是否為安裝套件、轉換或修補套件。在安裝套件中，安裝程式會在系統管理安裝期間，將此屬性設定為 [LogonUser] 屬性的值。 資料庫編輯工具的開發人員可能會在開發程式中使用這個屬性，來追蹤最後一個修改安裝資料庫的人員。 在最後的出貨資料庫中，這個屬性應該設定為 Null。 安裝程式永遠不會使用這個屬性，而且使用者永遠不需要修改它。在轉換中，此摘要屬性包含資料庫在轉換之後應該具有的平臺和語言識別項 (s) 。 屬性會指定要在新資料庫中設定範本摘要的內容。在 patch 封裝中，此摘要屬性包含以分號分隔的轉換 substorage 名稱清單（依此修補程式套用的順序）。
ms.assetid: 6da171d9-29db-4524-abc6-77db8fbfca38
title: 上次儲存的摘要屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dfd1c00863eee3bc31728783042ada8298b2067
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999375"
---
# <a name="last-saved-by-summary-property"></a><span data-ttu-id="d82c7-107">上次儲存的摘要屬性</span><span class="sxs-lookup"><span data-stu-id="d82c7-107">Last Saved By Summary property</span></span>

<span data-ttu-id="d82c7-108">安裝程式會將 [ **上次儲存的摘要** ] 屬性設定為值，取決於這是否為安裝套件、轉換或修補套件。</span><span class="sxs-lookup"><span data-stu-id="d82c7-108">The installer sets the **Last Saved by Summary** Property to a value that depends on whether this is an installation package, transform, or patch package.</span></span>

<span data-ttu-id="d82c7-109">在安裝套件中，安裝程式會在系統 [管理安裝](administrative-installation.md)期間，將此屬性設定為 [ [**LogonUser**](logonuser.md) ] 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="d82c7-109">In an installation package, the installer sets this property to the value of the [**LogonUser**](logonuser.md) property during an [administrative installation](administrative-installation.md).</span></span> <span data-ttu-id="d82c7-110">資料庫編輯工具的開發人員可能會在開發程式中使用這個屬性，來追蹤最後一個修改安裝資料庫的人員。</span><span class="sxs-lookup"><span data-stu-id="d82c7-110">Developers of database editing tools may use this property during the development process to track the last person to modify the installation database.</span></span> <span data-ttu-id="d82c7-111">在最後的出貨資料庫中，這個屬性應該設定為 Null。</span><span class="sxs-lookup"><span data-stu-id="d82c7-111">This property should be set to Null in a final shipping database.</span></span> <span data-ttu-id="d82c7-112">安裝程式永遠不會使用這個屬性，而且使用者永遠不需要修改它。</span><span class="sxs-lookup"><span data-stu-id="d82c7-112">The installer never uses this property and a user never needs to modify it.</span></span>

<span data-ttu-id="d82c7-113">在轉換中，此摘要屬性包含資料庫在轉換之後應該具有的平臺和語言識別項 (s) 。</span><span class="sxs-lookup"><span data-stu-id="d82c7-113">In a transform, this summary property contains the platform and language ID(s) that a database should have after it has been transformed.</span></span> <span data-ttu-id="d82c7-114">屬性會指定要在新資料庫中設定 [**範本摘要**](template-summary.md) 的內容。</span><span class="sxs-lookup"><span data-stu-id="d82c7-114">The property specifies to what the [**Template Summary**](template-summary.md) should be set in the new database.</span></span>

<span data-ttu-id="d82c7-115">在 patch 封裝中，此摘要屬性包含以分號分隔的轉換 substorage 名稱清單（依此修補程式套用的順序）。</span><span class="sxs-lookup"><span data-stu-id="d82c7-115">In a patch package, this summary property contains a semicolon-delimited list of transform substorage names in the order they are applied by this patch.</span></span>

## <a name="requirements"></a><span data-ttu-id="d82c7-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d82c7-116">Requirements</span></span>



| <span data-ttu-id="d82c7-117">需求</span><span class="sxs-lookup"><span data-stu-id="d82c7-117">Requirement</span></span> | <span data-ttu-id="d82c7-118">值</span><span class="sxs-lookup"><span data-stu-id="d82c7-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d82c7-119">版本</span><span class="sxs-lookup"><span data-stu-id="d82c7-119">Version</span></span><br/> | <span data-ttu-id="d82c7-120">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="d82c7-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d82c7-121">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="d82c7-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d82c7-122">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d82c7-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d82c7-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d82c7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d82c7-124">摘要屬性描述</span><span class="sxs-lookup"><span data-stu-id="d82c7-124">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




