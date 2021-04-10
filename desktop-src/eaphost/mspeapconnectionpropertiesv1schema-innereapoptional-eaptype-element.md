---
title: InnerEapOptional (EapType) 元素
description: 瞭解 InnerEapOptional (EapType) 元素。 此元素會指出是否要執行來賓存取。
ms.assetid: 2d314c89-5415-407f-84c3-c4c5c8957b39
keywords:
- InnerEapOptional 元素 EAPHost
topic_type:
- apiref
api_name:
- InnerEapOptional
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be63845f389936656172b4cbb4e42de659bbf0e1
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093292"
---
# <a name="innereapoptional-eaptype-element"></a><span data-ttu-id="780e2-105">InnerEapOptional (EapType) 元素</span><span class="sxs-lookup"><span data-stu-id="780e2-105">InnerEapOptional (EapType) Element</span></span>

<span data-ttu-id="780e2-106">**InnerEapOptional (EapType)** 元素指出是否要執行來賓存取。</span><span class="sxs-lookup"><span data-stu-id="780e2-106">The **InnerEapOptional (EapType)** element indicates whether to perform GUEST access.</span></span>

``` syntax
<xs:element name="InnerEapOptional"
    type="boolean"
 />
```

<span data-ttu-id="780e2-107">**InnerEapOptional** 元素是由 [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="780e2-107">The **InnerEapOptional** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="780e2-108">備註</span><span class="sxs-lookup"><span data-stu-id="780e2-108">Remarks</span></span>

<span data-ttu-id="780e2-109">如果 **InnerEapOptional** 專案是 TRUE，則 [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) 元素必須存在，並且描述內部方法和其設定;若為 FALSE，則 PEAP 會執行來賓存取。</span><span class="sxs-lookup"><span data-stu-id="780e2-109">If the **InnerEapOptional** element is TRUE, then the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be present and describe the inner method and it's configuration; if FALSE, then PEAP will perform GUEST access.</span></span> <span data-ttu-id="780e2-110">**InnerEapOptional** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="780e2-110">The **InnerEapOptional** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="780e2-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="780e2-111">Requirements</span></span>



| <span data-ttu-id="780e2-112">角色</span><span class="sxs-lookup"><span data-stu-id="780e2-112">Role</span></span> | <span data-ttu-id="780e2-113">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="780e2-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="780e2-114">用戶端</span><span class="sxs-lookup"><span data-stu-id="780e2-114">Client</span></span><br/> | <span data-ttu-id="780e2-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="780e2-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="780e2-116">伺服器</span><span class="sxs-lookup"><span data-stu-id="780e2-116">Server</span></span><br/> | <span data-ttu-id="780e2-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="780e2-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="780e2-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="780e2-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="780e2-119">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="780e2-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="780e2-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="780e2-120">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="780e2-121">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="780e2-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="780e2-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="780e2-122">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="780e2-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="780e2-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="780e2-124">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="780e2-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="780e2-125">mspeapconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="780e2-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="780e2-126">mspeapconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="780e2-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





