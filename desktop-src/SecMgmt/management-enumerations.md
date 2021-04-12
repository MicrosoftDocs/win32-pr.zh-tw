---
description: 列出 LSA 原則管理函數使用的列舉。
ms.assetid: f4fd2a61-61bc-44d2-b01f-3ca07699bcb8
title: 安全性管理列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39bec2cdd731e2a3befe75e543f692d93bc5d9ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192937"
---
# <a name="security-management-enumerations"></a><span data-ttu-id="ae481-103">安全性管理列舉</span><span class="sxs-lookup"><span data-stu-id="ae481-103">Security Management Enumerations</span></span>

<span data-ttu-id="ae481-104">安全性管理列舉包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="ae481-104">The security management enumerations include the following:</span></span>

-   [<span data-ttu-id="ae481-105">LSA 原則列舉</span><span class="sxs-lookup"><span data-stu-id="ae481-105">LSA Policy Enumerations</span></span>](#lsa-policy-enumerations)
-   [<span data-ttu-id="ae481-106">更安全的列舉</span><span class="sxs-lookup"><span data-stu-id="ae481-106">Safer Enumerations</span></span>](#safer-enumerations)

## <a name="lsa-policy-enumerations"></a><span data-ttu-id="ae481-107">LSA 原則列舉</span><span class="sxs-lookup"><span data-stu-id="ae481-107">LSA Policy Enumerations</span></span>

<span data-ttu-id="ae481-108">LSA 原則管理函數會使用下列列舉類型。</span><span class="sxs-lookup"><span data-stu-id="ae481-108">The following enumeration types are used by the LSA policy management functions.</span></span>



| <span data-ttu-id="ae481-109">列舉型別</span><span class="sxs-lookup"><span data-stu-id="ae481-109">Enumeration</span></span>                                                                               | <span data-ttu-id="ae481-110">描述</span><span class="sxs-lookup"><span data-stu-id="ae481-110">Description</span></span>                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae481-111">**原則 \_ 審核 \_ 事件 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="ae481-111">**POLICY\_AUDIT\_EVENT\_TYPE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_audit_event_type)                             | <span data-ttu-id="ae481-112">定義系統可以審核的事件種類。</span><span class="sxs-lookup"><span data-stu-id="ae481-112">Defines the types of events the system can audit.</span></span>                                                                                     |
| [<span data-ttu-id="ae481-113">**原則 \_ 資訊 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="ae481-113">**POLICY\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class)                            | <span data-ttu-id="ae481-114">定義可以設定或查詢 [**原則**](policy-object.md) 物件的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="ae481-114">Defines the types of information that can be set or queried for a [**Policy**](policy-object.md) object.</span></span>                             |
| [<span data-ttu-id="ae481-115">**原則 \_ LSA \_ 伺服器 \_ 角色**</span><span class="sxs-lookup"><span data-stu-id="ae481-115">**POLICY\_LSA\_SERVER\_ROLE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_lsa_server_role)                               | <span data-ttu-id="ae481-116">指出 LSA 伺服器的角色。</span><span class="sxs-lookup"><span data-stu-id="ae481-116">Indicate the role of an LSA server.</span></span>                                                                                                   |
| [<span data-ttu-id="ae481-117">**原則 \_ 通知 \_ 資訊 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="ae481-117">**POLICY\_NOTIFICATION\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_notification_information_class) | <span data-ttu-id="ae481-118">定義您的應用程式可以要求變更通知的原則資訊和原則網域資訊類型。</span><span class="sxs-lookup"><span data-stu-id="ae481-118">Defines the types of policy information and policy domain information for which your application can request notification of changes.</span></span> |
| [<span data-ttu-id="ae481-119">**原則 \_ 伺服器 \_ 啟用 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="ae481-119">**POLICY\_SERVER\_ENABLE\_STATE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_server_enable_state)                       | <span data-ttu-id="ae481-120">代表 LSA 伺服器的狀態，也就是啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="ae481-120">Represents the state of the LSA server, that is, whether it is enabled or disabled.</span></span>                                                   |
| [<span data-ttu-id="ae481-121">**受信任的 \_ 資訊 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="ae481-121">**TRUSTED\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-trusted_information_class)                          | <span data-ttu-id="ae481-122">定義可以針對受信任的網域設定或查詢的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="ae481-122">Defines the types of information that can be set or queried for a trusted domain.</span></span>                                                     |



 

## <a name="safer-enumerations"></a><span data-ttu-id="ae481-123">更安全的列舉</span><span class="sxs-lookup"><span data-stu-id="ae481-123">Safer Enumerations</span></span>

<span data-ttu-id="ae481-124">[更安全](safer.md) 地使用下列列舉類型。</span><span class="sxs-lookup"><span data-stu-id="ae481-124">[Safer](safer.md) uses the following enumerated types.</span></span>



| <span data-ttu-id="ae481-125">Name</span><span class="sxs-lookup"><span data-stu-id="ae481-125">Name</span></span>                                                               | <span data-ttu-id="ae481-126">描述</span><span class="sxs-lookup"><span data-stu-id="ae481-126">Description</span></span>                                                                                                                                                                                      |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae481-127">**更安全的 \_ 識別 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="ae481-127">**SAFER\_IDENTIFICATION\_TYPES**</span></span>](/windows/desktop/api/WinSafer/ne-winsafer-safer_identification_types) | <span data-ttu-id="ae481-128">列舉類型，定義可由 [**更安全的 \_ 識別 \_ 標頭**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) 結構識別的識別規則結構的可能類型。</span><span class="sxs-lookup"><span data-stu-id="ae481-128">Enumeration type that defines the possible types of identification rule structures that can be identified by the [**SAFER\_IDENTIFICATION\_HEADER**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) structure.</span></span> |
| [<span data-ttu-id="ae481-129">**更安全的 \_ 物件 \_ 資訊 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="ae481-129">**SAFER\_OBJECT\_INFO\_CLASS**</span></span>](/windows/desktop/api/WinSafer/ne-winsafer-safer_object_info_class)      | <span data-ttu-id="ae481-130">列舉類型，定義針對較安全物件所要求的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="ae481-130">Enumeration type that defines the type of information requested about a Safer object.</span></span>                                                                                                            |
| [<span data-ttu-id="ae481-131">**更安全的 \_ 原則 \_ 資訊 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="ae481-131">**SAFER\_POLICY\_INFO\_CLASS**</span></span>](/windows/desktop/api/WinSafer/ne-winsafer-safer_policy_info_class)      | <span data-ttu-id="ae481-132">列舉類型，定義可以查詢原則的方式。</span><span class="sxs-lookup"><span data-stu-id="ae481-132">Enumeration type that defines the ways in which a policy may be queried.</span></span>                                                                                                                         |



 

 

 



