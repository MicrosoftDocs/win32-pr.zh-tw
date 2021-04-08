---
description: FRAMETABLE 結構（框架指標的圓形緩衝區）會傳回到附加至 NPP 之 ITRC 介面的應用程式。
ms.assetid: 6e2d4f8d-46f2-4d53-bc28-7b0706663490
title: 'FRAMETABLE 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAMETABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 95d7930d7943b26ebba1bb194d083ca8beb9dcf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112236"
---
# <a name="frametable-structure"></a><span data-ttu-id="fe4ad-103">FRAMETABLE 結構</span><span class="sxs-lookup"><span data-stu-id="fe4ad-103">FRAMETABLE structure</span></span>

<span data-ttu-id="fe4ad-104">**FRAMETABLE** 結構（框架指標的圓形緩衝區）會傳回到附加至 NPP 之 **ITRC** 介面的應用程式。</span><span class="sxs-lookup"><span data-stu-id="fe4ad-104">The **FRAMETABLE** structure, a circular buffer of frame pointers, is handed back to applications attached to the **ITRC** interface of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe4ad-105">語法</span><span class="sxs-lookup"><span data-stu-id="fe4ad-105">Syntax</span></span>


```C++
typedef struct _FRAMETABLE {
  DWORD            FrameTableLength;
  DWORD            StartIndex;
  DWORD            EndIndex;
  DWORD            FrameCount;
  FRAME_DESCRIPTOR Frames[1];
} FRAMETABLE, *LPFRAMETABLE;
```



## <a name="members"></a><span data-ttu-id="fe4ad-106">成員</span><span class="sxs-lookup"><span data-stu-id="fe4ad-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fe4ad-107">**FrameTableLength**</span><span class="sxs-lookup"><span data-stu-id="fe4ad-107">**FrameTableLength**</span></span>
</dt> <dd>

<span data-ttu-id="fe4ad-108">資料表的總長度。</span><span class="sxs-lookup"><span data-stu-id="fe4ad-108">The total length of the table.</span></span>

</dd> <dt>

<span data-ttu-id="fe4ad-109">**StartIndex**</span><span class="sxs-lookup"><span data-stu-id="fe4ad-109">**StartIndex**</span></span>
</dt> <dd>

<span data-ttu-id="fe4ad-110">資料表中的第一個索引。</span><span class="sxs-lookup"><span data-stu-id="fe4ad-110">The first index within the table.</span></span>

</dd> <dt>

<span data-ttu-id="fe4ad-111">**EndIndex**</span><span class="sxs-lookup"><span data-stu-id="fe4ad-111">**EndIndex**</span></span>
</dt> <dd>

<span data-ttu-id="fe4ad-112">資料表內的最後一個索引。</span><span class="sxs-lookup"><span data-stu-id="fe4ad-112">The last index within the table.</span></span>

</dd> <dt>

<span data-ttu-id="fe4ad-113">**FrameCount**</span><span class="sxs-lookup"><span data-stu-id="fe4ad-113">**FrameCount**</span></span>
</dt> <dd>

<span data-ttu-id="fe4ad-114">此資料表所描述的框架數目。</span><span class="sxs-lookup"><span data-stu-id="fe4ad-114">The number of frames described by this table.</span></span>

</dd> <dt>

<span data-ttu-id="fe4ad-115">**框架**</span><span class="sxs-lookup"><span data-stu-id="fe4ad-115">**Frames**</span></span>
</dt> <dd>

<span data-ttu-id="fe4ad-116">實際的框架描述項陣列。</span><span class="sxs-lookup"><span data-stu-id="fe4ad-116">The actual array of frame descriptors.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe4ad-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe4ad-117">Requirements</span></span>



| <span data-ttu-id="fe4ad-118">需求</span><span class="sxs-lookup"><span data-stu-id="fe4ad-118">Requirement</span></span> | <span data-ttu-id="fe4ad-119">值</span><span class="sxs-lookup"><span data-stu-id="fe4ad-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fe4ad-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe4ad-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fe4ad-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe4ad-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="fe4ad-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe4ad-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fe4ad-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe4ad-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fe4ad-124">標頭</span><span class="sxs-lookup"><span data-stu-id="fe4ad-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe4ad-125"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="fe4ad-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




