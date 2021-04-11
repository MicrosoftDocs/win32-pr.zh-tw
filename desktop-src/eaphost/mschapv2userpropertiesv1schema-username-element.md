---
title: 'Username 元素 (CHAP) '
description: 瞭解 Username 元素，這會識別正在驗證的使用者。 請參閱語法範例，並查看其他可用的資源。
ms.assetid: 3dd12864-5e0a-492c-a2c3-28118d21a0f2
keywords:
- Username 元素 EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29065a59e150d2a4295e91b41862250d58e017b5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933613"
---
# <a name="username-element-chap"></a><span data-ttu-id="991bd-105">Username 元素 (CHAP) </span><span class="sxs-lookup"><span data-stu-id="991bd-105">Username element (CHAP)</span></span>

<span data-ttu-id="991bd-106">**Username** 元素會識別要驗證的使用者。</span><span class="sxs-lookup"><span data-stu-id="991bd-106">The **Username** element identifies the user being authenticated.</span></span>

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="remarks"></a><span data-ttu-id="991bd-107">備註</span><span class="sxs-lookup"><span data-stu-id="991bd-107">Remarks</span></span>

<span data-ttu-id="991bd-108">如果 **Username** 元素不存在，則會從 winlogon 取得使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="991bd-108">If the **Username** element is not present, the user name is obtained from winlogon.</span></span> <span data-ttu-id="991bd-109">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="991bd-109">This element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="991bd-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="991bd-110">Requirements</span></span>



| <span data-ttu-id="991bd-111">角色</span><span class="sxs-lookup"><span data-stu-id="991bd-111">Role</span></span> | <span data-ttu-id="991bd-112">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="991bd-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="991bd-113">用戶端</span><span class="sxs-lookup"><span data-stu-id="991bd-113">Client</span></span><br/> | <span data-ttu-id="991bd-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="991bd-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="991bd-115">伺服器</span><span class="sxs-lookup"><span data-stu-id="991bd-115">Server</span></span><br/> | <span data-ttu-id="991bd-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="991bd-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="991bd-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="991bd-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="991bd-118">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="991bd-118">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="991bd-119">mschapv2userpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="991bd-119">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





