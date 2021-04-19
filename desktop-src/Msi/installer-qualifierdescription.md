---
description: 唯讀 QualifierDescription 屬性會傳回描述限定元件的文字字串。
ms.assetid: 43615bd9-824b-4b84-a8f2-eef30cc7619a
title: QualifierDescription 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.QualifierDescription
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8937e0a1fee89bb3ebe1b6402c94778bdd2a0915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995460"
---
# <a name="installerqualifierdescription-property"></a><span data-ttu-id="8f718-103">QualifierDescription 屬性</span><span class="sxs-lookup"><span data-stu-id="8f718-103">Installer.QualifierDescription property</span></span>

<span data-ttu-id="8f718-104">唯讀 **QualifierDescription** 屬性會傳回描述限定元件的文字字串。</span><span class="sxs-lookup"><span data-stu-id="8f718-104">The read-only **QualifierDescription** property returns a text string describing the qualified component.</span></span> <span data-ttu-id="8f718-105">這個可當地語系化的字串會編寫到 [PublishComponent 資料表](publishcomponent-table.md) 的 AppData 資料行中，而且可以向使用者顯示。</span><span class="sxs-lookup"><span data-stu-id="8f718-105">This localizable string is authored into the AppData column of the [PublishComponent table](publishcomponent-table.md) and can be displayed to the user.</span></span> <span data-ttu-id="8f718-106">限定詞會區分相同元件的多個表單，例如以多種語言所執行的元件。</span><span class="sxs-lookup"><span data-stu-id="8f718-106">The qualifier distinguishes multiple forms of the same component, such as a component that is implemented in multiple languages.</span></span>

<span data-ttu-id="8f718-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="8f718-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f718-108">語法</span><span class="sxs-lookup"><span data-stu-id="8f718-108">Syntax</span></span>


```JScript
propVal = Installer.QualifierDescription
```



## <a name="property-value"></a><span data-ttu-id="8f718-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="8f718-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="8f718-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f718-110">Requirements</span></span>



| <span data-ttu-id="8f718-111">需求</span><span class="sxs-lookup"><span data-stu-id="8f718-111">Requirement</span></span> | <span data-ttu-id="8f718-112">值</span><span class="sxs-lookup"><span data-stu-id="8f718-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f718-113">版本</span><span class="sxs-lookup"><span data-stu-id="8f718-113">Version</span></span><br/> | <span data-ttu-id="8f718-114">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="8f718-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8f718-115">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="8f718-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8f718-116">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="8f718-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="8f718-117">DLL</span><span class="sxs-lookup"><span data-stu-id="8f718-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="8f718-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f718-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="8f718-119">IID</span><span class="sxs-lookup"><span data-stu-id="8f718-119">IID</span></span><br/>     | <span data-ttu-id="8f718-120">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="8f718-120">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="8f718-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f718-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f718-122">**MsiEnumComponentQualifiers**</span><span class="sxs-lookup"><span data-stu-id="8f718-122">**MsiEnumComponentQualifiers**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> <dt>

[<span data-ttu-id="8f718-123">合格元件</span><span class="sxs-lookup"><span data-stu-id="8f718-123">Qualified Components</span></span>](qualified-components.md)
</dt> </dl>

 

 




