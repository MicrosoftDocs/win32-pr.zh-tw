---
description: KSMULTIPLE \_ 專案結構描述核心模式 pin 上可變長度屬性的大小和計數。
ms.assetid: aedbf7bc-393d-4ab5-afcd-d8822b925f07
title: 'KSMULTIPLE_ITEM 結構 (Ks) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSMULTIPLE_ITEM
api_type:
- HeaderDef
api_location:
- ks.h
ms.openlocfilehash: 62e26b1aa8804514588e66c1d02e1f0643e97bcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998633"
---
# <a name="ksmultiple_item-structure"></a><span data-ttu-id="ef863-103">KSMULTIPLE \_ 專案結構</span><span class="sxs-lookup"><span data-stu-id="ef863-103">KSMULTIPLE\_ITEM structure</span></span>

<span data-ttu-id="ef863-104">`KSMULTIPLE_ITEM`結構描述核心模式 pin 上可變長度屬性的大小和計數。</span><span class="sxs-lookup"><span data-stu-id="ef863-104">The `KSMULTIPLE_ITEM` structure describes the size and count of variable-length properties on kernel-mode pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef863-105">語法</span><span class="sxs-lookup"><span data-stu-id="ef863-105">Syntax</span></span>


```C++
typedef struct {
  ULONG Size;
  ULONG Count;
} KSMULTIPLE_ITEM, *PKSMULTIPLE_ITEM;
```



## <a name="members"></a><span data-ttu-id="ef863-106">成員</span><span class="sxs-lookup"><span data-stu-id="ef863-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ef863-107">**大小**</span><span class="sxs-lookup"><span data-stu-id="ef863-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="ef863-108">傳回之記憶體區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ef863-108">Size of the returned memory block, in bytes.</span></span> <span data-ttu-id="ef863-109">大小包含 **KSMULTIPLE \_ 專案** 結構和其後的專案。</span><span class="sxs-lookup"><span data-stu-id="ef863-109">The size includes the **KSMULTIPLE\_ITEM** structure and the items that follow it.</span></span>

</dd> <dt>

<span data-ttu-id="ef863-110">**Count**</span><span class="sxs-lookup"><span data-stu-id="ef863-110">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="ef863-111">指定遵循此結構的總專案數。</span><span class="sxs-lookup"><span data-stu-id="ef863-111">Specifies the total number of items that follow this structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef863-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef863-112">Requirements</span></span>



| <span data-ttu-id="ef863-113">需求</span><span class="sxs-lookup"><span data-stu-id="ef863-113">Requirement</span></span> | <span data-ttu-id="ef863-114">值</span><span class="sxs-lookup"><span data-stu-id="ef863-114">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="ef863-115">標頭</span><span class="sxs-lookup"><span data-stu-id="ef863-115">Header</span></span><br/> | <dl> <span data-ttu-id="ef863-116"><dt>Ks. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef863-116"><dt>Ks.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef863-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef863-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef863-118">DirectShow 結構</span><span class="sxs-lookup"><span data-stu-id="ef863-118">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="ef863-119">**IKsPin::KsQueryMediums**</span><span class="sxs-lookup"><span data-stu-id="ef863-119">**IKsPin::KsQueryMediums**</span></span>](ikspin-ksquerymediums.md)
</dt> <dt>

[<span data-ttu-id="ef863-120">**REGPINMEDIUM**</span><span class="sxs-lookup"><span data-stu-id="ef863-120">**REGPINMEDIUM**</span></span>](/windows/desktop/api/strmif/ns-strmif-regpinmedium)
</dt> </dl>

 

 




