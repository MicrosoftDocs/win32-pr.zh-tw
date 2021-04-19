---
description: FeatureInfo 物件包含有關目標功能的資訊，並使用 FeatureInfo 方法從會話物件建立。
ms.assetid: c9c96799-22c7-4e74-947b-3b8d31ebc1f1
title: FeatureInfo 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1db1bab5b1e55f027bb01eb9eff22484a4e39170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975731"
---
# <a name="featureinfo-object"></a><span data-ttu-id="420fd-103">FeatureInfo 物件</span><span class="sxs-lookup"><span data-stu-id="420fd-103">FeatureInfo object</span></span>

<span data-ttu-id="420fd-104">**FeatureInfo** 物件包含有關目標功能的資訊，並使用 [**FeatureInfo**](session-featureinfo.md)方法從 [**會話**](session-object.md)物件建立。</span><span class="sxs-lookup"><span data-stu-id="420fd-104">The **FeatureInfo** object contains information regarding the targeted feature and is created from the [**Session**](session-object.md) object using the [**FeatureInfo**](session-featureinfo.md) Method.</span></span>

## <a name="members"></a><span data-ttu-id="420fd-105">成員</span><span class="sxs-lookup"><span data-stu-id="420fd-105">Members</span></span>

<span data-ttu-id="420fd-106">**FeatureInfo** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="420fd-106">The **FeatureInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="420fd-107">屬性</span><span class="sxs-lookup"><span data-stu-id="420fd-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="420fd-108">屬性</span><span class="sxs-lookup"><span data-stu-id="420fd-108">Properties</span></span>

<span data-ttu-id="420fd-109">**FeatureInfo** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="420fd-109">The **FeatureInfo** object has these properties.</span></span>



| <span data-ttu-id="420fd-110">屬性</span><span class="sxs-lookup"><span data-stu-id="420fd-110">Property</span></span>                                                  | <span data-ttu-id="420fd-111">存取類型</span><span class="sxs-lookup"><span data-stu-id="420fd-111">Access type</span></span>           | <span data-ttu-id="420fd-112">Description</span><span class="sxs-lookup"><span data-stu-id="420fd-112">Description</span></span>                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="420fd-113">**屬性**</span><span class="sxs-lookup"><span data-stu-id="420fd-113">**Attributes**</span></span>](featureinfo-attributes.md)<br/>   | <span data-ttu-id="420fd-114">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="420fd-114">Read/write</span></span><br/> | <span data-ttu-id="420fd-115">在功能資料表的 [屬性] 資料行中，傳回功能的值。</span><span class="sxs-lookup"><span data-stu-id="420fd-115">Returns the value for the feature in the Attributes column of the Feature table.</span></span><br/> |
| [<span data-ttu-id="420fd-116">**描述**</span><span class="sxs-lookup"><span data-stu-id="420fd-116">**Description**</span></span>](featureinfo-description.md)<br/> |                       | <span data-ttu-id="420fd-117">傳回功能的描述。</span><span class="sxs-lookup"><span data-stu-id="420fd-117">Returns the description of the feature.</span></span><br/>                                          |
| [<span data-ttu-id="420fd-118">**標題**</span><span class="sxs-lookup"><span data-stu-id="420fd-118">**Title**</span></span>](featureinfo-title.md)<br/>             | <span data-ttu-id="420fd-119">唯讀</span><span class="sxs-lookup"><span data-stu-id="420fd-119">Read-only</span></span><br/>  | <span data-ttu-id="420fd-120">傳回功能的標題。</span><span class="sxs-lookup"><span data-stu-id="420fd-120">Returns the title of the feature.</span></span><br/>                                                |



 

## <a name="requirements"></a><span data-ttu-id="420fd-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="420fd-121">Requirements</span></span>



| <span data-ttu-id="420fd-122">需求</span><span class="sxs-lookup"><span data-stu-id="420fd-122">Requirement</span></span> | <span data-ttu-id="420fd-123">值</span><span class="sxs-lookup"><span data-stu-id="420fd-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="420fd-124">版本</span><span class="sxs-lookup"><span data-stu-id="420fd-124">Version</span></span><br/> | <span data-ttu-id="420fd-125">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="420fd-125">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="420fd-126">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="420fd-126">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="420fd-127">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="420fd-127">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="420fd-128">DLL</span><span class="sxs-lookup"><span data-stu-id="420fd-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="420fd-129"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="420fd-129"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="420fd-130">IID</span><span class="sxs-lookup"><span data-stu-id="420fd-130">IID</span></span><br/>     | <span data-ttu-id="420fd-131">IID \_ IFeatureInfo 定義為 000C109F-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="420fd-131">IID\_IFeatureInfo is defined as 000C109F-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="420fd-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="420fd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="420fd-133">Windows Installer 腳本範例</span><span class="sxs-lookup"><span data-stu-id="420fd-133">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




