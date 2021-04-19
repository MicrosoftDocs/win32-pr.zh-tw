---
description: 唯讀 RelatedProducts 屬性會傳回 StringList 物件，以列舉其屬性工作表中具有指定 UpgradeCode 屬性之目前使用者和電腦的所有已安裝或公告的產品集合。
ms.assetid: 0316e536-ccd4-4d7a-9c49-66e6c4a07f1c
title: RelatedProducts 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RelatedProducts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fb30be6ea5250a90ef8aa18065e9be679946e503
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978473"
---
# <a name="installerrelatedproducts-property"></a><span data-ttu-id="15f62-103">RelatedProducts 屬性</span><span class="sxs-lookup"><span data-stu-id="15f62-103">Installer.RelatedProducts property</span></span>

<span data-ttu-id="15f62-104">唯讀 **RelatedProducts** 屬性會傳回 [**StringList**](stringlist-object.md)物件，以列舉其 [屬性工作表](property-table.md)中具有指定 [**UpgradeCode**](upgradecode.md)屬性之目前使用者和電腦的所有已安裝或公告的產品集合。</span><span class="sxs-lookup"><span data-stu-id="15f62-104">The read-only **RelatedProducts** property returns a [**StringList**](stringlist-object.md) object enumerating the set of all products installed or advertised for the current user and machine with a specified [**UpgradeCode**](upgradecode.md) property in their [Property table](property-table.md).</span></span>

<span data-ttu-id="15f62-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="15f62-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="15f62-106">語法</span><span class="sxs-lookup"><span data-stu-id="15f62-106">Syntax</span></span>


```JScript
propVal = Installer.RelatedProducts
```



## <a name="property-value"></a><span data-ttu-id="15f62-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="15f62-107">Property value</span></span>

<span data-ttu-id="15f62-108">安裝程式所列舉之相關產品的升級程式碼。</span><span class="sxs-lookup"><span data-stu-id="15f62-108">The upgrade code of related products that the installer enumerates.</span></span>

## <a name="remarks"></a><span data-ttu-id="15f62-109">備註</span><span class="sxs-lookup"><span data-stu-id="15f62-109">Remarks</span></span>

<span data-ttu-id="15f62-110">若要列舉相關的產品，應用程式會使用 For Each 結構逐一查看 [**StringList**](stringlist-object.md) 。</span><span class="sxs-lookup"><span data-stu-id="15f62-110">To enumerate the related products, an application iterates through the [**StringList**](stringlist-object.md) using a For Each construct.</span></span> <span data-ttu-id="15f62-111">由於相關產品未排序，因此任何新的相關產品都有任意的索引。</span><span class="sxs-lookup"><span data-stu-id="15f62-111">Because related products are not ordered, any new related product has an arbitrary index.</span></span> <span data-ttu-id="15f62-112">這表示函數可以依任何順序傳回相關的產品。</span><span class="sxs-lookup"><span data-stu-id="15f62-112">This means that the function can return related products in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="15f62-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="15f62-113">Requirements</span></span>



| <span data-ttu-id="15f62-114">需求</span><span class="sxs-lookup"><span data-stu-id="15f62-114">Requirement</span></span> | <span data-ttu-id="15f62-115">值</span><span class="sxs-lookup"><span data-stu-id="15f62-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15f62-116">版本</span><span class="sxs-lookup"><span data-stu-id="15f62-116">Version</span></span><br/> | <span data-ttu-id="15f62-117">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="15f62-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="15f62-118">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="15f62-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="15f62-119">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="15f62-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="15f62-120">DLL</span><span class="sxs-lookup"><span data-stu-id="15f62-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="15f62-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15f62-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="15f62-122">IID</span><span class="sxs-lookup"><span data-stu-id="15f62-122">IID</span></span><br/>     | <span data-ttu-id="15f62-123">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="15f62-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="15f62-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15f62-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15f62-125">**MsiEnumRelatedProducts**</span><span class="sxs-lookup"><span data-stu-id="15f62-125">**MsiEnumRelatedProducts**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)
</dt> </dl>

 

 




