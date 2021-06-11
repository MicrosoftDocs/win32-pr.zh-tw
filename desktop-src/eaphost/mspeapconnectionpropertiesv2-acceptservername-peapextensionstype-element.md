---
title: AcceptServerName (PeapExtensionsType) 元素
description: AcceptServerName (PeapExtensionsType) 元素指出是否根據 mspeapconnectionpropertiesv2 架構中 ServerNames 中指定的名稱字串驗證伺服器名稱。
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
ms.openlocfilehash: 64e82defae9c5ae9f7cf60056cfdac8b58373602
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989473"
---
# <a name="acceptservername-peapextensionstype-element"></a><span data-ttu-id="b3707-104">AcceptServerName (PeapExtensionsType) 元素</span><span class="sxs-lookup"><span data-stu-id="b3707-104">AcceptServerName (PeapExtensionsType) Element</span></span>

<span data-ttu-id="b3707-105">**AcceptServerName (PeapExtensionsType)** 元素指出伺服器名稱是否會根據 [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)元素中指定的名稱字串進行驗證。</span><span class="sxs-lookup"><span data-stu-id="b3707-105">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

<span data-ttu-id="b3707-106">**AcceptServerName** 元素是由 [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="b3707-106">The **AcceptServerName** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3707-107">備註</span><span class="sxs-lookup"><span data-stu-id="b3707-107">Remarks</span></span>

<span data-ttu-id="b3707-108">**AcceptServerName** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="b3707-108">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3707-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3707-109">Requirements</span></span>



| <span data-ttu-id="b3707-110">需求</span><span class="sxs-lookup"><span data-stu-id="b3707-110">Requirement</span></span> | <span data-ttu-id="b3707-111">值</span><span class="sxs-lookup"><span data-stu-id="b3707-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="b3707-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b3707-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b3707-113">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3707-113">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="b3707-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b3707-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b3707-115">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3707-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b3707-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3707-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="b3707-117">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="b3707-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b3707-118">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="b3707-118">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="b3707-119">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="b3707-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b3707-120">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="b3707-120">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="b3707-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="b3707-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="b3707-122">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="b3707-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b3707-123">mspeapconnectionpropertiesv2 架構</span><span class="sxs-lookup"><span data-stu-id="b3707-123">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="b3707-124">mspeapconnectionpropertiesv2 架構元素</span><span class="sxs-lookup"><span data-stu-id="b3707-124">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





