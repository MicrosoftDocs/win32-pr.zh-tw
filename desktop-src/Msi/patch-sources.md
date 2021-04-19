---
description: '[來源] 屬性會列舉 patch 實例的所有來源。 這個屬性會呼叫 MsiSourceListEnumSources 並傳回字串陣列，並接受來源類型做為引數。'
ms.assetid: 4a052518-4d76-4a95-be9e-7acae36db626
title: Patch。來源屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 18b9e6ab867d68908bc8dd7e7f87f942f8cd015c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997677"
---
# <a name="patchsources-property"></a><span data-ttu-id="0f4d5-104">Patch。來源屬性</span><span class="sxs-lookup"><span data-stu-id="0f4d5-104">Patch.Sources property</span></span>

<span data-ttu-id="0f4d5-105">[ **來源** ] 屬性會列舉 patch 實例的所有來源。</span><span class="sxs-lookup"><span data-stu-id="0f4d5-105">The **Sources** property enumerates all the sources for the patch instance.</span></span> <span data-ttu-id="0f4d5-106">這個屬性會呼叫 [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) 並傳回字串陣列，並接受來源類型做為引數。</span><span class="sxs-lookup"><span data-stu-id="0f4d5-106">This property calls [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) and returns an array of strings, and accepts the source type as argument.</span></span>

<span data-ttu-id="0f4d5-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="0f4d5-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f4d5-108">語法</span><span class="sxs-lookup"><span data-stu-id="0f4d5-108">Syntax</span></span>


```JScript
propVal = Patch.Sources
```



## <a name="property-value"></a><span data-ttu-id="0f4d5-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="0f4d5-109">Property value</span></span>

<span data-ttu-id="0f4d5-110">要列舉的來源型別。</span><span class="sxs-lookup"><span data-stu-id="0f4d5-110">The type of source to enumerate.</span></span> <span data-ttu-id="0f4d5-111">值可以 *msiInstallSourceTypeNetwork* (1) 或 *msiInstallSourceTypeURL* (2) 。</span><span class="sxs-lookup"><span data-stu-id="0f4d5-111">The value can be *msiInstallSourceTypeNetwork* (1) or *msiInstallSourceTypeURL* (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f4d5-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f4d5-112">Requirements</span></span>



| <span data-ttu-id="0f4d5-113">需求</span><span class="sxs-lookup"><span data-stu-id="0f4d5-113">Requirement</span></span> | <span data-ttu-id="0f4d5-114">值</span><span class="sxs-lookup"><span data-stu-id="0f4d5-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f4d5-115">版本</span><span class="sxs-lookup"><span data-stu-id="0f4d5-115">Version</span></span><br/> | <span data-ttu-id="0f4d5-116">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="0f4d5-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0f4d5-117">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="0f4d5-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0f4d5-118">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="0f4d5-118">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="0f4d5-119">DLL</span><span class="sxs-lookup"><span data-stu-id="0f4d5-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="0f4d5-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f4d5-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="0f4d5-121">IID</span><span class="sxs-lookup"><span data-stu-id="0f4d5-121">IID</span></span><br/>     | <span data-ttu-id="0f4d5-122">IID \_ IPatch 定義為000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0f4d5-122">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="0f4d5-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f4d5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f4d5-124">**Patch**</span><span class="sxs-lookup"><span data-stu-id="0f4d5-124">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="0f4d5-125">**MsiSourceListEnumSources**</span><span class="sxs-lookup"><span data-stu-id="0f4d5-125">**MsiSourceListEnumSources**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[<span data-ttu-id="0f4d5-126">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="0f4d5-126">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




