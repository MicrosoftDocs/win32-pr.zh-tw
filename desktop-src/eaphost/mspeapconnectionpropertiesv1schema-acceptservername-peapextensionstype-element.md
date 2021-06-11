---
title: 'AcceptServerName (PeapExtensionsType) 元素 (EAPHost) '
description: AcceptServerName (PeapExtensionsType) 元素指出是否根據 mspeapconnectionpropertiesv1 架構中 ServerNames 中指定的名稱字串驗證伺服器名稱。
ms.assetid: 95173b57-8100-44e4-98f0-4f2a3deabce7
keywords:
- 元素 EAPHost
topic_type:
- apiref
api_name:
- AcceptServerName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 64565b24da0b4a93fd35fd3c4a6e7075546024c4
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989093"
---
# <a name="acceptservername-peapextensionstype-element-eaphost"></a><span data-ttu-id="450ee-104">AcceptServerName (PeapExtensionsType) 元素 (EAPHost) </span><span class="sxs-lookup"><span data-stu-id="450ee-104">AcceptServerName (PeapExtensionsType) Element (EAPHost)</span></span>

<span data-ttu-id="450ee-105">**AcceptServerName (PeapExtensionsType)** 元素指出伺服器名稱是否會根據 [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)元素中指定的名稱字串進行驗證。</span><span class="sxs-lookup"><span data-stu-id="450ee-105">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:AcceptServerName"
 />
```

<span data-ttu-id="450ee-106">元素是由 [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="450ee-106">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="450ee-107">備註</span><span class="sxs-lookup"><span data-stu-id="450ee-107">Remarks</span></span>

<span data-ttu-id="450ee-108">**AcceptServerName** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="450ee-108">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="450ee-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="450ee-109">Requirements</span></span>



| <span data-ttu-id="450ee-110">需求</span><span class="sxs-lookup"><span data-stu-id="450ee-110">Requirement</span></span> | <span data-ttu-id="450ee-111">值</span><span class="sxs-lookup"><span data-stu-id="450ee-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="450ee-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="450ee-112">Minimum supported client</span></span><br/> | <span data-ttu-id="450ee-113">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="450ee-113">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="450ee-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="450ee-114">Minimum supported server</span></span><br/> | <span data-ttu-id="450ee-115">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="450ee-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="450ee-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="450ee-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="450ee-117">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="450ee-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="450ee-118">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="450ee-118">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="450ee-119">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="450ee-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="450ee-120">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="450ee-120">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="450ee-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="450ee-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="450ee-122">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="450ee-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="450ee-123">mspeapconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="450ee-123">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="450ee-124">mspeapconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="450ee-124">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="450ee-125">**AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="450ee-125">**AcceptServerName**</span></span>](mspeapconnectionpropertiesv2-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





