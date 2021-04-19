---
title: AcceptServerName 元素
description: 指出伺服器名稱是否根據 ServerNames (ServerValidationParameters) 專案中指定的名稱字串進行驗證。 |AcceptServerName 元素
ms.assetid: 307b2d2a-1678-4aa9-82ed-46d401cf0e0f
keywords:
- AcceptServerName 元素 EAPHost
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
ms.openlocfilehash: b48c43bce2bd71f4d761ea58fcdf5e0632107f87
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106995886"
---
# <a name="acceptservername-element"></a><span data-ttu-id="e4d76-105">AcceptServerName 元素</span><span class="sxs-lookup"><span data-stu-id="e4d76-105">AcceptServerName element</span></span>

<span data-ttu-id="e4d76-106">**AcceptServerName (EapType)** 元素指出伺服器名稱是否會根據 [**ServerNames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)元素中指定的名稱字串進行驗證。</span><span class="sxs-lookup"><span data-stu-id="e4d76-106">The **AcceptServerName (EapType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

<span data-ttu-id="e4d76-107">**AcceptServerName** 元素是由 [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="e4d76-107">The **AcceptServerName** element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4d76-108">備註</span><span class="sxs-lookup"><span data-stu-id="e4d76-108">Remarks</span></span>

<span data-ttu-id="e4d76-109">**AcceptServerName** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="e4d76-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4d76-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4d76-110">Requirements</span></span>



| <span data-ttu-id="e4d76-111">需求</span><span class="sxs-lookup"><span data-stu-id="e4d76-111">Requirement</span></span> | <span data-ttu-id="e4d76-112">值</span><span class="sxs-lookup"><span data-stu-id="e4d76-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e4d76-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e4d76-113">Minimum supported client</span></span><br/> | <span data-ttu-id="e4d76-114">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4d76-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e4d76-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e4d76-115">Minimum supported server</span></span><br/> | <span data-ttu-id="e4d76-116">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4d76-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e4d76-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4d76-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="e4d76-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="e4d76-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e4d76-119">**EapType**</span><span class="sxs-lookup"><span data-stu-id="e4d76-119">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="e4d76-120">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="e4d76-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e4d76-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="e4d76-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="e4d76-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="e4d76-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="e4d76-123">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="e4d76-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="e4d76-124">eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="e4d76-124">eaptlsconnectionpropertiesv2</span></span>](eaptlsconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="e4d76-125">eaptlsconnectionpropertiesv2 架構元素</span><span class="sxs-lookup"><span data-stu-id="e4d76-125">eaptlsconnectionpropertiesv2 Schema Elements</span></span>](eaptlsconnectionpropertiesv2schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e4d76-126">**AcceptServerName (EapType)**</span><span class="sxs-lookup"><span data-stu-id="e4d76-126">**AcceptServerName (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)
</dt> </dl>

 

 





