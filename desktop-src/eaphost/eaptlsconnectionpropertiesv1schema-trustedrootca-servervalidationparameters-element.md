---
title: TrustedRootCA (ServerValidationParameters) 元素-連接
description: 捕捉用戶端信任的根憑證授權單位 (Ca) 的列印經驗。 |TrustedRootCA (ServerValidationParameters) 元素
ms.assetid: 81e3b6ca-6360-42dc-bfd3-298e81e66c1a
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
ms.openlocfilehash: e6f91816ba90300a76545a7a22cea6d037b4e897
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106992759"
---
# <a name="trustedrootca-servervalidationparameters-element-for-connection-properties"></a><span data-ttu-id="556e0-105">連接屬性的 TrustedRootCA (ServerValidationParameters) 元素</span><span class="sxs-lookup"><span data-stu-id="556e0-105">TrustedRootCA (ServerValidationParameters) Element for connection properties</span></span>

<span data-ttu-id="556e0-106">**TrustedRootCA (ServerValidationParameters)** 專案會捕捉用戶端所信任之根憑證授權單位 (ca) 的 thumb 列印。</span><span class="sxs-lookup"><span data-stu-id="556e0-106">The **TrustedRootCA (ServerValidationParameters)** element captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span>

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

<span data-ttu-id="556e0-107">**TrustedRootCA** 元素是由 [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="556e0-107">The **TrustedRootCA** element is defined by the [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="556e0-108">備註</span><span class="sxs-lookup"><span data-stu-id="556e0-108">Remarks</span></span>

<span data-ttu-id="556e0-109">Thumb 列印是包含憑證之 SHA-1 雜湊的十六進位字串。</span><span class="sxs-lookup"><span data-stu-id="556e0-109">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate.</span></span> <span data-ttu-id="556e0-110">**TrustedRootCA** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="556e0-110">The **TrustedRootCA** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="556e0-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="556e0-111">Requirements</span></span>



| <span data-ttu-id="556e0-112">需求</span><span class="sxs-lookup"><span data-stu-id="556e0-112">Requirement</span></span> | <span data-ttu-id="556e0-113">值</span><span class="sxs-lookup"><span data-stu-id="556e0-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="556e0-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="556e0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="556e0-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="556e0-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="556e0-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="556e0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="556e0-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="556e0-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="556e0-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="556e0-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="556e0-119">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="556e0-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="556e0-120">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="556e0-120">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="556e0-121">**架構實例中可能的直接父元素**</span><span class="sxs-lookup"><span data-stu-id="556e0-121">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="556e0-122">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="556e0-122">**ServerValidation (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="556e0-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="556e0-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="556e0-124">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="556e0-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="556e0-125">eaptlsconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="556e0-125">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="556e0-126">eaptlsconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="556e0-126">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





