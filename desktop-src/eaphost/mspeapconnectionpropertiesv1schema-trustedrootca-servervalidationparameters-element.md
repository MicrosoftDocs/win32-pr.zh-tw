---
title: 'TrustedRootCA (ServerValidationParameters) 元素 (v1) '
description: 捕捉用戶端信任的根憑證授權單位 (Ca) 的 thumb 列印。 |TrustedRootCA (ServerValidationParameters) 元素
ms.assetid: f0485dcc-8610-4c5b-b4db-6f2a77057489
keywords:
- TrustedRootCA 元素 EAPHost
topic_type:
- apiref
api_name:
- TrustedRootCA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17e1b81e080d48ac8fae4f082c3cf4b46bac858e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/05/2021
ms.locfileid: "106995983"
---
# <a name="trustedrootca-servervalidationparameters-element"></a><span data-ttu-id="bbd6f-105">TrustedRootCA (ServerValidationParameters) 元素</span><span class="sxs-lookup"><span data-stu-id="bbd6f-105">TrustedRootCA (ServerValidationParameters) Element</span></span>

<span data-ttu-id="bbd6f-106">**TrustedRootCA (ServerValidationParameters)** 元素元素會捕捉用戶端所信任之根憑證授權單位 (ca) 的 thumb 列印。</span><span class="sxs-lookup"><span data-stu-id="bbd6f-106">The **TrustedRootCA (ServerValidationParameters)** element element captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span>

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

<span data-ttu-id="bbd6f-107">**TrustedRootCA** 元素是由 [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="bbd6f-107">The **TrustedRootCA** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbd6f-108">備註</span><span class="sxs-lookup"><span data-stu-id="bbd6f-108">Remarks</span></span>

<span data-ttu-id="bbd6f-109">Thumb 列印是包含憑證之 SHA-1 雜湊的十六進位字串。</span><span class="sxs-lookup"><span data-stu-id="bbd6f-109">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate.</span></span> <span data-ttu-id="bbd6f-110">**TrustedRootCA** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="bbd6f-110">The **TrustedRootCA** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbd6f-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="bbd6f-111">Requirements</span></span>



| <span data-ttu-id="bbd6f-112">需求</span><span class="sxs-lookup"><span data-stu-id="bbd6f-112">Requirement</span></span> | <span data-ttu-id="bbd6f-113">值</span><span class="sxs-lookup"><span data-stu-id="bbd6f-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bbd6f-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bbd6f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="bbd6f-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bbd6f-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bbd6f-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bbd6f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="bbd6f-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bbd6f-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bbd6f-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bbd6f-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="bbd6f-119">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="bbd6f-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bbd6f-120">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="bbd6f-120">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="bbd6f-121">**架構實例中可能的直接父元素**</span><span class="sxs-lookup"><span data-stu-id="bbd6f-121">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bbd6f-122">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="bbd6f-122">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="bbd6f-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="bbd6f-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="bbd6f-124">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="bbd6f-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="bbd6f-125">mspeapconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="bbd6f-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="bbd6f-126">mspeapconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="bbd6f-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





