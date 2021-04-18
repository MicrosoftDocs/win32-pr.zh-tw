---
title: 'ServerNames (ServerValidationParameters) 元素 (PEAP) '
description: '瞭解 ServerNames (ServerValidationParameters) 元素。 此元素代表以分號分隔的伺服器名稱清單。 |ServerNames (ServerValidationParameters) 元素 (PEAP) '
ms.assetid: 2595daa1-9f1b-40cf-9219-0e7295fdd5c3
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
ms.openlocfilehash: 40aa7ba317b7ba7c3f7a06cce87ef57c2906fe4b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106976423"
---
# <a name="servernames-servervalidationparameters-element-peap"></a><span data-ttu-id="58fc1-106">ServerNames (ServerValidationParameters) 元素 (PEAP) </span><span class="sxs-lookup"><span data-stu-id="58fc1-106">ServerNames (ServerValidationParameters) element (PEAP)</span></span>

<span data-ttu-id="58fc1-107">**ServerNames (ServerValidationParameters)** 元素表示以分號分隔的伺服器名稱清單。</span><span class="sxs-lookup"><span data-stu-id="58fc1-107">The **ServerNames (ServerValidationParameters)** element represents a list of semicolon delimited server names.</span></span>

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="58fc1-108">**ServerNames** 元素是由 [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="58fc1-108">The **ServerNames** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="58fc1-109">備註</span><span class="sxs-lookup"><span data-stu-id="58fc1-109">Remarks</span></span>

<span data-ttu-id="58fc1-110">每個伺服器名稱會以分號分隔，而且可以使用正則運算式來表示。</span><span class="sxs-lookup"><span data-stu-id="58fc1-110">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span> <span data-ttu-id="58fc1-111">**ServerNames** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="58fc1-111">The **ServerNames** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="58fc1-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="58fc1-112">Requirements</span></span>



| <span data-ttu-id="58fc1-113">角色</span><span class="sxs-lookup"><span data-stu-id="58fc1-113">Role</span></span> | <span data-ttu-id="58fc1-114">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="58fc1-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="58fc1-115">用戶端</span><span class="sxs-lookup"><span data-stu-id="58fc1-115">Client</span></span><br/> | <span data-ttu-id="58fc1-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58fc1-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="58fc1-117">伺服器</span><span class="sxs-lookup"><span data-stu-id="58fc1-117">Server</span></span><br/> | <span data-ttu-id="58fc1-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58fc1-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="58fc1-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58fc1-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="58fc1-120">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="58fc1-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="58fc1-121">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="58fc1-121">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="58fc1-122">**架構實例中可能的直接父元素**</span><span class="sxs-lookup"><span data-stu-id="58fc1-122">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="58fc1-123">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="58fc1-123">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="58fc1-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="58fc1-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="58fc1-125">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="58fc1-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="58fc1-126">mspeapconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="58fc1-126">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="58fc1-127">mspeapconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="58fc1-127">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





