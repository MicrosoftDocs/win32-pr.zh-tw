---
title: 'EDB_RSTMAP 結構 (Ntdsbcli .h) '
description: 搭配 DsRestoreRegister 函式使用，將已備份的資料庫對應至新的資料庫。
ms.assetid: b2c5d30a-3617-4807-82e8-57f7179b817c
ms.tgt_platform: multiple
keywords:
- EDB_RSTMAP 結構 Active Directory
- PEDB_RSTMAP 結構指標 Active Directory
topic_type:
- apiref
api_name:
- EDB_RSTMAP
- EDB_RSTMAPA
- EDB_RSTMAPW
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be2c960ab7ebc687508131deac6cd8e7b99bbe81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025213"
---
# <a name="edb_rstmap-structure"></a><span data-ttu-id="2e0b7-105">EDB \_ RSTMAP 結構</span><span class="sxs-lookup"><span data-stu-id="2e0b7-105">EDB\_RSTMAP structure</span></span>

<span data-ttu-id="2e0b7-106">**EDB \_ RSTMAP** 結構會搭配 [**DsRestoreRegister**](dsrestoreregister.md)函數使用，以將備份的資料庫對應至新的資料庫。</span><span class="sxs-lookup"><span data-stu-id="2e0b7-106">The **EDB\_RSTMAP** structure is used with the [**DsRestoreRegister**](dsrestoreregister.md) function to map a backed up database to a new database.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e0b7-107">語法</span><span class="sxs-lookup"><span data-stu-id="2e0b7-107">Syntax</span></span>


```C++
typedef struct {
  LPTSTR szDatabaseName;
  LPTSTR szNewDatabaseName;
} EDB_RSTMAP, *PEDB_RSTMAP;
```



## <a name="members"></a><span data-ttu-id="2e0b7-108">成員</span><span class="sxs-lookup"><span data-stu-id="2e0b7-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2e0b7-109">**szDatabaseName**</span><span class="sxs-lookup"><span data-stu-id="2e0b7-109">**szDatabaseName**</span></span>
</dt> <dd>

<span data-ttu-id="2e0b7-110">以 null 結束的字串指標，其中包含備份時資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e0b7-110">Pointer to a null-terminated string that contains the name of the database when it was backed up.</span></span>

</dd> <dt>

<span data-ttu-id="2e0b7-111">**szNewDatabaseName**</span><span class="sxs-lookup"><span data-stu-id="2e0b7-111">**szNewDatabaseName**</span></span>
</dt> <dd>

<span data-ttu-id="2e0b7-112">以 null 結束的字串指標，其中包含資料庫的新名稱（如果適用的話），包括新的位置。</span><span class="sxs-lookup"><span data-stu-id="2e0b7-112">Pointer to a null-terminated string that contains the new name of the database, including its new location, when applicable.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e0b7-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e0b7-113">Requirements</span></span>



| <span data-ttu-id="2e0b7-114">需求</span><span class="sxs-lookup"><span data-stu-id="2e0b7-114">Requirement</span></span> | <span data-ttu-id="2e0b7-115">值</span><span class="sxs-lookup"><span data-stu-id="2e0b7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e0b7-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2e0b7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2e0b7-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e0b7-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="2e0b7-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2e0b7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2e0b7-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e0b7-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="2e0b7-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2e0b7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e0b7-121"><dt>Ntdsbcli。h</dt></span><span class="sxs-lookup"><span data-stu-id="2e0b7-121"><dt>Ntdsbcli.h</dt></span></span> </dl> |
| <span data-ttu-id="2e0b7-122">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="2e0b7-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2e0b7-123">**EDB \_RSTMAPW** (Unicode) 和 **EDB \_ RSTMAPA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="2e0b7-123">**EDB\_RSTMAPW** (Unicode) and **EDB\_RSTMAPA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="2e0b7-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e0b7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e0b7-125">**DsRestoreRegister**</span><span class="sxs-lookup"><span data-stu-id="2e0b7-125">**DsRestoreRegister**</span></span>](dsrestoreregister.md)
</dt> <dt>

[<span data-ttu-id="2e0b7-126">目錄備份結構</span><span class="sxs-lookup"><span data-stu-id="2e0b7-126">Directory Backup Structures</span></span>](directory-backup-structures.md)
</dt> </dl>

 

 





