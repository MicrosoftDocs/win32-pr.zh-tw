---
description: 識別行動電話通訊網路的名稱和提供者識別碼。
ms.assetid: 007ecad9-23a3-4352-b3e2-c22d0f3f449d
title: 提供者 (DataRoamingPartners) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Provider
api_type:
- Schema
ms.openlocfilehash: b5b36c973bf44175b90e25fd2a141fed3624d8b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112893"
---
# <a name="provider-dataroamingpartners-element"></a><span data-ttu-id="00d9d-103">提供者 (DataRoamingPartners) 元素</span><span class="sxs-lookup"><span data-stu-id="00d9d-103">Provider (DataRoamingPartners) Element</span></span>

<span data-ttu-id="00d9d-104">**提供者 (DataRoamingPartners)** 元素會識別行動電話網路的名稱和提供者識別碼。</span><span class="sxs-lookup"><span data-stu-id="00d9d-104">The **Provider (DataRoamingPartners)** element identifies the name and provider ID for a cellular network.</span></span>

<span data-ttu-id="00d9d-105">此元素具有下列子項目。</span><span class="sxs-lookup"><span data-stu-id="00d9d-105">This element has the following child elements.</span></span>

-   [<span data-ttu-id="00d9d-106">**ProviderID**</span><span class="sxs-lookup"><span data-stu-id="00d9d-106">**ProviderID**</span></span>](schema-providerid-providertype-element.md)
-   [<span data-ttu-id="00d9d-107">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="00d9d-107">**ProviderName**</span></span>](schema-providername-providertype-element.md)

<span data-ttu-id="00d9d-108">可以在 [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) 元素內多次定義這個元素。</span><span class="sxs-lookup"><span data-stu-id="00d9d-108">This element can be defined multiple times within the [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) element.</span></span> <span data-ttu-id="00d9d-109">至少必須定義一次。</span><span class="sxs-lookup"><span data-stu-id="00d9d-109">It must be defined at least once.</span></span>

``` syntax
<xs:element name="Provider"
    type="providerType"
 />
```

<span data-ttu-id="00d9d-110">**Provider** 元素是由 [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="00d9d-110">The **Provider** element is defined by the [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="00d9d-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="00d9d-111">Requirements</span></span>



| <span data-ttu-id="00d9d-112">需求</span><span class="sxs-lookup"><span data-stu-id="00d9d-112">Requirement</span></span> | <span data-ttu-id="00d9d-113">值</span><span class="sxs-lookup"><span data-stu-id="00d9d-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="00d9d-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00d9d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="00d9d-115">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00d9d-115">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="00d9d-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00d9d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="00d9d-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="00d9d-117">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="00d9d-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00d9d-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="00d9d-119">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="00d9d-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="00d9d-120">**DataRoamingPartners**</span><span class="sxs-lookup"><span data-stu-id="00d9d-120">**DataRoamingPartners**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="00d9d-121">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="00d9d-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="00d9d-122">**DataRoamingPartners (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="00d9d-122">**DataRoamingPartners (MBNProfile)**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)
</dt> </dl>

 

 




