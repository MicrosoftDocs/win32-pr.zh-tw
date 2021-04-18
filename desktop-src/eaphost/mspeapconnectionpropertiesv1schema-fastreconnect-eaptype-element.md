---
title: FastReconnect (EapType) 元素
description: 瞭解 FastReconnect (EapType) 元素。 此元素指出是否要執行快速重新連接。
ms.assetid: 075285b0-7b1b-4d3c-af27-a718f3c20394
keywords:
- FastReconnect 元素 EAPHost
topic_type:
- apiref
api_name:
- FastReconnect
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2214519db68b8c95b0e0efa91d68a7cd667b5f87
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106965453"
---
# <a name="fastreconnect-eaptype-element"></a><span data-ttu-id="416c5-105">FastReconnect (EapType) 元素</span><span class="sxs-lookup"><span data-stu-id="416c5-105">FastReconnect (EapType) Element</span></span>

<span data-ttu-id="416c5-106">**FastReconnect (EapType)** 元素指出是否要執行快速重新連接。</span><span class="sxs-lookup"><span data-stu-id="416c5-106">The **FastReconnect (EapType)** element indicates whether to perform a fast reconnect.</span></span>

``` syntax
<xs:element name="FastReconnect"
    type="boolean"
 />
```

<span data-ttu-id="416c5-107">**FastReconnect** 元素是由 [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="416c5-107">The **FastReconnect** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="416c5-108">備註</span><span class="sxs-lookup"><span data-stu-id="416c5-108">Remarks</span></span>

<span data-ttu-id="416c5-109">如果 **FastReconnect** 元素為 TRUE，則 PEAP 會嘗試執行快速重新連線;如果為 FALSE，則 PEAP 會執行完整驗證。</span><span class="sxs-lookup"><span data-stu-id="416c5-109">If the **FastReconnect** element is TRUE, then PEAP attempts to perform a fast reconnect; if FALSE, PEAP performs the full authentication.</span></span> <span data-ttu-id="416c5-110">**FastReconnect** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="416c5-110">The **FastReconnect** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="416c5-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="416c5-111">Requirements</span></span>



| <span data-ttu-id="416c5-112">角色</span><span class="sxs-lookup"><span data-stu-id="416c5-112">Role</span></span> | <span data-ttu-id="416c5-113">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="416c5-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="416c5-114">用戶端</span><span class="sxs-lookup"><span data-stu-id="416c5-114">Client</span></span><br/> | <span data-ttu-id="416c5-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="416c5-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="416c5-116">伺服器</span><span class="sxs-lookup"><span data-stu-id="416c5-116">Server</span></span><br/> | <span data-ttu-id="416c5-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="416c5-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="416c5-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="416c5-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="416c5-119">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="416c5-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="416c5-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="416c5-120">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="416c5-121">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="416c5-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="416c5-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="416c5-122">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="416c5-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="416c5-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="416c5-124">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="416c5-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="416c5-125">mspeapconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="416c5-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="416c5-126">mspeapconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="416c5-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





