---
description: 指定行動電話網路的提供者識別碼。
ms.assetid: 5528dfec-eb1b-4af3-8d7d-03b458e5ae75
title: ProviderID (providerType) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProviderID
api_type:
- Schema
ms.openlocfilehash: 750e6c3f4397f710bb1ccbcea0286be68a89e145
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191441"
---
# <a name="providerid-providertype-element"></a><span data-ttu-id="8aefd-103">ProviderID (providerType) 元素</span><span class="sxs-lookup"><span data-stu-id="8aefd-103">ProviderID (providerType) Element</span></span>

<span data-ttu-id="8aefd-104">**ProviderID (providerType)** 元素會指定行動電話網路的提供者識別碼。</span><span class="sxs-lookup"><span data-stu-id="8aefd-104">The **ProviderID (providerType)** element specifies the provider ID of the cellular network.</span></span>

<span data-ttu-id="8aefd-105">元素是一系列的數位，最多6位數。</span><span class="sxs-lookup"><span data-stu-id="8aefd-105">The element is a sequence of digits with a maximum of 6 digits.</span></span>

<span data-ttu-id="8aefd-106">在 [**提供者**](schema-provider-dataroamingpartners-element.md) 元素內需要這個元素。</span><span class="sxs-lookup"><span data-stu-id="8aefd-106">This element is required within the [**Provider**](schema-provider-dataroamingpartners-element.md) element.</span></span>

``` syntax
<xs:element name="ProviderID"
    type="providerType"
 />
```

<span data-ttu-id="8aefd-107">**ProviderID** 元素是由 [**providerType**](schema-providertype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="8aefd-107">The **ProviderID** element is defined by the [**providerType**](schema-providertype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="8aefd-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="8aefd-108">Requirements</span></span>



| <span data-ttu-id="8aefd-109">需求</span><span class="sxs-lookup"><span data-stu-id="8aefd-109">Requirement</span></span> | <span data-ttu-id="8aefd-110">值</span><span class="sxs-lookup"><span data-stu-id="8aefd-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="8aefd-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8aefd-111">Minimum supported client</span></span><br/> | <span data-ttu-id="8aefd-112">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8aefd-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="8aefd-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8aefd-113">Minimum supported server</span></span><br/> | <span data-ttu-id="8aefd-114">都不支援</span><span class="sxs-lookup"><span data-stu-id="8aefd-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="8aefd-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8aefd-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="8aefd-116">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="8aefd-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="8aefd-117">**providerType**</span><span class="sxs-lookup"><span data-stu-id="8aefd-117">**providerType**</span></span>](schema-providertype-complextype.md)
</dt> <dt>

<span data-ttu-id="8aefd-118">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="8aefd-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="8aefd-119">**提供者 (DataRoamingPartners)**</span><span class="sxs-lookup"><span data-stu-id="8aefd-119">**Provider (DataRoamingPartners)**</span></span>](schema-provider-dataroamingpartners-element.md)
</dt> </dl>

 

 




