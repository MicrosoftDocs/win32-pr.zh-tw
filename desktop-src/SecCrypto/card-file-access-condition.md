---
description: 指定智慧卡上檔案的存取控制許可權。
ms.assetid: 995d959f-30dc-4e5c-be2d-6b447499415a
title: 'CARD_FILE_ACCESS_CONDITION 列舉 (Cardmod.h .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_FILE_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: d3ef9fc81c9ab3bff5f3992c3aedeb3f923648ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991707"
---
# <a name="card_file_access_condition-enumeration"></a><span data-ttu-id="7332d-103">卡片 \_ 檔案 \_ 存取 \_ 條件列舉</span><span class="sxs-lookup"><span data-stu-id="7332d-103">CARD\_FILE\_ACCESS\_CONDITION enumeration</span></span>

<span data-ttu-id="7332d-104">**卡片檔案 \_ \_ 存取 \_ 條件** 列舉會指定 [*智慧卡*](../secgloss/s-gly.md)上檔案的存取控制許可權。</span><span class="sxs-lookup"><span data-stu-id="7332d-104">The **CARD\_FILE\_ACCESS\_CONDITION** enumeration specifies access control permissions for a file on a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7332d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7332d-105">Syntax</span></span>


```C++
typedef enum  { 
  InvalidAc                 = 0,
  EveryoneReadUserWriteAc   = 1,
  UserWriteExecuteAc        = 2,
  EveryoneReadAdminWriteAc  = 3,
  UnknownAc                 = 4
} CARD_FILE_ACCESS_CONDITION;
```



## <a name="constants"></a><span data-ttu-id="7332d-106">常數</span><span class="sxs-lookup"><span data-stu-id="7332d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7332d-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span><span class="sxs-lookup"><span data-stu-id="7332d-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span></span>
</dt> <dd>

<span data-ttu-id="7332d-108">此值無效。</span><span class="sxs-lookup"><span data-stu-id="7332d-108">This value is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="7332d-109"><span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**EveryoneReadUserWriteAc**</span><span class="sxs-lookup"><span data-stu-id="7332d-109"><span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**EveryoneReadUserWriteAc**</span></span>
</dt> <dd>

<span data-ttu-id="7332d-110">每個人都可以讀取檔案。</span><span class="sxs-lookup"><span data-stu-id="7332d-110">Everyone can read the file.</span></span> <span data-ttu-id="7332d-111">特定使用者可以寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="7332d-111">Specific users can write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="7332d-112"><span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**UserWriteExecuteAc**</span><span class="sxs-lookup"><span data-stu-id="7332d-112"><span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**UserWriteExecuteAc**</span></span>
</dt> <dd>

<span data-ttu-id="7332d-113">只有特定使用者可以讀取或寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="7332d-113">Only specific users can read or write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="7332d-114"><span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**EveryoneReadAdminWriteAc**</span><span class="sxs-lookup"><span data-stu-id="7332d-114"><span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**EveryoneReadAdminWriteAc**</span></span>
</dt> <dd>

<span data-ttu-id="7332d-115">每個人都可以讀取檔案。</span><span class="sxs-lookup"><span data-stu-id="7332d-115">Everyone can read the file.</span></span> <span data-ttu-id="7332d-116">系統管理員可以寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="7332d-116">Administrators can write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="7332d-117"><span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**UnknownAc**</span><span class="sxs-lookup"><span data-stu-id="7332d-117"><span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**UnknownAc**</span></span>
</dt> <dd>

<span data-ttu-id="7332d-118">檔案的存取權限不明。</span><span class="sxs-lookup"><span data-stu-id="7332d-118">Access permissions for the file are unknown.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7332d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="7332d-119">Requirements</span></span>



| <span data-ttu-id="7332d-120">需求</span><span class="sxs-lookup"><span data-stu-id="7332d-120">Requirement</span></span> | <span data-ttu-id="7332d-121">值</span><span class="sxs-lookup"><span data-stu-id="7332d-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7332d-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7332d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7332d-123">僅限 windows XP、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7332d-123">Windows XP, Windows XP \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7332d-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7332d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7332d-125">僅限 windows Server 2003、Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7332d-125">Windows Server 2003, Windows Server 2003 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="7332d-126">標頭</span><span class="sxs-lookup"><span data-stu-id="7332d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7332d-127"><dt>Cardmod.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="7332d-127"><dt>Cardmod.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7332d-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7332d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7332d-129">Microsoft 基礎智慧卡密碼編譯服務提供者</span><span class="sxs-lookup"><span data-stu-id="7332d-129">Microsoft Base Smart Card Cryptographic Service Provider</span></span>](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[<span data-ttu-id="7332d-130">**卡片 \_ 檔案 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="7332d-130">**CARD\_FILE\_INFO**</span></span>](/previous-versions/windows/desktop/secsmart/card-file-info)
</dt> <dt>

[<span data-ttu-id="7332d-131">**CardCreateFile**</span><span class="sxs-lookup"><span data-stu-id="7332d-131">**CardCreateFile**</span></span>](/previous-versions/windows/desktop/secsmart/cardcreatefile)
</dt> </dl>

 

 
