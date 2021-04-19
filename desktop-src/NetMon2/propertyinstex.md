---
description: PROPERTYINSTEX 結構會定義一個自由格式的擴充屬性實例。
ms.assetid: a2316baf-07e2-4617-bb35-e20cfb11fbcb
title: 'PROPERTYINSTEX 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINSTEX
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f7b196d30e96f9d047f7f923d969d65a918aa4f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973442"
---
# <a name="propertyinstex-structure"></a><span data-ttu-id="9be5d-103">PROPERTYINSTEX 結構</span><span class="sxs-lookup"><span data-stu-id="9be5d-103">PROPERTYINSTEX structure</span></span>

<span data-ttu-id="9be5d-104">**PROPERTYINSTEX** 結構會定義一個自由格式的擴充屬性實例。</span><span class="sxs-lookup"><span data-stu-id="9be5d-104">The **PROPERTYINSTEX** structure defines a freeform, extended property instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="9be5d-105">語法</span><span class="sxs-lookup"><span data-stu-id="9be5d-105">Syntax</span></span>


```C++
typedef struct _PROPERTYINSTEX {
  WORD    Length;
  WORD    LengthEx;
  ULPVOID lpData;
  union {
    BYTE          Byte[];
    WORD          Word[];
    DWORD         Dword[];
    LARGE_INTEGER LargeInt[];
    SYSTEMTIME    SysTime[];
    TYPED_STRING  TypedString;
  };
} PROPERTYINSTEX;
```



## <a name="members"></a><span data-ttu-id="9be5d-106">成員</span><span class="sxs-lookup"><span data-stu-id="9be5d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9be5d-107">**長度**</span><span class="sxs-lookup"><span data-stu-id="9be5d-107">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="9be5d-108">資料的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9be5d-108">Length of the data in Bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9be5d-109">**LengthEx**</span><span class="sxs-lookup"><span data-stu-id="9be5d-109">**LengthEx**</span></span>
</dt> <dd>

<span data-ttu-id="9be5d-110">擴充資料的長度。</span><span class="sxs-lookup"><span data-stu-id="9be5d-110">Length of the extended data.</span></span>

</dd> <dt>

<span data-ttu-id="9be5d-111">**lpData**</span><span class="sxs-lookup"><span data-stu-id="9be5d-111">**lpData**</span></span>
</dt> <dd>

<span data-ttu-id="9be5d-112">擴充資料的指標。</span><span class="sxs-lookup"><span data-stu-id="9be5d-112">Pointer to the extended data.</span></span>

</dd> <dt>

<span data-ttu-id="9be5d-113">**位元組**</span><span class="sxs-lookup"><span data-stu-id="9be5d-113">**Byte**</span></span>
</dt> <dd>

<span data-ttu-id="9be5d-114">**位元組** 資料的指標。</span><span class="sxs-lookup"><span data-stu-id="9be5d-114">Pointer to the **BYTE** data.</span></span>

</dd> <dt>

<span data-ttu-id="9be5d-115">**Word**</span><span class="sxs-lookup"><span data-stu-id="9be5d-115">**Word**</span></span>
</dt> <dd>

<span data-ttu-id="9be5d-116">**文字** 資料的指標。</span><span class="sxs-lookup"><span data-stu-id="9be5d-116">Pointer to the **WORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="9be5d-117">**Dword**</span><span class="sxs-lookup"><span data-stu-id="9be5d-117">**Dword**</span></span>
</dt> <dd>

<span data-ttu-id="9be5d-118">**DWORD** 資料的指標。</span><span class="sxs-lookup"><span data-stu-id="9be5d-118">Pointer to the **DWORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="9be5d-119">**LargeInt**</span><span class="sxs-lookup"><span data-stu-id="9be5d-119">**LargeInt**</span></span>
</dt> <dd>

<span data-ttu-id="9be5d-120">**LARGEINT** 資料的指標。</span><span class="sxs-lookup"><span data-stu-id="9be5d-120">Pointer to the **LARGEINT** data.</span></span>

</dd> <dt>

<span data-ttu-id="9be5d-121">**SysTime**</span><span class="sxs-lookup"><span data-stu-id="9be5d-121">**SysTime**</span></span>
</dt> <dd>

<span data-ttu-id="9be5d-122">**SYSTEMTIME** 資料的指標。</span><span class="sxs-lookup"><span data-stu-id="9be5d-122">Pointer to the **SYSTEMTIME** data.</span></span>

</dd> <dt>

<span data-ttu-id="9be5d-123">**TypedString**</span><span class="sxs-lookup"><span data-stu-id="9be5d-123">**TypedString**</span></span>
</dt> <dd>

<span data-ttu-id="9be5d-124">可能有擴充資料的具類型字串。</span><span class="sxs-lookup"><span data-stu-id="9be5d-124">A typed string that may have extended data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9be5d-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="9be5d-125">Requirements</span></span>



| <span data-ttu-id="9be5d-126">需求</span><span class="sxs-lookup"><span data-stu-id="9be5d-126">Requirement</span></span> | <span data-ttu-id="9be5d-127">值</span><span class="sxs-lookup"><span data-stu-id="9be5d-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9be5d-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9be5d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9be5d-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9be5d-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9be5d-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9be5d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9be5d-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9be5d-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9be5d-132">標頭</span><span class="sxs-lookup"><span data-stu-id="9be5d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9be5d-133"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="9be5d-133"><dt>Netmon.h</dt></span></span> </dl> |



 

 




