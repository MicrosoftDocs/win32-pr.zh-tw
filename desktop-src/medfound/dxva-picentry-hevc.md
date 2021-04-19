---
description: 指定未壓縮表面的參考。
ms.assetid: 01F9C9F9-8EB4-49D5-91F0-89B4C40DDDC8
title: 'DXVA_PicEntry_HEVC 結構 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_PicEntry_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: a2c4856452d0f8010e8f97126b4e660557ea40ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966654"
---
# <a name="dxva_picentry_hevc-structure"></a><span data-ttu-id="ff0b5-103">DXVA \_ PicEntry \_ HEVC 結構</span><span class="sxs-lookup"><span data-stu-id="ff0b5-103">DXVA\_PicEntry\_HEVC structure</span></span>

<span data-ttu-id="ff0b5-104">指定未壓縮表面的參考。</span><span class="sxs-lookup"><span data-stu-id="ff0b5-104">Specifies a reference to an uncompressed surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff0b5-105">語法</span><span class="sxs-lookup"><span data-stu-id="ff0b5-105">Syntax</span></span>


```C++
typedef struct _DXVA_PicEntry_HEVC {
  union {
    struct {
      UCHAR  Index7Bits  :7;
      UCHAR  AssociatedFlag   :1;
    };
    UCHAR  bPicEntry;
  };
} DXVA_PicEntry_HEVC, *PDXVA_PicEntry_HEVC;
```



## <a name="members"></a><span data-ttu-id="ff0b5-106">成員</span><span class="sxs-lookup"><span data-stu-id="ff0b5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ff0b5-107">**Index7Bits**</span><span class="sxs-lookup"><span data-stu-id="ff0b5-107">**Index7Bits**</span></span>
</dt> <dd>

<span data-ttu-id="ff0b5-108">識別未壓縮表面的索引。</span><span class="sxs-lookup"><span data-stu-id="ff0b5-108">An index that identifies an uncompressed surface .</span></span>

</dd> <dt>

<span data-ttu-id="ff0b5-109">**AssociatedFlag**</span><span class="sxs-lookup"><span data-stu-id="ff0b5-109">**AssociatedFlag**</span></span> 
</dt> <dd>

<span data-ttu-id="ff0b5-110">與介面相關聯的選擇性1位旗標。</span><span class="sxs-lookup"><span data-stu-id="ff0b5-110">Optional 1-bit flag associated with the surface.</span></span> <span data-ttu-id="ff0b5-111">旗標的意義取決於內容。</span><span class="sxs-lookup"><span data-stu-id="ff0b5-111">The meaning of the flag depends on the context.</span></span> <span data-ttu-id="ff0b5-112">例如，它可以指定參考框架是否為長期參考或短期參考。</span><span class="sxs-lookup"><span data-stu-id="ff0b5-112">For example, it can specify whether the reference frame is a long-term reference or a short-term reference.</span></span>

</dd> <dt>

<span data-ttu-id="ff0b5-113">**bPicEntry**</span><span class="sxs-lookup"><span data-stu-id="ff0b5-113">**bPicEntry**</span></span>
</dt> <dd>

<span data-ttu-id="ff0b5-114">存取聯集的整個8位。</span><span class="sxs-lookup"><span data-stu-id="ff0b5-114">Accesses the entire 8 bits of the union.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff0b5-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff0b5-115">Requirements</span></span>



| <span data-ttu-id="ff0b5-116">需求</span><span class="sxs-lookup"><span data-stu-id="ff0b5-116">Requirement</span></span> | <span data-ttu-id="ff0b5-117">值</span><span class="sxs-lookup"><span data-stu-id="ff0b5-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ff0b5-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff0b5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ff0b5-119">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff0b5-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ff0b5-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff0b5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ff0b5-121">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff0b5-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ff0b5-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ff0b5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff0b5-123"><dt>Dxva。h</dt></span><span class="sxs-lookup"><span data-stu-id="ff0b5-123"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff0b5-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff0b5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff0b5-125">媒體基礎結構</span><span class="sxs-lookup"><span data-stu-id="ff0b5-125">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




