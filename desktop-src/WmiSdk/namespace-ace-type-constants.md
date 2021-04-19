---
description: 存取控制專案中的類型欄位 (ACE) ，可判斷 ACE 是否為允許存取或拒絕存取的 ACE。
ms.assetid: a78c72f7-0bc0-4bda-9012-4abe45342d8d
ms.tgt_platform: multiple
title: '命名空間 ACE 類型常數 (Winnt. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Allow
- Deny
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 0c9f1f7e05f663782c0d748ddb296ca36ecbe29c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999384"
---
# <a name="namespace-ace-type-constants"></a><span data-ttu-id="e4491-103">命名空間 ACE 類型常數</span><span class="sxs-lookup"><span data-stu-id="e4491-103">Namespace ACE Type Constants</span></span>

<span data-ttu-id="e4491-104">存取控制專案中的 **類型** 欄位 (ace) ，可判斷 ace 是否為允許存取或拒絕存取的 ace。</span><span class="sxs-lookup"><span data-stu-id="e4491-104">The **Type** field in an access control entry (ACE) that determines whether the ACE is an ACE that allows access or denies access.</span></span>

<dl> <dt>

<span data-ttu-id="e4491-105"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**允許**</span><span class="sxs-lookup"><span data-stu-id="e4491-105"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Allow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4491-106">0</span><span class="sxs-lookup"><span data-stu-id="e4491-106">0</span></span>
</dt> <dt>



<span data-ttu-id="e4491-107">ACE 允許存取命名空間。</span><span class="sxs-lookup"><span data-stu-id="e4491-107">The ACE allows access to the namespace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4491-108"><span id="Deny"></span><span id="deny"></span><span id="DENY"></span>**否認**</span><span class="sxs-lookup"><span data-stu-id="e4491-108"><span id="Deny"></span><span id="deny"></span><span id="DENY"></span>**Deny**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4491-109">1</span><span class="sxs-lookup"><span data-stu-id="e4491-109">1</span></span>
</dt> <dt>



<span data-ttu-id="e4491-110">ACE 會拒絕對命名空間的存取。</span><span class="sxs-lookup"><span data-stu-id="e4491-110">The ACE denies access to the namespace.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4491-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4491-111">Requirements</span></span>



| <span data-ttu-id="e4491-112">需求</span><span class="sxs-lookup"><span data-stu-id="e4491-112">Requirement</span></span> | <span data-ttu-id="e4491-113">值</span><span class="sxs-lookup"><span data-stu-id="e4491-113">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e4491-114">標頭</span><span class="sxs-lookup"><span data-stu-id="e4491-114">Header</span></span><br/> | <dl> <span data-ttu-id="e4491-115"><dt>Winnt。h</dt></span><span class="sxs-lookup"><span data-stu-id="e4491-115"><dt>Winnt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4491-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4491-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4491-117">WMI 安全性常數</span><span class="sxs-lookup"><span data-stu-id="e4491-117">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="e4491-118">設定命名空間安全描述項</span><span class="sxs-lookup"><span data-stu-id="e4491-118">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="e4491-119">建立命名空間安全性的繼承</span><span class="sxs-lookup"><span data-stu-id="e4491-119">Establishing Inheritance of Namespace Security</span></span>](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[<span data-ttu-id="e4491-120">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="e4491-120">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

 




