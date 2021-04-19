---
description: Features 屬性是唯讀屬性，它會傳回 StringList 物件，以列舉指定產品的已發行功能集。
ms.assetid: feb8f09a-fa97-4fee-9082-8f04288af22f
title: 安裝程式。 Features 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Features
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4f63ce80249fb8bd24d70f92e72c44420a13d798
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986591"
---
# <a name="installerfeatures-property"></a><span data-ttu-id="4f175-103">安裝程式。 Features 屬性</span><span class="sxs-lookup"><span data-stu-id="4f175-103">Installer.Features property</span></span>

<span data-ttu-id="4f175-104">**Features** 屬性是唯讀屬性，它會傳回 [**StringList**](stringlist-object.md)物件，以列舉指定產品的已發行功能集。</span><span class="sxs-lookup"><span data-stu-id="4f175-104">The **Features** property is a read-only property that returns a [**StringList**](stringlist-object.md) object enumerating the set of published features for the specified product.</span></span>

<span data-ttu-id="4f175-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="4f175-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f175-106">語法</span><span class="sxs-lookup"><span data-stu-id="4f175-106">Syntax</span></span>


```JScript
propVal = Installer.Features
```



## <a name="property-value"></a><span data-ttu-id="4f175-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="4f175-107">Property value</span></span>

<span data-ttu-id="4f175-108">指定產品的產品代碼。</span><span class="sxs-lookup"><span data-stu-id="4f175-108">Specifies the product code of the product.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f175-109">備註</span><span class="sxs-lookup"><span data-stu-id="4f175-109">Remarks</span></span>

<span data-ttu-id="4f175-110">若要列舉功能，應用程式會使用 For Each 結構逐一查看 [**StringList**](stringlist-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="4f175-110">To enumerate the features, an application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="4f175-111">因為功能未排序，所以任何新功能都有任意的索引，這表示函式可以依任何順序傳回特徵。</span><span class="sxs-lookup"><span data-stu-id="4f175-111">Because features are not ordered, any new feature has an arbitrary index, meaning the function can return features in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f175-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f175-112">Requirements</span></span>



| <span data-ttu-id="4f175-113">需求</span><span class="sxs-lookup"><span data-stu-id="4f175-113">Requirement</span></span> | <span data-ttu-id="4f175-114">值</span><span class="sxs-lookup"><span data-stu-id="4f175-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f175-115">版本</span><span class="sxs-lookup"><span data-stu-id="4f175-115">Version</span></span><br/> | <span data-ttu-id="4f175-116">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="4f175-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4f175-117">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="4f175-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4f175-118">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="4f175-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="4f175-119">DLL</span><span class="sxs-lookup"><span data-stu-id="4f175-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="4f175-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f175-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="4f175-121">IID</span><span class="sxs-lookup"><span data-stu-id="4f175-121">IID</span></span><br/>     | <span data-ttu-id="4f175-122">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4f175-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="4f175-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f175-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f175-124">**MsiEnumFeatures**</span><span class="sxs-lookup"><span data-stu-id="4f175-124">**MsiEnumFeatures**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)
</dt> <dt>

[<span data-ttu-id="4f175-125">系統狀態函數</span><span class="sxs-lookup"><span data-stu-id="4f175-125">System Status Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




