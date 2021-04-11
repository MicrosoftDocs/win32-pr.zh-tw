---
title: AcceptServerName (PeapExtensionsType) 元素
description: 指出伺服器名稱是否根據 ServerNames (ServerValidationParameters) 專案中指定的名稱字串進行驗證。 |AcceptServerName (PeapExtensionsType) 元素
ms.assetid: 24409775-d00d-439f-bb0b-a9fe5fb736a7
keywords:
- AcceptServerName 元素 EAPHost
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
ms.openlocfilehash: d085122104c2764896801015c58fcbc9f72a1580
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945974"
---
# <a name="acceptservername-peapextensionstype-element"></a><span data-ttu-id="40d51-105">AcceptServerName (PeapExtensionsType) 元素</span><span class="sxs-lookup"><span data-stu-id="40d51-105">AcceptServerName (PeapExtensionsType) Element</span></span>

<span data-ttu-id="40d51-106">**AcceptServerName (PeapExtensionsType)** 元素指出伺服器名稱是否會根據 [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)元素中指定的名稱字串進行驗證。</span><span class="sxs-lookup"><span data-stu-id="40d51-106">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

<span data-ttu-id="40d51-107">**AcceptServerName** 元素是由 [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="40d51-107">The **AcceptServerName** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="40d51-108">備註</span><span class="sxs-lookup"><span data-stu-id="40d51-108">Remarks</span></span>

<span data-ttu-id="40d51-109">**AcceptServerName** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="40d51-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="40d51-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="40d51-110">Requirements</span></span>



| <span data-ttu-id="40d51-111">需求</span><span class="sxs-lookup"><span data-stu-id="40d51-111">Requirement</span></span> | <span data-ttu-id="40d51-112">值</span><span class="sxs-lookup"><span data-stu-id="40d51-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="40d51-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="40d51-113">Minimum supported client</span></span><br/> | <span data-ttu-id="40d51-114">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40d51-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="40d51-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="40d51-115">Minimum supported server</span></span><br/> | <span data-ttu-id="40d51-116">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40d51-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="40d51-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40d51-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="40d51-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="40d51-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="40d51-119">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="40d51-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="40d51-120">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="40d51-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="40d51-121">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="40d51-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="40d51-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="40d51-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="40d51-123">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="40d51-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="40d51-124">mspeapconnectionpropertiesv2 架構</span><span class="sxs-lookup"><span data-stu-id="40d51-124">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="40d51-125">mspeapconnectionpropertiesv2 架構元素</span><span class="sxs-lookup"><span data-stu-id="40d51-125">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





