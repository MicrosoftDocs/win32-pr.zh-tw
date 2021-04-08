---
title: LogonDomain (EapType) 元素
description: 瞭解 LogonDomain (EapType) 元素。 這個元素會識別要驗證之使用者或電腦的網域。
ms.assetid: a93793cd-29ee-47f9-8d91-895844c08bae
keywords:
- LogonDomain 元素 EAPHost
topic_type:
- apiref
api_name:
- LogonDomain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3dbbe57bcd29459f6e9807d8f39aedb4faa72a1b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024080"
---
# <a name="logondomain-eaptype-element"></a><span data-ttu-id="6c70b-105">LogonDomain (EapType) 元素</span><span class="sxs-lookup"><span data-stu-id="6c70b-105">LogonDomain (EapType) Element</span></span>

<span data-ttu-id="6c70b-106">**LogonDomain (EapType)** 元素會識別要驗證之使用者或電腦的網域。</span><span class="sxs-lookup"><span data-stu-id="6c70b-106">The **LogonDomain (EapType)** element identifies the domain of the user or machine being authenticated.</span></span>

``` syntax
<xs:element name="LogonDomain
          
        "
    type="string"
 />
```

<span data-ttu-id="6c70b-107">**LogonDomain** 元素是由 [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="6c70b-107">The **LogonDomain** element is defined by the [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c70b-108">備註</span><span class="sxs-lookup"><span data-stu-id="6c70b-108">Remarks</span></span>

<span data-ttu-id="6c70b-109">如果 **LogonDomain (EapType)** 元素不存在，則會使用 winlogon 的網域。</span><span class="sxs-lookup"><span data-stu-id="6c70b-109">If the **LogonDomain (EapType)** element is not present, the domain from winlogon is used.</span></span> <span data-ttu-id="6c70b-110">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="6c70b-110">This element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c70b-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c70b-111">Requirements</span></span>



| <span data-ttu-id="6c70b-112">角色</span><span class="sxs-lookup"><span data-stu-id="6c70b-112">Role</span></span> | <span data-ttu-id="6c70b-113">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="6c70b-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="6c70b-114">用戶端</span><span class="sxs-lookup"><span data-stu-id="6c70b-114">Client</span></span><br/> | <span data-ttu-id="6c70b-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c70b-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6c70b-116">伺服器</span><span class="sxs-lookup"><span data-stu-id="6c70b-116">Server</span></span><br/> | <span data-ttu-id="6c70b-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c70b-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c70b-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c70b-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="6c70b-119">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="6c70b-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6c70b-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="6c70b-120">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="6c70b-121">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="6c70b-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6c70b-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="6c70b-122">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="6c70b-123">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="6c70b-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="6c70b-124">mschapv2userpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="6c70b-124">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





