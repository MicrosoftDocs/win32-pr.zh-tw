---
description: FeatureUsageDate 屬性是唯讀屬性，會傳回上次使用指定功能的日期。
ms.assetid: 444e54b2-94e7-44ea-8d7b-eeac984e3715
title: FeatureUsageDate 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageDate
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b393f9a24b9d1ebeb82de86d26483f703d7854c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986172"
---
# <a name="installerfeatureusagedate-property"></a><span data-ttu-id="10a19-103">FeatureUsageDate 屬性</span><span class="sxs-lookup"><span data-stu-id="10a19-103">Installer.FeatureUsageDate property</span></span>

<span data-ttu-id="10a19-104">**FeatureUsageDate** 屬性是唯讀屬性，會傳回上次使用指定功能的日期。</span><span class="sxs-lookup"><span data-stu-id="10a19-104">The **FeatureUsageDate** property is a read-only property that returns the date the specified feature was last used.</span></span>

<span data-ttu-id="10a19-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="10a19-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="10a19-106">語法</span><span class="sxs-lookup"><span data-stu-id="10a19-106">Syntax</span></span>


```JScript
propVal = Installer.FeatureUsageDate
```



## <a name="property-value"></a><span data-ttu-id="10a19-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="10a19-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="10a19-108">備註</span><span class="sxs-lookup"><span data-stu-id="10a19-108">Remarks</span></span>

<span data-ttu-id="10a19-109">使用 [**UseFeature**](installer-usefeature.md)、 [**ProvideComponent**](installer-providecomponent.md) 或 [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) 方法或其在指定功能上的 API 對等專案，會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="10a19-109">Use of the [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) or [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) methods or their API equivalents on the specified feature sets this property.</span></span>

<span data-ttu-id="10a19-110">日期會是 MS-DOS 日期格式，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="10a19-110">The date is in the MS-DOS date format as shown in the following table.</span></span>



| <span data-ttu-id="10a19-111">Bits</span><span class="sxs-lookup"><span data-stu-id="10a19-111">Bits</span></span> | <span data-ttu-id="10a19-112">目錄</span><span class="sxs-lookup"><span data-stu-id="10a19-112">Contents</span></span>                                            |
|------|-----------------------------------------------------|
| <span data-ttu-id="10a19-113">0-4</span><span class="sxs-lookup"><span data-stu-id="10a19-113">0-4</span></span>  | <span data-ttu-id="10a19-114">每月的日 (1-31) </span><span class="sxs-lookup"><span data-stu-id="10a19-114">Day of the month (1-31)</span></span>                             |
| <span data-ttu-id="10a19-115">5-8</span><span class="sxs-lookup"><span data-stu-id="10a19-115">5-8</span></span>  | <span data-ttu-id="10a19-116">月 (1 = 一月、2 = 二月，依此類推) </span><span class="sxs-lookup"><span data-stu-id="10a19-116">Month (1 = January, 2 = February, and so on)</span></span>        |
| <span data-ttu-id="10a19-117">9-15</span><span class="sxs-lookup"><span data-stu-id="10a19-117">9-15</span></span> | <span data-ttu-id="10a19-118">從1980算起的年位移 (新增1980以取得實際年份) </span><span class="sxs-lookup"><span data-stu-id="10a19-118">Year offset from 1980 (add 1980 to get actual year)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="10a19-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="10a19-119">Requirements</span></span>



| <span data-ttu-id="10a19-120">需求</span><span class="sxs-lookup"><span data-stu-id="10a19-120">Requirement</span></span> | <span data-ttu-id="10a19-121">值</span><span class="sxs-lookup"><span data-stu-id="10a19-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10a19-122">版本</span><span class="sxs-lookup"><span data-stu-id="10a19-122">Version</span></span><br/> | <span data-ttu-id="10a19-123">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="10a19-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="10a19-124">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="10a19-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="10a19-125">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="10a19-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="10a19-126">DLL</span><span class="sxs-lookup"><span data-stu-id="10a19-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="10a19-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10a19-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="10a19-128">IID</span><span class="sxs-lookup"><span data-stu-id="10a19-128">IID</span></span><br/>     | <span data-ttu-id="10a19-129">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="10a19-129">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="10a19-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10a19-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10a19-131">**MsiGetFeatureUsage**</span><span class="sxs-lookup"><span data-stu-id="10a19-131">**MsiGetFeatureUsage**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




