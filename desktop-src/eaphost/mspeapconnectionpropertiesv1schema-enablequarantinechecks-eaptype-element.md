---
title: EnableQuarantineChecks (EapType) 元素
description: 瞭解 EnableQuarantineChecks (EapType) 元素。 此元素指出 (NAP) 檢查是否執行網路存取保護。
ms.assetid: bd5c7efc-f857-4e21-9cd8-0a1cbe5a87d8
keywords:
- EnableQuarantineChecks 元素 EAPHost
topic_type:
- apiref
api_name:
- EnableQuarantineChecks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0becd1add038bb91307095eaf5cd0743d383632b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933631"
---
# <a name="enablequarantinechecks-eaptype-element"></a><span data-ttu-id="17a81-105">EnableQuarantineChecks (EapType) 元素</span><span class="sxs-lookup"><span data-stu-id="17a81-105">EnableQuarantineChecks (EapType) Element</span></span>

<span data-ttu-id="17a81-106">**EnableQuarantineChecks (EapType)** 元素指出是否 (NAP) 檢查來執行網路存取保護。</span><span class="sxs-lookup"><span data-stu-id="17a81-106">The **EnableQuarantineChecks (EapType)** element indicates whether to perform Network Access Protection (NAP) checks.</span></span>

``` syntax
<xs:element name="EnableQuarantineChecks"
    type="boolean"
 />
```

<span data-ttu-id="17a81-107">**EnableQuarantineChecks** 元素是由 [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="17a81-107">The **EnableQuarantineChecks** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="17a81-108">備註</span><span class="sxs-lookup"><span data-stu-id="17a81-108">Remarks</span></span>

<span data-ttu-id="17a81-109">如果 **EnableQuarantineChecks** 元素為 TRUE，則 PEAP 會執行 NAP 檢查;若為 FALSE，PEAP 將不會執行 NAP 檢查。</span><span class="sxs-lookup"><span data-stu-id="17a81-109">If the **EnableQuarantineChecks** element is TRUE, then PEAP will perform NAP checks; if FALSE, PEAP will not perform NAP checks.</span></span> <span data-ttu-id="17a81-110">**EnableQuarantineChecks** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="17a81-110">The **EnableQuarantineChecks** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="17a81-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="17a81-111">Requirements</span></span>



| <span data-ttu-id="17a81-112">角色</span><span class="sxs-lookup"><span data-stu-id="17a81-112">Role</span></span> | <span data-ttu-id="17a81-113">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="17a81-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="17a81-114">用戶端</span><span class="sxs-lookup"><span data-stu-id="17a81-114">Client</span></span><br/> | <span data-ttu-id="17a81-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17a81-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="17a81-116">伺服器</span><span class="sxs-lookup"><span data-stu-id="17a81-116">Server</span></span><br/> | <span data-ttu-id="17a81-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17a81-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="17a81-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17a81-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="17a81-119">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="17a81-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="17a81-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="17a81-120">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="17a81-121">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="17a81-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="17a81-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="17a81-122">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="17a81-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="17a81-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="17a81-124">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="17a81-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="17a81-125">mspeapconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="17a81-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="17a81-126">mspeapconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="17a81-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





