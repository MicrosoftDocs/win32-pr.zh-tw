---
description: ComponentQualifiers 屬性是唯讀屬性，它會傳回 StringList 物件，以列舉指定元件的已註冊限定詞集合。
ms.assetid: 49b16c9a-ce84-42ff-af1d-f4ecf7dbe23a
title: ComponentQualifiers 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentQualifiers
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0e6f58850974eaa2021578f0d56015ea0ef6d9e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987162"
---
# <a name="installercomponentqualifiers-property"></a><span data-ttu-id="36f37-103">ComponentQualifiers 屬性</span><span class="sxs-lookup"><span data-stu-id="36f37-103">Installer.ComponentQualifiers property</span></span>

<span data-ttu-id="36f37-104">**ComponentQualifiers** 屬性是唯讀屬性，它會傳回 [**StringList**](stringlist-object.md)物件，以列舉指定元件的已註冊限定詞集合。</span><span class="sxs-lookup"><span data-stu-id="36f37-104">The **ComponentQualifiers** property is a read-only property that returns a [**StringList**](stringlist-object.md) object enumerating the set of registered qualifiers for the specified component.</span></span>

<span data-ttu-id="36f37-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="36f37-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="36f37-106">語法</span><span class="sxs-lookup"><span data-stu-id="36f37-106">Syntax</span></span>


```JScript
propVal = Installer.ComponentQualifiers
```



## <a name="property-value"></a><span data-ttu-id="36f37-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="36f37-107">Property value</span></span>

<span data-ttu-id="36f37-108">表示 [元件](publishcomponent-table.md)類別目錄的字串 GUID。</span><span class="sxs-lookup"><span data-stu-id="36f37-108">A string GUID that represents the category of [component](publishcomponent-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="36f37-109">備註</span><span class="sxs-lookup"><span data-stu-id="36f37-109">Remarks</span></span>

<span data-ttu-id="36f37-110">若要列舉限定詞，應用程式會使用 For Each 結構逐一查看 [**StringList**](stringlist-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="36f37-110">To enumerate qualifiers the application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="36f37-111">因為不會排序限定詞，所以任何新的限定詞都會有任意的索引，這表示函式可以依照任何順序傳回限定詞。</span><span class="sxs-lookup"><span data-stu-id="36f37-111">Because qualifiers are not ordered, any new qualifier has an arbitrary index, meaning the function can return qualifiers in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="36f37-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="36f37-112">Requirements</span></span>



| <span data-ttu-id="36f37-113">需求</span><span class="sxs-lookup"><span data-stu-id="36f37-113">Requirement</span></span> | <span data-ttu-id="36f37-114">值</span><span class="sxs-lookup"><span data-stu-id="36f37-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36f37-115">版本</span><span class="sxs-lookup"><span data-stu-id="36f37-115">Version</span></span><br/> | <span data-ttu-id="36f37-116">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="36f37-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="36f37-117">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="36f37-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="36f37-118">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="36f37-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="36f37-119">DLL</span><span class="sxs-lookup"><span data-stu-id="36f37-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="36f37-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36f37-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="36f37-121">IID</span><span class="sxs-lookup"><span data-stu-id="36f37-121">IID</span></span><br/>     | <span data-ttu-id="36f37-122">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="36f37-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="36f37-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36f37-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36f37-124">**MsiEnumComponentQualifiers**</span><span class="sxs-lookup"><span data-stu-id="36f37-124">**MsiEnumComponentQualifiers**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> </dl>

 

 




