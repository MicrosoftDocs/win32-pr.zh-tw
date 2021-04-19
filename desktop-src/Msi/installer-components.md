---
description: '[唯讀元件] 屬性會傳回 StringList 物件，以列舉所有產品的已安裝元件集合。'
ms.assetid: c84e4329-428a-440a-bd65-097588a86932
title: 安裝程式. Components 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Components
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6767be5182b15836c071bf8b00ed8441f6031dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997775"
---
# <a name="installercomponents-property"></a><span data-ttu-id="c9f99-103">安裝程式. Components 屬性</span><span class="sxs-lookup"><span data-stu-id="c9f99-103">Installer.Components property</span></span>

<span data-ttu-id="c9f99-104">[唯讀 **元件** ] 屬性會傳回 [**StringList**](stringlist-object.md) 物件，以列舉所有產品的已安裝元件集合。</span><span class="sxs-lookup"><span data-stu-id="c9f99-104">The read-only **Components** property returns a [**StringList**](stringlist-object.md) object enumerating the set of installed components for all products.</span></span>

<span data-ttu-id="c9f99-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="c9f99-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9f99-106">語法</span><span class="sxs-lookup"><span data-stu-id="c9f99-106">Syntax</span></span>


```JScript
propVal = Installer.Components
```



## <a name="property-value"></a><span data-ttu-id="c9f99-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="c9f99-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="c9f99-108">備註</span><span class="sxs-lookup"><span data-stu-id="c9f99-108">Remarks</span></span>

<span data-ttu-id="c9f99-109">若要列舉元件，應用程式可以使用 For Each 結構來逐一查看 [**StringList**](stringlist-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="c9f99-109">To enumerate the components, an application can iterate through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="c9f99-110">因為不會排序元件，所以任何新元件都有任意的索引。</span><span class="sxs-lookup"><span data-stu-id="c9f99-110">Because components are not ordered, any new components has an arbitrary index.</span></span> <span data-ttu-id="c9f99-111">這表示函數可以依任何順序傳回元件。</span><span class="sxs-lookup"><span data-stu-id="c9f99-111">This means that the function can return components in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9f99-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9f99-112">Requirements</span></span>



| <span data-ttu-id="c9f99-113">需求</span><span class="sxs-lookup"><span data-stu-id="c9f99-113">Requirement</span></span> | <span data-ttu-id="c9f99-114">值</span><span class="sxs-lookup"><span data-stu-id="c9f99-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9f99-115">版本</span><span class="sxs-lookup"><span data-stu-id="c9f99-115">Version</span></span><br/> | <span data-ttu-id="c9f99-116">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="c9f99-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c9f99-117">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="c9f99-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c9f99-118">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="c9f99-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c9f99-119">DLL</span><span class="sxs-lookup"><span data-stu-id="c9f99-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="c9f99-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9f99-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c9f99-121">IID</span><span class="sxs-lookup"><span data-stu-id="c9f99-121">IID</span></span><br/>     | <span data-ttu-id="c9f99-122">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c9f99-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="c9f99-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9f99-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9f99-124">**MsiEnumComponents**</span><span class="sxs-lookup"><span data-stu-id="c9f99-124">**MsiEnumComponents**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)
</dt> </dl>

 

 




