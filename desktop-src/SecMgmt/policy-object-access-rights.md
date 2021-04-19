---
description: 列出並描述原則物件的存取類型。
ms.assetid: 592dea65-9da1-4e49-82e4-8e08c451e026
title: 原則物件存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5c762955a4c53015241086b2249c5edbc4f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971192"
---
# <a name="policy-object-access-rights"></a><span data-ttu-id="66d3d-103">原則物件存取權限</span><span class="sxs-lookup"><span data-stu-id="66d3d-103">Policy Object Access Rights</span></span>

<span data-ttu-id="66d3d-104">[**原則**](policy-object.md)物件具有下列物件特定的存取類型：</span><span class="sxs-lookup"><span data-stu-id="66d3d-104">The [**Policy**](policy-object.md) object has the following object-specific access types:</span></span>



| <span data-ttu-id="66d3d-105">存取類型</span><span class="sxs-lookup"><span data-stu-id="66d3d-105">Access type</span></span>                         | <span data-ttu-id="66d3d-106">Description</span><span class="sxs-lookup"><span data-stu-id="66d3d-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66d3d-107">原則 \_ 視圖 \_ 區域 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="66d3d-107">POLICY\_VIEW\_LOCAL\_INFORMATION</span></span>    | <span data-ttu-id="66d3d-108">需要此存取類型才能讀取目標系統的其他安全性原則資訊。</span><span class="sxs-lookup"><span data-stu-id="66d3d-108">This access type is needed to read the target system's miscellaneous security policy information.</span></span> <span data-ttu-id="66d3d-109">這包括預設配額、審核、伺服器狀態和角色資訊，以及信任資訊。</span><span class="sxs-lookup"><span data-stu-id="66d3d-109">This includes the default quota, auditing, server state and role information, and trust information.</span></span> <span data-ttu-id="66d3d-110">列舉受信任的網域、帳戶和 [*許可權*](/windows/desktop/SecGloss/p-gly)也需要此存取類型。</span><span class="sxs-lookup"><span data-stu-id="66d3d-110">This access type is also needed to enumerate trusted domains, accounts, and [*privileges*](/windows/desktop/SecGloss/p-gly).</span></span> |
| <span data-ttu-id="66d3d-111">原則 \_ 取得 \_ 私用 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="66d3d-111">POLICY\_GET\_PRIVATE\_INFORMATION</span></span>   | <span data-ttu-id="66d3d-112">需要此存取類型才能查看敏感性資訊，例如針對信任的網域關聯性所建立的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="66d3d-112">This access type is needed to view sensitive information, such as the names of accounts established for trusted domain relationships.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="66d3d-113">原則 \_ 信任 \_ 管理員</span><span class="sxs-lookup"><span data-stu-id="66d3d-113">POLICY\_TRUST\_ADMIN</span></span>                | <span data-ttu-id="66d3d-114">變更帳戶網域或主域資訊需要此存取類型。</span><span class="sxs-lookup"><span data-stu-id="66d3d-114">This access type is needed to change the account domain or primary domain information.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="66d3d-115">原則 \_ 設定 \_ 預設 \_ 配額 \_ 限制</span><span class="sxs-lookup"><span data-stu-id="66d3d-115">POLICY\_SET\_DEFAULT\_QUOTA\_LIMITS</span></span> | <span data-ttu-id="66d3d-116">設定套用至使用者帳戶的預設系統配額。</span><span class="sxs-lookup"><span data-stu-id="66d3d-116">Set the default system quotas that are applied to user accounts.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="66d3d-117">原則 \_ 建立 \_ 秘密</span><span class="sxs-lookup"><span data-stu-id="66d3d-117">POLICY\_CREATE\_SECRET</span></span>              | <span data-ttu-id="66d3d-118">需要此存取類型才能建立新的私用資料物件。</span><span class="sxs-lookup"><span data-stu-id="66d3d-118">This access type is needed to create a new Private Data object.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="66d3d-119">原則 \_ 建立 \_ 帳戶</span><span class="sxs-lookup"><span data-stu-id="66d3d-119">POLICY\_CREATE\_ACCOUNT</span></span>             | <span data-ttu-id="66d3d-120">建立新的 [**帳戶**](account-object.md) 物件時需要此存取類型。</span><span class="sxs-lookup"><span data-stu-id="66d3d-120">This access type is needed to create a new [**Account**](account-object.md) object.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="66d3d-121">原則 \_ 集 \_ 審核 \_ 需求</span><span class="sxs-lookup"><span data-stu-id="66d3d-121">POLICY\_SET\_AUDIT\_REQUIREMENTS</span></span>    | <span data-ttu-id="66d3d-122">需要此存取類型才能更新系統的審核需求。</span><span class="sxs-lookup"><span data-stu-id="66d3d-122">This access type is needed to update the auditing requirements of the system.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="66d3d-123">原則 \_ 審核 \_ 記錄 \_ 管理員</span><span class="sxs-lookup"><span data-stu-id="66d3d-123">POLICY\_AUDIT\_LOG\_ADMIN</span></span>           | <span data-ttu-id="66d3d-124">需要此存取類型才能變更審核記錄的特性，例如其大小上限或審核記錄的保留期限，或清除記錄檔。</span><span class="sxs-lookup"><span data-stu-id="66d3d-124">This access type is needed to change the characteristics of the audit trail such as its maximum size or the retention period for audit records, or to clear the log.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="66d3d-125">原則 \_ 視圖 \_ 審核 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="66d3d-125">POLICY\_VIEW\_AUDIT\_INFORMATION</span></span>    | <span data-ttu-id="66d3d-126">需要此存取類型才能查看審核記錄或審核需求資訊。</span><span class="sxs-lookup"><span data-stu-id="66d3d-126">This access type is needed to view audit trail or audit requirements information.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="66d3d-127">原則 \_ 伺服器 \_ 管理員</span><span class="sxs-lookup"><span data-stu-id="66d3d-127">POLICY\_SERVER\_ADMIN</span></span>               | <span data-ttu-id="66d3d-128">需要此存取類型才能修改伺服器狀態或 (master/replica) 資訊的角色。</span><span class="sxs-lookup"><span data-stu-id="66d3d-128">This access type is needed to modify the server state or role (master/replica) information.</span></span> <span data-ttu-id="66d3d-129">您也需要變更複本來源和帳戶名稱資訊。</span><span class="sxs-lookup"><span data-stu-id="66d3d-129">It is also needed to change the replica source and account name information.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="66d3d-130">原則 \_ 查閱 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="66d3d-130">POLICY\_LOOKUP\_NAMES</span></span>               | <span data-ttu-id="66d3d-131">需要有此存取類型，才能在名稱和 Sid 之間轉譯。</span><span class="sxs-lookup"><span data-stu-id="66d3d-131">This access type is needed to translate between names and SIDs.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="66d3d-132">原則 \_ 建立 \_ 許可權</span><span class="sxs-lookup"><span data-stu-id="66d3d-132">POLICY\_CREATE\_PRIVILEGE</span></span>           | <span data-ttu-id="66d3d-133">尚不支援。</span><span class="sxs-lookup"><span data-stu-id="66d3d-133">Not yet supported.</span></span>                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="generic-access-masks"></a><span data-ttu-id="66d3d-134">一般存取遮罩</span><span class="sxs-lookup"><span data-stu-id="66d3d-134">Generic Access Masks</span></span>

