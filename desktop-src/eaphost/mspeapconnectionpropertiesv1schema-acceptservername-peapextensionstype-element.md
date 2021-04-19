---
title: 'AcceptServerName (PeapExtensionsType) 元素 (EAPHost) '
description: 指出伺服器名稱是否根據 ServerNames (ServerValidationParameters) 專案中指定的名稱字串進行驗證。 |AcceptServerName (PeapExtensionsType) 元素
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
ms.openlocfilehash: ba4874b7c8761f35fa93387b23eaf5463a31bcf4
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314601"
---
# <a name="acceptservername-peapextensionstype-element-eaphost"></a><span data-ttu-id="49b63-105">AcceptServerName (PeapExtensionsType) 元素 (EAPHost) </span><span class="sxs-lookup"><span data-stu-id="49b63-105">AcceptServerName (PeapExtensionsType) Element (EAPHost)</span></span>

<span data-ttu-id="49b63-106">**AcceptServerName (PeapExtensionsType)** 元素指出伺服器名稱是否會根據 [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)元素中指定的名稱字串進行驗證。</span><span class="sxs-lookup"><span data-stu-id="49b63-106">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:AcceptServerName"
 />
```

<span data-ttu-id="49b63-107">元素是由 [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="49b63-107">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="49b63-108">備註</span><span class="sxs-lookup"><span data-stu-id="49b63-108">Remarks</span></span>

<span data-ttu-id="49b63-109">**AcceptServerName** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="49b63-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="49b63-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="49b63-110">Requirements</span></span>



| <span data-ttu-id="49b63-111">需求</span><span class="sxs-lookup"><span data-stu-id="49b63-111">Requirement</span></span> | <span data-ttu-id="49b63-112">值</span><span class="sxs-lookup"><span data-stu-id="49b63-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="49b63-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49b63-113">Minimum supported client</span></span><br/> | <span data-ttu-id="49b63-114">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49b63-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="49b63-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49b63-115">Minimum supported server</span></span><br/> | <span data-ttu-id="49b63-116">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49b63-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49b63-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49b63-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="49b63-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="49b63-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="49b63-119">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="49b63-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="49b63-120">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="49b63-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="49b63-121">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="49b63-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="49b63-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="49b63-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="49b63-123">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="49b63-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="49b63-124">mspeapconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="49b63-124">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="49b63-125">mspeapconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="49b63-125">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="49b63-126">**AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="49b63-126">**AcceptServerName**</span></span>](mspeapconnectionpropertiesv2-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





