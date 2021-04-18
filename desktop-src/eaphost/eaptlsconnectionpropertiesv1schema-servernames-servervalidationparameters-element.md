---
title: 'ServerNames (ServerValidationParameters) 元素 (TLS) '
description: '瞭解 ServerNames (ServerValidationParameters) 元素。 此元素代表以分號分隔的伺服器名稱清單。 |ServerNames (ServerValidationParameters) 元素 (TLS) '
ms.assetid: c6cfcc67-4e6a-4bf0-87d9-37cc1d504598
keywords:
- ServerNames 元素 EAPHost
topic_type:
- apiref
api_name:
- ServerNames
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef94bc650432c4fb87abf00a93841d0d4d42e965
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106976440"
---
# <a name="servernames-servervalidationparameters-element-tls"></a><span data-ttu-id="628e7-106">ServerNames (ServerValidationParameters) 元素 (TLS) </span><span class="sxs-lookup"><span data-stu-id="628e7-106">ServerNames (ServerValidationParameters) element (TLS)</span></span>

<span data-ttu-id="628e7-107">**ServerNames (ServerValidationParameters)** 元素表示以分號分隔的伺服器名稱清單。</span><span class="sxs-lookup"><span data-stu-id="628e7-107">The **ServerNames (ServerValidationParameters)** element represents a list of semicolon delimited server names.</span></span>

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="628e7-108">**ServerNames** 元素是由 [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="628e7-108">The **ServerNames** element is defined by the [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="628e7-109">備註</span><span class="sxs-lookup"><span data-stu-id="628e7-109">Remarks</span></span>

<span data-ttu-id="628e7-110">每個伺服器名稱會以分號分隔，而且可以使用正則運算式來表示。</span><span class="sxs-lookup"><span data-stu-id="628e7-110">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span> <span data-ttu-id="628e7-111">**ServerNames** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="628e7-111">The **ServerNames** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="628e7-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="628e7-112">Requirements</span></span>



| <span data-ttu-id="628e7-113">角色</span><span class="sxs-lookup"><span data-stu-id="628e7-113">Role</span></span> | <span data-ttu-id="628e7-114">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="628e7-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="628e7-115">用戶端</span><span class="sxs-lookup"><span data-stu-id="628e7-115">Client</span></span><br/> | <span data-ttu-id="628e7-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="628e7-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="628e7-117">伺服器</span><span class="sxs-lookup"><span data-stu-id="628e7-117">Server</span></span><br/> | <span data-ttu-id="628e7-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="628e7-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="628e7-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="628e7-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="628e7-120">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="628e7-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="628e7-121">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="628e7-121">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="628e7-122">**架構實例中可能的直接父元素**</span><span class="sxs-lookup"><span data-stu-id="628e7-122">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="628e7-123">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="628e7-123">**ServerValidation (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="628e7-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="628e7-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="628e7-125">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="628e7-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="628e7-126">eaptlsconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="628e7-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="628e7-127">eaptlsconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="628e7-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





