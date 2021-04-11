---
description: 包含檔案的屬性資料。
ms.assetid: f23f801c-826c-4269-bf96-0e01430484f4
title: ATTRINFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 01c061330db3e97989e0700452fd4a205488a9fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847012"
---
# <a name="attrinfo-structure"></a><span data-ttu-id="6c3c9-103">ATTRINFO 結構</span><span class="sxs-lookup"><span data-stu-id="6c3c9-103">ATTRINFO structure</span></span>

<span data-ttu-id="6c3c9-104">包含檔案的屬性資料。</span><span class="sxs-lookup"><span data-stu-id="6c3c9-104">Contains the attribute data for a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c3c9-105">語法</span><span class="sxs-lookup"><span data-stu-id="6c3c9-105">Syntax</span></span>


```C++
typedef struct tagATTRINFO {
  TAG   tAttrID;
  DWORD dwFlags;
  union {
    ULONGLONG ullAttr;
    DWORD     dwAttr;
    TCHAR     *lpAttr;
  };
} ATTRINFO, *PATTRINFO;
```



## <a name="members"></a><span data-ttu-id="6c3c9-106">成員</span><span class="sxs-lookup"><span data-stu-id="6c3c9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6c3c9-107">**tAttrID**</span><span class="sxs-lookup"><span data-stu-id="6c3c9-107">**tAttrID**</span></span>
</dt> <dd>

<span data-ttu-id="6c3c9-108">屬性類型。</span><span class="sxs-lookup"><span data-stu-id="6c3c9-108">The attribute type.</span></span> <span data-ttu-id="6c3c9-109">請參閱 [標記類型](tag-types.md)。</span><span class="sxs-lookup"><span data-stu-id="6c3c9-109">See [TAG Types](tag-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c3c9-110">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="6c3c9-110">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="6c3c9-111">這個屬性的旗標。</span><span class="sxs-lookup"><span data-stu-id="6c3c9-111">The flags for this attribute.</span></span>



| <span data-ttu-id="6c3c9-112">值</span><span class="sxs-lookup"><span data-stu-id="6c3c9-112">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="6c3c9-113">意義</span><span class="sxs-lookup"><span data-stu-id="6c3c9-113">Meaning</span></span>                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="ATTRIBUTE_AVAILABLE"></span><span id="attribute_available"></span><dl> <span data-ttu-id="6c3c9-114"><dt>**屬性 \_可用**</dt>的 <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="6c3c9-114"><dt>**ATTRIBUTE\_AVAILABLE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="6c3c9-115">屬性可供使用。</span><span class="sxs-lookup"><span data-stu-id="6c3c9-115">The attribute is available.</span></span><br/>                             |
| <span id="ATTRIBUTE_FAILED"></span><span id="attribute_failed"></span><dl> <span data-ttu-id="6c3c9-116"><dt>**屬性 \_失敗**</dt>的 <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="6c3c9-116"><dt>**ATTRIBUTE\_FAILED**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="6c3c9-117">因為無法使用屬性，所以呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="6c3c9-117">The call failed because the attribute is not available.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6c3c9-118">**ullAttr**</span><span class="sxs-lookup"><span data-stu-id="6c3c9-118">**ullAttr**</span></span>
</dt> <dd>

<span data-ttu-id="6c3c9-119">如果標記類型為 **\_ \_ qword) 標記** 類型，則為 **qword** 值 (。</span><span class="sxs-lookup"><span data-stu-id="6c3c9-119">A **QWORD** value (if the tag type is **TAG\_TYPE\_QWORD**).</span></span>

</dd> <dt>

<span data-ttu-id="6c3c9-120">**dwAttr**</span><span class="sxs-lookup"><span data-stu-id="6c3c9-120">**dwAttr**</span></span>
</dt> <dd>

<span data-ttu-id="6c3c9-121">**Dword** 值 (如果標記類型為 **標記 \_ 類型 \_ DWORD**) 。</span><span class="sxs-lookup"><span data-stu-id="6c3c9-121">A **DWORD** value (if the tag type is **TAG\_TYPE\_DWORD**).</span></span>

</dd> <dt>

<span data-ttu-id="6c3c9-122">**lpAttr**</span><span class="sxs-lookup"><span data-stu-id="6c3c9-122">**lpAttr**</span></span>
</dt> <dd>

<span data-ttu-id="6c3c9-123">如果標記類型為 **標記 \_ 類型 \_ STRINGREF**) ，則為字串 (的指標。</span><span class="sxs-lookup"><span data-stu-id="6c3c9-123">A pointer to a string (if the tag type is **TAG\_TYPE\_STRINGREF**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c3c9-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c3c9-124">Requirements</span></span>



| <span data-ttu-id="6c3c9-125">需求</span><span class="sxs-lookup"><span data-stu-id="6c3c9-125">Requirement</span></span> | <span data-ttu-id="6c3c9-126">值</span><span class="sxs-lookup"><span data-stu-id="6c3c9-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6c3c9-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c3c9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6c3c9-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c3c9-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6c3c9-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c3c9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6c3c9-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c3c9-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c3c9-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c3c9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c3c9-132">**SdbFormatAttribute**</span><span class="sxs-lookup"><span data-stu-id="6c3c9-132">**SdbFormatAttribute**</span></span>](sdbformatattribute.md)
</dt> <dt>

[<span data-ttu-id="6c3c9-133">**SdbFreeFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="6c3c9-133">**SdbFreeFileAttributes**</span></span>](sdbfreefileattributes.md)
</dt> <dt>

[<span data-ttu-id="6c3c9-134">**SdbGetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="6c3c9-134">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
</dt> </dl>

 

 




