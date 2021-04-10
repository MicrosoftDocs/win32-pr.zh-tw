---
title: 密碼 (EapType) 元素
description: 深入瞭解密碼 (EapType) 元素。 這個元素會識別要驗證之使用者或電腦的密碼。
ms.assetid: d3ad95b8-2d98-420f-a680-a83b49ae2992
keywords:
- 密碼元素 EAPHost
topic_type:
- apiref
api_name:
- Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6da29146be7ed2f0c17d7311f79921b44cd0929e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024110"
---
# <a name="password-eaptype-element"></a><span data-ttu-id="f171f-105">密碼 (EapType) 元素</span><span class="sxs-lookup"><span data-stu-id="f171f-105">Password (EapType) Element</span></span>

<span data-ttu-id="f171f-106">**密碼 (EapType)** 元素會識別要驗證之使用者或電腦的密碼。</span><span class="sxs-lookup"><span data-stu-id="f171f-106">The **Password (EapType)** element identifies the password of the user or machine being authenticated.</span></span>

``` syntax
<xs:element name="Password"
    type="string"
 />
```

<span data-ttu-id="f171f-107">**Password** 元素是由 [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="f171f-107">The **Password** element is defined by the [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="f171f-108">備註</span><span class="sxs-lookup"><span data-stu-id="f171f-108">Remarks</span></span>

<span data-ttu-id="f171f-109">如果 **密碼 (EapType)** 元素不存在，則會從 winlogon 取得密碼雜湊。</span><span class="sxs-lookup"><span data-stu-id="f171f-109">If the **Password (EapType)** element is not present, the password hash is obtained from winlogon.</span></span> <span data-ttu-id="f171f-110">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="f171f-110">This element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="f171f-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="f171f-111">Requirements</span></span>



| <span data-ttu-id="f171f-112">角色</span><span class="sxs-lookup"><span data-stu-id="f171f-112">Role</span></span> | <span data-ttu-id="f171f-113">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="f171f-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="f171f-114">用戶端</span><span class="sxs-lookup"><span data-stu-id="f171f-114">Client</span></span><br/> | <span data-ttu-id="f171f-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f171f-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f171f-116">伺服器</span><span class="sxs-lookup"><span data-stu-id="f171f-116">Server</span></span><br/> | <span data-ttu-id="f171f-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f171f-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f171f-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f171f-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="f171f-119">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="f171f-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f171f-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="f171f-120">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="f171f-121">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="f171f-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f171f-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="f171f-122">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="f171f-123">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="f171f-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f171f-124">mschapv2userpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="f171f-124">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





