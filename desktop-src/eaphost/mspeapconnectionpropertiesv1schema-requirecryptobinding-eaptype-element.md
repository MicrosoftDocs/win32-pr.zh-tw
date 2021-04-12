---
title: RequireCryptoBinding (EapType) 元素
description: 指出是否要使用支援加密的伺服器進行驗證。
ms.assetid: 6b6a131d-8fce-4a5c-a649-891c4617b0f2
keywords:
- RequireCryptoBinding 元素 EAPHost
topic_type:
- apiref
api_name:
- RequireCryptoBinding
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 63ee456f87205346a935ad047cb8db9828febba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385085"
---
# <a name="requirecryptobinding-eaptype-element"></a><span data-ttu-id="c04b0-104">RequireCryptoBinding (EapType) 元素</span><span class="sxs-lookup"><span data-stu-id="c04b0-104">RequireCryptoBinding (EapType) Element</span></span>

<span data-ttu-id="c04b0-105">**RequireCryptoBinding (EapType)** 元素指出是否要使用支援加密的伺服器進行驗證。</span><span class="sxs-lookup"><span data-stu-id="c04b0-105">The **RequireCryptoBinding (EapType)** element indicates whether to authenticate with servers that support cryptobinding.</span></span>

``` syntax
<xs:element name="RequireCryptoBinding"
    type="boolean"
 />
```

<span data-ttu-id="c04b0-106">**RequireCryptoBinding** 元素是由 [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="c04b0-106">The **RequireCryptoBinding** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="c04b0-107">備註</span><span class="sxs-lookup"><span data-stu-id="c04b0-107">Remarks</span></span>

<span data-ttu-id="c04b0-108">如果 **RequireCryptoBinding** 元素為 TRUE，則 PEAP 會向不支援加密的伺服器進行驗證;若為 FALSE，則 PEAP 只會驗證支援加密的伺服器。</span><span class="sxs-lookup"><span data-stu-id="c04b0-108">If the **RequireCryptoBinding** element is TRUE, then PEAP will authenticate with servers that don't support cryptobinding; if FALSE, then PEAP will only authenticate with servers that support cryptobinding.</span></span> <span data-ttu-id="c04b0-109">**RequireCryptoBinding** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="c04b0-109">The **RequireCryptoBinding** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="c04b0-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="c04b0-110">Requirements</span></span>



| <span data-ttu-id="c04b0-111">需求</span><span class="sxs-lookup"><span data-stu-id="c04b0-111">Requirement</span></span> | <span data-ttu-id="c04b0-112">值</span><span class="sxs-lookup"><span data-stu-id="c04b0-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c04b0-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c04b0-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c04b0-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c04b0-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c04b0-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c04b0-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c04b0-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c04b0-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c04b0-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c04b0-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="c04b0-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="c04b0-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c04b0-119">**EapType**</span><span class="sxs-lookup"><span data-stu-id="c04b0-119">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="c04b0-120">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="c04b0-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c04b0-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="c04b0-121">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="c04b0-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="c04b0-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="c04b0-123">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="c04b0-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="c04b0-124">mspeapconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="c04b0-124">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="c04b0-125">mspeapconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="c04b0-125">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





