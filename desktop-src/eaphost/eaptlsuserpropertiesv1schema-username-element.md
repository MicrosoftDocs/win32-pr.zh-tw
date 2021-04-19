---
title: " (TLS) 的 Username 元素"
description: 瞭解 Username 元素。 這個元素會捕捉要在 EAP-Identity 回應中傳送的使用者名稱。
ms.assetid: dda4a7dd-36ba-418d-9b26-2818ef20854d
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
ms.openlocfilehash: 2975b425bc760979b33d83182d94469532944e46
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106991298"
---
# <a name="username-element-tls"></a><span data-ttu-id="4b115-105"> (TLS) 的 Username 元素</span><span class="sxs-lookup"><span data-stu-id="4b115-105">Username element (TLS)</span></span>

<span data-ttu-id="4b115-106">**Username** 元素會捕捉要在 EAP-Identity 回應中傳送的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="4b115-106">The **Username** element captures the user name to be sent in the EAP-Identity response.</span></span>

<span data-ttu-id="4b115-107">如果 **Username** 專案不存在，則 eap-tls 會使用 [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) 元素中所參考之憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b115-107">If the **Username** element is absent, then EAP-TLS uses the name in the certificate referred to in the [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) element.</span></span>

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="requirements"></a><span data-ttu-id="4b115-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b115-108">Requirements</span></span>



| <span data-ttu-id="4b115-109">角色</span><span class="sxs-lookup"><span data-stu-id="4b115-109">Role</span></span> | <span data-ttu-id="4b115-110">支援的最低 OS 版本</span><span class="sxs-lookup"><span data-stu-id="4b115-110">Minimum supported OS versions</span></span> |
|------|-------------------------------|
| <span data-ttu-id="4b115-111">用戶端</span><span class="sxs-lookup"><span data-stu-id="4b115-111">Client</span></span><br/> | <span data-ttu-id="4b115-112">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b115-112">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4b115-113">伺服器</span><span class="sxs-lookup"><span data-stu-id="4b115-113">Server</span></span><br/> | <span data-ttu-id="4b115-114">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b115-114">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4b115-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b115-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b115-116">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="4b115-116">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="4b115-117">eaptlsuserpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="4b115-117">eaptlsuserpropertiesv1 Schema</span></span>](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





