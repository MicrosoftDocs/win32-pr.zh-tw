---
description: FeatureUsageCount 屬性是唯讀屬性，會傳回功能已使用的次數。
ms.assetid: 70171e22-d73a-4718-a360-df9d1722761b
title: FeatureUsageCount 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageCount
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fbacb6b6fd5dc4d31d7c727d719e1253969c0d43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000671"
---
# <a name="installerfeatureusagecount-property"></a><span data-ttu-id="7e06d-103">FeatureUsageCount 屬性</span><span class="sxs-lookup"><span data-stu-id="7e06d-103">Installer.FeatureUsageCount property</span></span>

<span data-ttu-id="7e06d-104">**FeatureUsageCount** 屬性是唯讀屬性，會傳回功能已使用的次數。</span><span class="sxs-lookup"><span data-stu-id="7e06d-104">The **FeatureUsageCount** property is a read-only property that returns the number of times the feature has been used.</span></span>

<span data-ttu-id="7e06d-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="7e06d-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e06d-106">語法</span><span class="sxs-lookup"><span data-stu-id="7e06d-106">Syntax</span></span>


```JScript
propVal = Installer.FeatureUsageCount
```



## <a name="property-value"></a><span data-ttu-id="7e06d-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="7e06d-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="7e06d-108">備註</span><span class="sxs-lookup"><span data-stu-id="7e06d-108">Remarks</span></span>

<span data-ttu-id="7e06d-109">使用 [**UseFeature**](installer-usefeature.md)、 [**ProvideComponent**](installer-providecomponent.md) 或 [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) 方法或其在指定功能上的 API 對等專案，會遞增這個屬性。</span><span class="sxs-lookup"><span data-stu-id="7e06d-109">Use of the [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) or [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) methods or their API equivalents on the specified feature increments this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e06d-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e06d-110">Requirements</span></span>



| <span data-ttu-id="7e06d-111">需求</span><span class="sxs-lookup"><span data-stu-id="7e06d-111">Requirement</span></span> | <span data-ttu-id="7e06d-112">值</span><span class="sxs-lookup"><span data-stu-id="7e06d-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e06d-113">版本</span><span class="sxs-lookup"><span data-stu-id="7e06d-113">Version</span></span><br/> | <span data-ttu-id="7e06d-114">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="7e06d-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7e06d-115">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="7e06d-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7e06d-116">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="7e06d-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7e06d-117">DLL</span><span class="sxs-lookup"><span data-stu-id="7e06d-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="7e06d-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e06d-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7e06d-119">IID</span><span class="sxs-lookup"><span data-stu-id="7e06d-119">IID</span></span><br/>     | <span data-ttu-id="7e06d-120">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7e06d-120">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="7e06d-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e06d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e06d-122">**MsiGetFeatureUsage**</span><span class="sxs-lookup"><span data-stu-id="7e06d-122">**MsiGetFeatureUsage**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




