---
description: 安裝程式物件的唯讀修補程式屬性會傳回 StringList 物件，其中包含套用至產品的所有修補程式。
ms.assetid: a8d46073-399b-480e-b4b0-a7a2f832e160
title: 安裝程式. 修補程式屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Patches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fd94c5853b3e455cf4d814dfb3c4078705ac727b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000474"
---
# <a name="installerpatches-property"></a><span data-ttu-id="85e08-103">安裝程式. 修補程式屬性</span><span class="sxs-lookup"><span data-stu-id="85e08-103">Installer.Patches property</span></span>

<span data-ttu-id="85e08-104">[**安裝程式**](installer-object.md)物件的唯讀 **修補** 程式屬性會傳回 [**StringList**](stringlist-object.md)物件，其中包含套用至產品的所有修補程式。</span><span class="sxs-lookup"><span data-stu-id="85e08-104">The read-only **Patches** property of the [**Installer**](installer-object.md) object returns a [**StringList**](stringlist-object.md) object that contains all the patches applied to the product.</span></span>

<span data-ttu-id="85e08-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="85e08-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="85e08-106">語法</span><span class="sxs-lookup"><span data-stu-id="85e08-106">Syntax</span></span>


```JScript
propVal = Installer.Patches
```



## <a name="property-value"></a><span data-ttu-id="85e08-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="85e08-107">Property value</span></span>

<span data-ttu-id="85e08-108">指定產品代碼。</span><span class="sxs-lookup"><span data-stu-id="85e08-108">Specifies the product code.</span></span>

## <a name="remarks"></a><span data-ttu-id="85e08-109">備註</span><span class="sxs-lookup"><span data-stu-id="85e08-109">Remarks</span></span>

<span data-ttu-id="85e08-110">若要列舉修補程式，應用程式會使用 For Each 結構逐一查看 [**StringList**](stringlist-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="85e08-110">To enumerate the patches, an application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="85e08-111">因為修補程式未排序，所以任何新的修補程式都有任意的索引。</span><span class="sxs-lookup"><span data-stu-id="85e08-111">Because patches are not ordered, any new patch has an arbitrary index.</span></span> <span data-ttu-id="85e08-112">這表示函數可以依任何順序傳回修補程式。</span><span class="sxs-lookup"><span data-stu-id="85e08-112">This means that the function can return patches in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="85e08-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="85e08-113">Requirements</span></span>



| <span data-ttu-id="85e08-114">需求</span><span class="sxs-lookup"><span data-stu-id="85e08-114">Requirement</span></span> | <span data-ttu-id="85e08-115">值</span><span class="sxs-lookup"><span data-stu-id="85e08-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85e08-116">版本</span><span class="sxs-lookup"><span data-stu-id="85e08-116">Version</span></span><br/> | <span data-ttu-id="85e08-117">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="85e08-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="85e08-118">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="85e08-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="85e08-119">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="85e08-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="85e08-120">DLL</span><span class="sxs-lookup"><span data-stu-id="85e08-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="85e08-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85e08-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="85e08-122">IID</span><span class="sxs-lookup"><span data-stu-id="85e08-122">IID</span></span><br/>     | <span data-ttu-id="85e08-123">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="85e08-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="85e08-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85e08-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85e08-125">**MsiEnumPatches**</span><span class="sxs-lookup"><span data-stu-id="85e08-125">**MsiEnumPatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> </dl>

 

 




