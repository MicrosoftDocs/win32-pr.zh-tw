---
title: AcceptServerName
description: 指出伺服器名稱是否根據 ServerNames (ServerValidationParameters) 專案中指定的名稱字串進行驗證。 |AcceptServerName
ms.assetid: 440a46ae-7fef-4e97-9fd7-cbd20143597b
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
ms.openlocfilehash: beb12da9897cc0e77480f609edee632c135b5c5d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196008"
---
# <a name="acceptservername"></a><span data-ttu-id="e41a4-105">AcceptServerName</span><span class="sxs-lookup"><span data-stu-id="e41a4-105">AcceptServerName</span></span>

<span data-ttu-id="e41a4-106">**AcceptServerName (EapType)** 元素指出伺服器名稱是否會根據 [**ServerNames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)元素中指定的名稱字串進行驗證。</span><span class="sxs-lookup"><span data-stu-id="e41a4-106">The **AcceptServerName (EapType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    maxOccurs="1"
    ref="extendedTLS: AcceptServerName"
 />
```

<span data-ttu-id="e41a4-107">元素是由 [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="e41a4-107">The element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="e41a4-108">備註</span><span class="sxs-lookup"><span data-stu-id="e41a4-108">Remarks</span></span>

<span data-ttu-id="e41a4-109">**AcceptServerName** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="e41a4-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="e41a4-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="e41a4-110">Requirements</span></span>



| <span data-ttu-id="e41a4-111">需求</span><span class="sxs-lookup"><span data-stu-id="e41a4-111">Requirement</span></span> | <span data-ttu-id="e41a4-112">值</span><span class="sxs-lookup"><span data-stu-id="e41a4-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e41a4-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e41a4-113">Minimum supported client</span></span><br/> | <span data-ttu-id="e41a4-114">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e41a4-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e41a4-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e41a4-115">Minimum supported server</span></span><br/> | <span data-ttu-id="e41a4-116">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e41a4-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e41a4-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e41a4-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="e41a4-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="e41a4-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e41a4-119">**EapType**</span><span class="sxs-lookup"><span data-stu-id="e41a4-119">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="e41a4-120">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="e41a4-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e41a4-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="e41a4-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="e41a4-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="e41a4-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="e41a4-123">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="e41a4-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="e41a4-124">eaptlsconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="e41a4-124">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="e41a4-125">eaptlsconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="e41a4-125">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e41a4-126">**AcceptServerName (EapType)**</span><span class="sxs-lookup"><span data-stu-id="e41a4-126">**AcceptServerName (EapType)**</span></span>](eaptlsconnectionpropertiesv2schema-acceptservername-eaptype-element.md)
</dt> </dl>

 

 





