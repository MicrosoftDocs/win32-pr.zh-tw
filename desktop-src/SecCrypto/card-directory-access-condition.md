---
description: 指定智慧卡上目錄的存取控制許可權。
ms.assetid: 361d9fa0-286e-4d2c-8452-3b5f48e77779
title: 'CARD_DIRECTORY_ACCESS_CONDITION 列舉 (Cardmod.h .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_DIRECTORY_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: 9879fa73f6bb45b56f433d7bca7765ab5fc0daef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191272"
---
# <a name="card_directory_access_condition-enumeration"></a><span data-ttu-id="7cb1c-103">卡片 \_ 目錄 \_ 存取 \_ 條件列舉</span><span class="sxs-lookup"><span data-stu-id="7cb1c-103">CARD\_DIRECTORY\_ACCESS\_CONDITION enumeration</span></span>

<span data-ttu-id="7cb1c-104">**卡片 \_ 目錄 \_ 存取 \_ 條件** 列舉會指定 [*智慧卡*](../secgloss/s-gly.md)上目錄的存取控制許可權。</span><span class="sxs-lookup"><span data-stu-id="7cb1c-104">The **CARD\_DIRECTORY\_ACCESS\_CONDITION** enumeration specifies access control permissions for a directory on a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7cb1c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cb1c-105">Syntax</span></span>


```C++
typedef enum  { 
  InvalidAc               = 0,
  UserCreateDeleteDirAc   = 1,
  AdminCreateDeleteDirAc  = 2
} CARD_DIRECTORY_ACCESS_CONDITION;
```



## <a name="constants"></a><span data-ttu-id="7cb1c-106">常數</span><span class="sxs-lookup"><span data-stu-id="7cb1c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7cb1c-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span></span>
</dt> <dd>

<span data-ttu-id="7cb1c-108">此值無效。</span><span class="sxs-lookup"><span data-stu-id="7cb1c-108">This value is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="7cb1c-109"><span id="UserCreateDeleteDirAc"></span><span id="usercreatedeletedirac"></span><span id="USERCREATEDELETEDIRAC"></span>**UserCreateDeleteDirAc**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-109"><span id="UserCreateDeleteDirAc"></span><span id="usercreatedeletedirac"></span><span id="USERCREATEDELETEDIRAC"></span>**UserCreateDeleteDirAc**</span></span>
</dt> <dd>

<span data-ttu-id="7cb1c-110">特定使用者可以讀取、寫入及刪除目錄。</span><span class="sxs-lookup"><span data-stu-id="7cb1c-110">Specific users can read, write, and delete the directory.</span></span>

</dd> <dt>

<span data-ttu-id="7cb1c-111"><span id="AdminCreateDeleteDirAc"></span><span id="admincreatedeletedirac"></span><span id="ADMINCREATEDELETEDIRAC"></span>**AdminCreateDeleteDirAc**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-111"><span id="AdminCreateDeleteDirAc"></span><span id="admincreatedeletedirac"></span><span id="ADMINCREATEDELETEDIRAC"></span>**AdminCreateDeleteDirAc**</span></span>
</dt> <dd>

<span data-ttu-id="7cb1c-112">系統管理員可以讀取、寫入及刪除目錄。</span><span class="sxs-lookup"><span data-stu-id="7cb1c-112">Administrators can read, write, and delete the directory.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7cb1c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7cb1c-113">Requirements</span></span>



| <span data-ttu-id="7cb1c-114">需求</span><span class="sxs-lookup"><span data-stu-id="7cb1c-114">Requirement</span></span> | <span data-ttu-id="7cb1c-115">值</span><span class="sxs-lookup"><span data-stu-id="7cb1c-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7cb1c-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7cb1c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7cb1c-117">僅限 windows XP、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7cb1c-117">Windows XP, Windows XP \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7cb1c-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7cb1c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7cb1c-119">僅限 windows Server 2003、Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7cb1c-119">Windows Server 2003, Windows Server 2003 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="7cb1c-120">標頭</span><span class="sxs-lookup"><span data-stu-id="7cb1c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cb1c-121"><dt>Cardmod.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="7cb1c-121"><dt>Cardmod.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cb1c-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7cb1c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cb1c-123">Microsoft 基礎智慧卡密碼編譯服務提供者</span><span class="sxs-lookup"><span data-stu-id="7cb1c-123">Microsoft Base Smart Card Cryptographic Service Provider</span></span>](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[<span data-ttu-id="7cb1c-124">**CardCreateDirectory**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-124">**CardCreateDirectory**</span></span>](/previous-versions/windows/desktop/secsmart/cardcreatedirectory)
</dt> <dt>

[<span data-ttu-id="7cb1c-125">**CardDeleteDirectory**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-125">**CardDeleteDirectory**</span></span>](/previous-versions/windows/desktop/secsmart/carddeletedirectory)
</dt> </dl>

 

 
