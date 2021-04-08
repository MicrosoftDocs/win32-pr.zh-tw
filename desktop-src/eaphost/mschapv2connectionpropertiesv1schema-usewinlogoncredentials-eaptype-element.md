---
title: UseWinLogonCredentials (EapType) 元素
description: 瞭解 UseWinLogonCredentials (EapType) 元素。 此元素控制 winlogin 認證的使用。
ms.assetid: 8ebd87ce-7d2b-4305-b50c-239bb9c7af75
keywords:
- UseWinLogonCredentials 元素 EAPHost
topic_type:
- apiref
api_name:
- UseWinLogonCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f17520d4eaee64d3dd9809ecb465ca8e39690fc4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683125"
---
# <a name="usewinlogoncredentials-eaptype-element"></a><span data-ttu-id="12abb-105">UseWinLogonCredentials (EapType) 元素</span><span class="sxs-lookup"><span data-stu-id="12abb-105">UseWinLogonCredentials (EapType) Element</span></span>

<span data-ttu-id="12abb-106">**UseWinLogonCredentials (EapType)** 元素會控制 winlogin 認證的使用。</span><span class="sxs-lookup"><span data-stu-id="12abb-106">The **UseWinLogonCredentials (EapType)** element controls use of the winlogin credentials.</span></span>

``` syntax
<xs:element name="UseWinLogonCredentials"
    type="boolean"
 />
```

<span data-ttu-id="12abb-107">**UseWinLogonCredentials** 元素是由 [**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="12abb-107">The **UseWinLogonCredentials** element is defined by the [**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="12abb-108">備註</span><span class="sxs-lookup"><span data-stu-id="12abb-108">Remarks</span></span>

<span data-ttu-id="12abb-109">若為 TRUE，則表示 EAP MS-CHAPv2 從 winlogon 取得認證。</span><span class="sxs-lookup"><span data-stu-id="12abb-109">If TRUE, then EAP MS-CHAPv2 obtains credentials from winlogon.</span></span> <span data-ttu-id="12abb-110">如果為 FALSE，則表示 EAP MS-CHAPv2 取得使用者的認證。</span><span class="sxs-lookup"><span data-stu-id="12abb-110">If FALSE, then EAP MS-CHAPv2 obtains credentials from the user.</span></span> <span data-ttu-id="12abb-111">**UseWinLogonCredentials (EapType)** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="12abb-111">The **UseWinLogonCredentials (EapType)** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="12abb-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="12abb-112">Requirements</span></span>



| <span data-ttu-id="12abb-113">角色</span><span class="sxs-lookup"><span data-stu-id="12abb-113">Role</span></span> | <span data-ttu-id="12abb-114">支援的最低 OS 版本</span><span class="sxs-lookup"><span data-stu-id="12abb-114">Minimum supported OS versions</span></span> |
|------|-------------------------------|
| <span data-ttu-id="12abb-115">用戶端</span><span class="sxs-lookup"><span data-stu-id="12abb-115">Client</span></span><br/> | <span data-ttu-id="12abb-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12abb-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="12abb-117">伺服器</span><span class="sxs-lookup"><span data-stu-id="12abb-117">Server</span></span><br/> | <span data-ttu-id="12abb-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12abb-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="12abb-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12abb-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="12abb-120">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="12abb-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="12abb-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="12abb-121">**EapType**</span></span>](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="12abb-122">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="12abb-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="12abb-123">**EapType**</span><span class="sxs-lookup"><span data-stu-id="12abb-123">**EapType**</span></span>](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="12abb-124">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="12abb-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="12abb-125">mschapv2connectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="12abb-125">mschapv2connectionpropertiesv1 Schema</span></span>](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