<span data-ttu-id="66d3d-135">[**原則**](policy-object.md)物件會從一般存取類型發佈下列對應到特定存取類型：</span><span class="sxs-lookup"><span data-stu-id="66d3d-135">The [**Policy**](policy-object.md) object publishes the following mappings from generic access types to specific access types:</span></span>

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                                        POLICY_SERVER_ADMIN

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_LOOKUP_NAMES
```

## <a name="standard-access-types"></a><span data-ttu-id="66d3d-136">標準存取類型</span><span class="sxs-lookup"><span data-stu-id="66d3d-136">Standard Access Types</span></span>

<span data-ttu-id="66d3d-137">此物件不支援 (選擇性) 同步處理標準存取類型。</span><span class="sxs-lookup"><span data-stu-id="66d3d-137">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="66d3d-138">支援所有必要的存取類型。</span><span class="sxs-lookup"><span data-stu-id="66d3d-138">All required access types are supported.</span></span> <span data-ttu-id="66d3d-139">此物件類型所有支援之存取類型的遮罩為：</span><span class="sxs-lookup"><span data-stu-id="66d3d-139">The mask of all supported access types for this object type is:</span></span>

``` syntax
    POLICY_ALL_ACCESS STANDARD_RIGHTS_REQUIRED |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                    POLICY_SERVER_ADMIN
                    POLICY_LOOKUP_NAMES
```

 

 
