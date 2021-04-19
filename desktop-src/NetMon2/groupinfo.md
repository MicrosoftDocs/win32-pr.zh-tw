---
description: 建立組名及其控制碼的關聯。
ms.assetid: 76f3fe37-cf85-42ab-8f9e-3ab2c6053dcd
title: 'GROUPINFO 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GROUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5152b0a621a34e49d6f1024a81b7e91aed94a06b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986299"
---
# <a name="groupinfo-structure"></a><span data-ttu-id="9ce0b-103">GROUPINFO 結構</span><span class="sxs-lookup"><span data-stu-id="9ce0b-103">GROUPINFO structure</span></span>

<span data-ttu-id="9ce0b-104">**GROUPINFO** 結構會將組名及其控制碼相關聯。</span><span class="sxs-lookup"><span data-stu-id="9ce0b-104">The **GROUPINFO** structure associates a group name and its handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ce0b-105">語法</span><span class="sxs-lookup"><span data-stu-id="9ce0b-105">Syntax</span></span>


```C++
typedef struct {
  char   szGroupName[EXPERTGROUPNAMELENGTH+1];
  HGROUP hGroup;
} GROUPINFO, *PGROUPINFO;
```



## <a name="members"></a><span data-ttu-id="9ce0b-106">成員</span><span class="sxs-lookup"><span data-stu-id="9ce0b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9ce0b-107">**szGroupName**</span><span class="sxs-lookup"><span data-stu-id="9ce0b-107">**szGroupName**</span></span>
</dt> <dd>

<span data-ttu-id="9ce0b-108">**在擁有組結構中** 的陣列遞增值。</span><span class="sxs-lookup"><span data-stu-id="9ce0b-108">Incremented value of an array in the **GROUPNAME** structure.</span></span>

</dd> <dt>

<span data-ttu-id="9ce0b-109">**hGroup**</span><span class="sxs-lookup"><span data-stu-id="9ce0b-109">**hGroup**</span></span>
</dt> <dd>

<span data-ttu-id="9ce0b-110">群組的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9ce0b-110">Handle to a group.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ce0b-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ce0b-111">Requirements</span></span>



| <span data-ttu-id="9ce0b-112">需求</span><span class="sxs-lookup"><span data-stu-id="9ce0b-112">Requirement</span></span> | <span data-ttu-id="9ce0b-113">值</span><span class="sxs-lookup"><span data-stu-id="9ce0b-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9ce0b-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9ce0b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="9ce0b-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ce0b-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9ce0b-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9ce0b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="9ce0b-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ce0b-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9ce0b-118">標頭</span><span class="sxs-lookup"><span data-stu-id="9ce0b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ce0b-119"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="9ce0b-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




