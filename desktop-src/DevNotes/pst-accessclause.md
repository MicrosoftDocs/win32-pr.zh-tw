---
description: 包含受保護儲存體之存取子句的相關資訊。
ms.assetid: 59634ada-4879-4ae7-b757-dfa6a88549af
title: 'PST_ACCESSCLAUSE 結構 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSCLAUSE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 3536b92bf1d014090f124976b8f4a16e25beb444
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991553"
---
# <a name="pst_accessclause-structure"></a><span data-ttu-id="b3f84-103">PST \_ ACCESSCLAUSE 結構</span><span class="sxs-lookup"><span data-stu-id="b3f84-103">PST\_ACCESSCLAUSE structure</span></span>

<span data-ttu-id="b3f84-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="b3f84-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="b3f84-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="b3f84-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="b3f84-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="b3f84-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="b3f84-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="b3f84-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="b3f84-108">包含受保護儲存體之存取子句的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b3f84-108">Contains information about the access clause for the protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3f84-109">語法</span><span class="sxs-lookup"><span data-stu-id="b3f84-109">Syntax</span></span>


```C++
typedef struct {
  DWORD                cbSize;
  PST_ACCESSCLAUSETYPE ClauseType;
  DWORD                cbClauseData;
  BYTE                 *pbClauseData;
} PST_ACCESSCLAUSE, *PPST_ACCESSCLAUSE;
```



## <a name="members"></a><span data-ttu-id="b3f84-110">成員</span><span class="sxs-lookup"><span data-stu-id="b3f84-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="b3f84-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="b3f84-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="b3f84-112">此結構的大小。</span><span class="sxs-lookup"><span data-stu-id="b3f84-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="b3f84-113">**ClauseType**</span><span class="sxs-lookup"><span data-stu-id="b3f84-113">**ClauseType**</span></span>
</dt> <dd>

<span data-ttu-id="b3f84-114">**PbClauseData** 成員所指向的資料類型。</span><span class="sxs-lookup"><span data-stu-id="b3f84-114">The type of data that is pointed to by the **pbClauseData** member.</span></span> <span data-ttu-id="b3f84-115">如需詳細資訊，請參閱 [**PStore 類型**](pstore-types.md)。</span><span class="sxs-lookup"><span data-stu-id="b3f84-115">For more information, see [**PStore Types**](pstore-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3f84-116">**cbClauseData**</span><span class="sxs-lookup"><span data-stu-id="b3f84-116">**cbClauseData**</span></span>
</dt> <dd>

<span data-ttu-id="b3f84-117">**PbClauseData** 成員所指向之資料的大小。</span><span class="sxs-lookup"><span data-stu-id="b3f84-117">The size of the data that is pointed to by the **pbClauseData** member.</span></span>

</dd> <dt>

<span data-ttu-id="b3f84-118">**pbClauseData**</span><span class="sxs-lookup"><span data-stu-id="b3f84-118">**pbClauseData**</span></span>
</dt> <dd>

<span data-ttu-id="b3f84-119">存取子句資料的指標。</span><span class="sxs-lookup"><span data-stu-id="b3f84-119">A pointer to the access clause data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3f84-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3f84-120">Requirements</span></span>



| <span data-ttu-id="b3f84-121">需求</span><span class="sxs-lookup"><span data-stu-id="b3f84-121">Requirement</span></span> | <span data-ttu-id="b3f84-122">值</span><span class="sxs-lookup"><span data-stu-id="b3f84-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b3f84-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b3f84-123">Header</span></span><br/> | <dl> <span data-ttu-id="b3f84-124"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="b3f84-124"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3f84-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3f84-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3f84-126">**PST \_ ACCESSRULE**</span><span class="sxs-lookup"><span data-stu-id="b3f84-126">**PST\_ACCESSRULE**</span></span>](pst-accessrule.md)
</dt> </dl>

 

 
