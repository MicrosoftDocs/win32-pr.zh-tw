---
description: 描述存取儲存在受保護儲存體中之專案的規則。
ms.assetid: 22aebac3-46e9-4c66-bfaf-e82cf9d494cb
title: 'PST_ACCESSRULE 結構 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 90a04f2f7a34874a8c076fa55b158944399fac2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993599"
---
# <a name="pst_accessrule-structure"></a><span data-ttu-id="e6372-103">PST \_ ACCESSRULE 結構</span><span class="sxs-lookup"><span data-stu-id="e6372-103">PST\_ACCESSRULE structure</span></span>

<span data-ttu-id="e6372-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="e6372-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="e6372-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="e6372-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="e6372-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="e6372-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="e6372-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="e6372-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="e6372-108">描述存取儲存在受保護儲存體中之專案的規則。</span><span class="sxs-lookup"><span data-stu-id="e6372-108">Describes a rule for access to items stored in protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6372-109">語法</span><span class="sxs-lookup"><span data-stu-id="e6372-109">Syntax</span></span>


```C++
typedef struct {
  DWORD            cbSize;
  PST_ACCESSMODE   AccessModeFlags;
  DWORD            cClauses;
  PST_ACCESSCLAUSE *rgClauses;
} PST_ACCESSRULE, *PPST_ACCESSRULE;
```



## <a name="members"></a><span data-ttu-id="e6372-110">成員</span><span class="sxs-lookup"><span data-stu-id="e6372-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="e6372-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="e6372-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="e6372-112">此結構的大小。</span><span class="sxs-lookup"><span data-stu-id="e6372-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="e6372-113">**AccessModeFlags**</span><span class="sxs-lookup"><span data-stu-id="e6372-113">**AccessModeFlags**</span></span>
</dt> <dd>

<span data-ttu-id="e6372-114">一組指定之存取子句所屬的存取模式。</span><span class="sxs-lookup"><span data-stu-id="e6372-114">The access modes to which a specified set of access clauses pertain.</span></span>



| <span data-ttu-id="e6372-115">值</span><span class="sxs-lookup"><span data-stu-id="e6372-115">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="e6372-116">意義</span><span class="sxs-lookup"><span data-stu-id="e6372-116">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <span data-ttu-id="e6372-117"><dt>**PST \_讀取**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="e6372-117"><dt>**PST\_READ**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="e6372-118">讀取存取模式。</span><span class="sxs-lookup"><span data-stu-id="e6372-118">Read access mode.</span></span><br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <span data-ttu-id="e6372-119"><dt>**PST \_寫入**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="e6372-119"><dt>**PST\_WRITE**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="e6372-120">寫入存取模式。</span><span class="sxs-lookup"><span data-stu-id="e6372-120">Write access mode.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e6372-121">**cClauses**</span><span class="sxs-lookup"><span data-stu-id="e6372-121">**cClauses**</span></span>
</dt> <dd>

<span data-ttu-id="e6372-122">**RgClauses** 陣列中的結構數目。</span><span class="sxs-lookup"><span data-stu-id="e6372-122">The number of structures in the **rgClauses** array.</span></span>

</dd> <dt>

<span data-ttu-id="e6372-123">**rgClauses**</span><span class="sxs-lookup"><span data-stu-id="e6372-123">**rgClauses**</span></span>
</dt> <dd>

<span data-ttu-id="e6372-124">[**PST \_ ACCESSCLAUSE**](pst-accessclause.md)結構陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="e6372-124">A pointer to an array of [**PST\_ACCESSCLAUSE**](pst-accessclause.md) structures.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e6372-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6372-125">Requirements</span></span>



| <span data-ttu-id="e6372-126">需求</span><span class="sxs-lookup"><span data-stu-id="e6372-126">Requirement</span></span> | <span data-ttu-id="e6372-127">值</span><span class="sxs-lookup"><span data-stu-id="e6372-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e6372-128">標頭</span><span class="sxs-lookup"><span data-stu-id="e6372-128">Header</span></span><br/> | <dl> <span data-ttu-id="e6372-129"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="e6372-129"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6372-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6372-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6372-131">**PST \_ ACCESSCLAUSE**</span><span class="sxs-lookup"><span data-stu-id="e6372-131">**PST\_ACCESSCLAUSE**</span></span>](pst-accessclause.md)
</dt> <dt>

[<span data-ttu-id="e6372-132">**PST \_ ACCESSRULESET**</span><span class="sxs-lookup"><span data-stu-id="e6372-132">**PST\_ACCESSRULESET**</span></span>](pst-accessruleset.md)
</dt> </dl>

 

 
