---
description: 範圍結構會定義有效屬性值的範圍。
ms.assetid: 7bd14410-f5c1-487b-8776-405567991e5a
title: '範圍結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RANGE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: bf465636f315e60e43350bb370e2002b8a96e635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989359"
---
# <a name="range-structure"></a><span data-ttu-id="00e6c-103">範圍結構</span><span class="sxs-lookup"><span data-stu-id="00e6c-103">RANGE structure</span></span>

<span data-ttu-id="00e6c-104">**範圍** 結構會定義有效屬性值的範圍。</span><span class="sxs-lookup"><span data-stu-id="00e6c-104">The **RANGE** structure defines a range of valid property values.</span></span>

## <a name="syntax"></a><span data-ttu-id="00e6c-105">語法</span><span class="sxs-lookup"><span data-stu-id="00e6c-105">Syntax</span></span>


```C++
typedef struct range {
  DWORD MinValue;
  DWORD MaxValue;
} RANGE, *LPRANGE;
```



## <a name="members"></a><span data-ttu-id="00e6c-106">成員</span><span class="sxs-lookup"><span data-stu-id="00e6c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="00e6c-107">**MinValue**</span><span class="sxs-lookup"><span data-stu-id="00e6c-107">**MinValue**</span></span>
</dt> <dd>

<span data-ttu-id="00e6c-108">範圍中可能的最小值。</span><span class="sxs-lookup"><span data-stu-id="00e6c-108">Lowest possible value in a range.</span></span>

</dd> <dt>

<span data-ttu-id="00e6c-109">**Timespan.maxvalue**</span><span class="sxs-lookup"><span data-stu-id="00e6c-109">**MaxValue**</span></span>
</dt> <dd>

<span data-ttu-id="00e6c-110">範圍中最高的可能值。</span><span class="sxs-lookup"><span data-stu-id="00e6c-110">Highest possible value in a range.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00e6c-111">備註</span><span class="sxs-lookup"><span data-stu-id="00e6c-111">Remarks</span></span>

<span data-ttu-id="00e6c-112">**範圍** 結構是用來為通訊協定屬性指定有效的數位範圍。</span><span class="sxs-lookup"><span data-stu-id="00e6c-112">The **RANGE** structure is used to specify a valid range of numbers for a protocol property.</span></span> <span data-ttu-id="00e6c-113">如果 **PROPERTYINFO** 結構的 **DataQualifier** 成員設定為 [ **\_ QUAL \_ 範圍**]，則 [PROPERTYINFO](propertyinfo.md)結構的 **lpRange** 成員必須提供 **範圍** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="00e6c-113">If the **DataQualifier** member of the **PROPERTYINFO** structure is set to **PROP\_QUAL\_RANGE**, the **lpRange** member of the [PROPERTYINFO](propertyinfo.md) structure must provide a pointer to a **RANGE** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="00e6c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="00e6c-114">Requirements</span></span>



| <span data-ttu-id="00e6c-115">需求</span><span class="sxs-lookup"><span data-stu-id="00e6c-115">Requirement</span></span> | <span data-ttu-id="00e6c-116">值</span><span class="sxs-lookup"><span data-stu-id="00e6c-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="00e6c-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00e6c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="00e6c-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00e6c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="00e6c-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00e6c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="00e6c-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00e6c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="00e6c-121">標頭</span><span class="sxs-lookup"><span data-stu-id="00e6c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="00e6c-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="00e6c-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00e6c-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00e6c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00e6c-124">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="00e6c-124">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> </dl>

 

 




