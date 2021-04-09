---
title: 'PerformServerValidation (PeapExtensionsType) 元素 (V2 架構) '
description: '瞭解 PerformServerValidation (PeapExtensionsType) 元素。 這個元素會指出是否執行伺服器驗證。 |PerformServerValidation (PeapExtensionsType) 元素 (V2 架構) '
ms.assetid: a9c383d4-2582-47dd-bdf1-dd4e6c1689f7
keywords:
- PerformServerValidation 元素 EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 32bc213aa67e87eb8af0643a15f16b298cfb3204
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196045"
---
# <a name="performservervalidation-peapextensionstype-element-v2-schema"></a><span data-ttu-id="3f8eb-106">PerformServerValidation (PeapExtensionsType) 元素 (V2 架構) </span><span class="sxs-lookup"><span data-stu-id="3f8eb-106">PerformServerValidation (PeapExtensionsType) Element (V2 schema)</span></span>

<span data-ttu-id="3f8eb-107">**PerformServerValidation (PeapExtensionsType)** 元素指出是否執行伺服器驗證。</span><span class="sxs-lookup"><span data-stu-id="3f8eb-107">The **PerformServerValidation (PeapExtensionsType)** element indicates whether server validation is performed.</span></span>

``` syntax
<xs:element name="PerformServerValidation"
    type="xs:boolean"
 />
```

<span data-ttu-id="3f8eb-108">**PerformServerValidation** 元素是由 [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="3f8eb-108">The **PerformServerValidation** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f8eb-109">備註</span><span class="sxs-lookup"><span data-stu-id="3f8eb-109">Remarks</span></span>

<span data-ttu-id="3f8eb-110">**PerformServerValidation** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="3f8eb-110">The **PerformServerValidation** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f8eb-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f8eb-111">Requirements</span></span>



| <span data-ttu-id="3f8eb-112">角色</span><span class="sxs-lookup"><span data-stu-id="3f8eb-112">Role</span></span> | <span data-ttu-id="3f8eb-113">最低 OS 版本</span><span class="sxs-lookup"><span data-stu-id="3f8eb-113">Minimum OS version</span></span> |
|------|--------------------|
| <span data-ttu-id="3f8eb-114">用戶端</span><span class="sxs-lookup"><span data-stu-id="3f8eb-114">Client</span></span><br/> | <span data-ttu-id="3f8eb-115">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f8eb-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="3f8eb-116">伺服器</span><span class="sxs-lookup"><span data-stu-id="3f8eb-116">Server</span></span><br/> | <span data-ttu-id="3f8eb-117">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f8eb-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3f8eb-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f8eb-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="3f8eb-119">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="3f8eb-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3f8eb-120">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="3f8eb-120">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="3f8eb-121">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="3f8eb-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3f8eb-122">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="3f8eb-122">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="3f8eb-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="3f8eb-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="3f8eb-124">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="3f8eb-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3f8eb-125">mspeapconnectionpropertiesv2 架構</span><span class="sxs-lookup"><span data-stu-id="3f8eb-125">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="3f8eb-126">mspeapconnectionpropertiesv2 架構元素</span><span class="sxs-lookup"><span data-stu-id="3f8eb-126">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





