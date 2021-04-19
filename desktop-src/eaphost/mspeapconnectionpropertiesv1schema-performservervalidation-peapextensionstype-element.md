---
title: 'PerformServerValidation (PeapExtensionsType) 元素 (v1 架構) '
description: '瞭解 PerformServerValidation (PeapExtensionsType) 元素。 這個元素會指出是否執行伺服器驗證。 |PerformServerValidation (PeapExtensionsType) 元素 (v1 架構) '
ms.assetid: b0483ed0-a02f-4f60-b1ae-7c5e6be8e196
keywords:
- 元素 EAPHost
topic_type:
- apiref
api_name:
- PerformServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 256d942d68c30788180f2d8080f963c1d79b401a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106976653"
---
# <a name="performservervalidation-peapextensionstype-element-v1-schema"></a><span data-ttu-id="99529-106">PerformServerValidation (PeapExtensionsType) 元素 (v1 架構) </span><span class="sxs-lookup"><span data-stu-id="99529-106">PerformServerValidation (PeapExtensionsType) element (v1 schema)</span></span>

<span data-ttu-id="99529-107">**PerformServerValidation (PeapExtensionsType)** 元素指出是否執行伺服器驗證。</span><span class="sxs-lookup"><span data-stu-id="99529-107">The **PerformServerValidation (PeapExtensionsType)** element indicates whether server validation is performed.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:PerformServerValidation"
 />
```

<span data-ttu-id="99529-108">元素是由 [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="99529-108">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="99529-109">備註</span><span class="sxs-lookup"><span data-stu-id="99529-109">Remarks</span></span>

<span data-ttu-id="99529-110">**PerformServerValidation** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="99529-110">The **PerformServerValidation** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="99529-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="99529-111">Requirements</span></span>



| <span data-ttu-id="99529-112">角色</span><span class="sxs-lookup"><span data-stu-id="99529-112">Role</span></span> | <span data-ttu-id="99529-113">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="99529-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="99529-114">用戶端</span><span class="sxs-lookup"><span data-stu-id="99529-114">Client</span></span><br/> | <span data-ttu-id="99529-115">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99529-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="99529-116">伺服器</span><span class="sxs-lookup"><span data-stu-id="99529-116">Server</span></span><br/> | <span data-ttu-id="99529-117">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99529-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="99529-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99529-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="99529-119">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="99529-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="99529-120">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="99529-120">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="99529-121">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="99529-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="99529-122">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="99529-122">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="99529-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="99529-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="99529-124">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="99529-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="99529-125">mspeapconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="99529-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="99529-126">mspeapconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="99529-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="99529-127">**PerformServerValidation (PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="99529-127">**PerformServerValidation(PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md)
</dt> </dl>

 

 





