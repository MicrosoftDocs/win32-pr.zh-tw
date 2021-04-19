---
description: Products 屬性是唯讀屬性，它會傳回 StringList 物件，以列舉針對目前使用者和電腦安裝或公告的所有產品集。
ms.assetid: 5c210827-a7cc-4358-bfe6-4d8e9767bd8c
title: 安裝程式. Products 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Products
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8d5b20a770154382e7e7a68cc3fe4d81c350fb1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992930"
---
# <a name="installerproducts-property"></a><span data-ttu-id="210ad-103">安裝程式. Products 屬性</span><span class="sxs-lookup"><span data-stu-id="210ad-103">Installer.Products property</span></span>

<span data-ttu-id="210ad-104">**Products** 屬性是唯讀屬性，它會傳回 [**StringList**](stringlist-object.md)物件，以列舉針對目前使用者和電腦安裝或公告的所有產品集。</span><span class="sxs-lookup"><span data-stu-id="210ad-104">The **Products** property is a read-only property that returns a [**StringList**](stringlist-object.md) object enumerating the set of all products installed or advertised for the current user and machine.</span></span>

<span data-ttu-id="210ad-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="210ad-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="210ad-106">語法</span><span class="sxs-lookup"><span data-stu-id="210ad-106">Syntax</span></span>


```JScript
propVal = Installer.Products
```



## <a name="property-value"></a><span data-ttu-id="210ad-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="210ad-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="210ad-108">備註</span><span class="sxs-lookup"><span data-stu-id="210ad-108">Remarks</span></span>

<span data-ttu-id="210ad-109">若要列舉產品，應用程式會使用 For Each 結構逐一查看 [**StringList**](stringlist-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="210ad-109">To enumerate the products, an application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="210ad-110">由於產品未排序，因此任何新產品都有任意的索引。</span><span class="sxs-lookup"><span data-stu-id="210ad-110">Because products are not ordered, any new product has an arbitrary index.</span></span> <span data-ttu-id="210ad-111">這表示函數可以依任何順序傳回產品。</span><span class="sxs-lookup"><span data-stu-id="210ad-111">This means that the function can return products in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="210ad-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="210ad-112">Requirements</span></span>



| <span data-ttu-id="210ad-113">需求</span><span class="sxs-lookup"><span data-stu-id="210ad-113">Requirement</span></span> | <span data-ttu-id="210ad-114">值</span><span class="sxs-lookup"><span data-stu-id="210ad-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="210ad-115">版本</span><span class="sxs-lookup"><span data-stu-id="210ad-115">Version</span></span><br/> | <span data-ttu-id="210ad-116">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="210ad-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="210ad-117">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="210ad-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="210ad-118">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="210ad-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="210ad-119">DLL</span><span class="sxs-lookup"><span data-stu-id="210ad-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="210ad-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="210ad-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="210ad-121">IID</span><span class="sxs-lookup"><span data-stu-id="210ad-121">IID</span></span><br/>     | <span data-ttu-id="210ad-122">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="210ad-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="210ad-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="210ad-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="210ad-124">**MsiEnumProducts**</span><span class="sxs-lookup"><span data-stu-id="210ad-124">**MsiEnumProducts**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> </dl>

 

 




