---
description: 若為安裝套件，[修訂編號摘要] 屬性會包含安裝程式套件的封裝程式碼。
ms.assetid: 79702b44-846a-4672-8e22-9b6e3f4b4678
title: 修訂編號摘要屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e97df1eafec2d543be0f975b9f5daca7728267b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984836"
---
# <a name="revision-number-summary-property"></a><span data-ttu-id="a26b6-103">修訂編號摘要屬性</span><span class="sxs-lookup"><span data-stu-id="a26b6-103">Revision Number Summary property</span></span>

<span data-ttu-id="a26b6-104">若為安裝套件，[ **修訂編號摘要** ] 屬性會包含安裝程式套件的 [*封裝程式碼*](p-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="a26b6-104">For an installation package, the **Revision Number Summary** property contains the [*package code*](p-gly.md) for the installer package.</span></span> <span data-ttu-id="a26b6-105">如需封裝程式碼的詳細資訊，請參閱 [封裝程式碼](package-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="a26b6-105">For more information about package codes, see [Package Codes](package-codes.md).</span></span>

<span data-ttu-id="a26b6-106">針對轉換，[ **修訂編號摘要** ] 屬性會列出產品程式碼 guid 和版本的新的和原始產品以及升級程式碼 GUID。</span><span class="sxs-lookup"><span data-stu-id="a26b6-106">For a transform, the **Revision Number Summary** property lists the product code GUIDs and version of the new and original products and the upgrade code GUID.</span></span> <span data-ttu-id="a26b6-107">清單會以分號分隔，如下所示。</span><span class="sxs-lookup"><span data-stu-id="a26b6-107">The list is separated with semicolons as follows.</span></span>

<span data-ttu-id="a26b6-108">「原始產品-程式碼原始產品版本;New-Product 程式碼新產品版本;Upgrade-Code "</span><span class="sxs-lookup"><span data-stu-id="a26b6-108">"Original-Product-Code Original-Product-Version ; New-Product Code New-Product-Version; Upgrade-Code"</span></span>

<span data-ttu-id="a26b6-109">針對 patch 封裝，[ **修訂編號摘要** ] 屬性會指定修補程式的 GUID 修補程式碼。</span><span class="sxs-lookup"><span data-stu-id="a26b6-109">For a patch package, the **Revision Number Summary** property specifies the GUID patch code for the patch.</span></span> <span data-ttu-id="a26b6-110">這可以緊接著套用此修補程式時要移除之過時修補程式的修補程式程式碼 Guid 清單。</span><span class="sxs-lookup"><span data-stu-id="a26b6-110">This can be followed by a list of patch code GUIDs for obsolete patches that are to be removed when this patch is applied.</span></span> <span data-ttu-id="a26b6-111">系統會串連修補程式碼，而不使用分隔符號分隔清單中的 Guid。</span><span class="sxs-lookup"><span data-stu-id="a26b6-111">The patch codes are concatenated with no delimiters separating GUIDs in the list.</span></span>

<span data-ttu-id="a26b6-112">\* \* Windows Installer 3.0： \* \* 如果 [MsiPatchSequence 資料表](msipatchsequence-table.md)中有排序資訊，Windows Installer 3.0 會使用資料表中的排序資訊，並忽略 **修訂編號摘要** 屬性中包含的過時修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="a26b6-112">\*\*Windows Installer 3.0:  \*\* If there is sequencing information present in the [MsiPatchSequence table](msipatchsequence-table.md), Windows Installer 3.0 uses the sequencing information in the table and ignores the list of obsolete patches included in the **Revision Number Summary** property.</span></span> <span data-ttu-id="a26b6-113">如果封裝未包含 MsiPatchSequence 資料表，則 Windows Installer 3.0 仍可使用 [ **修訂編號摘要** ] 屬性中的過時修補程式資訊。</span><span class="sxs-lookup"><span data-stu-id="a26b6-113">Windows Installer 3.0 can still use the obsolete patch information in the **Revision Number Summary** property if the package does not contain a MsiPatchSequence table.</span></span>

<span data-ttu-id="a26b6-114">\* \* Windows Installer 2.0： \* \* 不支援 [MsiPatchSequence 資料表](msipatchsequence-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="a26b6-114">\*\*Windows Installer 2.0:  \*\* The [MsiPatchSequence table](msipatchsequence-table.md) is not supported.</span></span> <span data-ttu-id="a26b6-115">如果封裝未包含 MsiPatchSequence 資料表，則 Windows Installer 2.0 仍可使用 [ **修訂編號摘要** ] 屬性中的過時修補程式資訊。</span><span class="sxs-lookup"><span data-stu-id="a26b6-115">Windows Installer 2.0 can still use the obsolete patch information in the **Revision Number Summary** property if the package does not contain a MsiPatchSequence table.</span></span>

<span data-ttu-id="a26b6-116">這是必要的摘要屬性。</span><span class="sxs-lookup"><span data-stu-id="a26b6-116">This summary property is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="a26b6-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a26b6-117">Requirements</span></span>



| <span data-ttu-id="a26b6-118">需求</span><span class="sxs-lookup"><span data-stu-id="a26b6-118">Requirement</span></span> | <span data-ttu-id="a26b6-119">值</span><span class="sxs-lookup"><span data-stu-id="a26b6-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a26b6-120">版本</span><span class="sxs-lookup"><span data-stu-id="a26b6-120">Version</span></span><br/> | <span data-ttu-id="a26b6-121">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="a26b6-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a26b6-122">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="a26b6-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a26b6-123">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="a26b6-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a26b6-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a26b6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a26b6-125">摘要屬性描述</span><span class="sxs-lookup"><span data-stu-id="a26b6-125">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




