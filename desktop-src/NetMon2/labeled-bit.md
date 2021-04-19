---
description: 加上標籤的 \_ 位結構會定義標籤位配對。
ms.assetid: 500b5159-bf9f-49d4-8567-d8e462015eb0
title: 'LABELED_BIT 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BIT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 24a56e832600b551dd3ab43ea93d59c5805af630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974948"
---
# <a name="labeled_bit-structure"></a><span data-ttu-id="120df-103">標記的 \_ 位結構</span><span class="sxs-lookup"><span data-stu-id="120df-103">LABELED\_BIT structure</span></span>

<span data-ttu-id="120df-104">加上卷 **標的 \_ 位** 結構會定義標籤位配對。</span><span class="sxs-lookup"><span data-stu-id="120df-104">The **LABELED\_BIT** structure defines a label BIT pair.</span></span>

## <a name="syntax"></a><span data-ttu-id="120df-105">語法</span><span class="sxs-lookup"><span data-stu-id="120df-105">Syntax</span></span>


```C++
typedef struct _LABELED_BIT {
  BYTE  BitNumber;
  LPSTR LabelOff;
  LPSTR LabelOn;
} LABELED_BIT, *LPLABELED_BIT;
```



## <a name="members"></a><span data-ttu-id="120df-106">成員</span><span class="sxs-lookup"><span data-stu-id="120df-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="120df-107">**BitNumber**</span><span class="sxs-lookup"><span data-stu-id="120df-107">**BitNumber**</span></span>
</dt> <dd>

<span data-ttu-id="120df-108">標籤位配對的位。</span><span class="sxs-lookup"><span data-stu-id="120df-108">BIT number of the label BIT pair.</span></span> <span data-ttu-id="120df-109">值的範圍是從0到255。</span><span class="sxs-lookup"><span data-stu-id="120df-109">Values range from 0 to 255.</span></span> <span data-ttu-id="120df-110">將 **Bitnumber** 成員設定為用於比較屬性值的位。</span><span class="sxs-lookup"><span data-stu-id="120df-110">Set the **Bitnumber** member to the BIT used in the comparison of the property value.</span></span>

</dd> <dt>

<span data-ttu-id="120df-111">**LabelOff**</span><span class="sxs-lookup"><span data-stu-id="120df-111">**LabelOff**</span></span>
</dt> <dd>

<span data-ttu-id="120df-112">當 **BitNumber** 中指定的位等於零時，所顯示的字串或標籤。</span><span class="sxs-lookup"><span data-stu-id="120df-112">String or label that is displayed when the BIT specified in **BitNumber** equals zero.</span></span> <span data-ttu-id="120df-113">例如，可能的標籤為 "Bit OFF"。</span><span class="sxs-lookup"><span data-stu-id="120df-113">For example, a possible label is "Bit OFF".</span></span>

</dd> <dt>

<span data-ttu-id="120df-114">**LabelOn**</span><span class="sxs-lookup"><span data-stu-id="120df-114">**LabelOn**</span></span>
</dt> <dd>

<span data-ttu-id="120df-115">在 **BitNumber** 中指定的位等於1時所顯示的字串或標籤。</span><span class="sxs-lookup"><span data-stu-id="120df-115">String or label that is displayed when the BIT specified in **BitNumber** equals 1.</span></span> <span data-ttu-id="120df-116">例如，可能的標籤是「位在」。</span><span class="sxs-lookup"><span data-stu-id="120df-116">For example, a possible label is "Bit ON".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="120df-117">備註</span><span class="sxs-lookup"><span data-stu-id="120df-117">Remarks</span></span>

<span data-ttu-id="120df-118">加上卷 **標 \_ 位** 結構的陣列，用來定義一組標籤位配對。</span><span class="sxs-lookup"><span data-stu-id="120df-118">An array of **LABELED\_BIT** structures is used to define a set of label BIT pairs.</span></span> <span data-ttu-id="120df-119">陣列的指標是在 [SET](set.md)結構的 **lpLabeledBit** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="120df-119">A pointer to the array is specified in the **lpLabeledBit** member of the [SET](set.md) structure.</span></span> <span data-ttu-id="120df-120">當您想要根據每個位的設定來顯示標籤時，會使用配對。</span><span class="sxs-lookup"><span data-stu-id="120df-120">The pairs are used when you want to display a label based on the setting of each BIT.</span></span> <span data-ttu-id="120df-121">一般而言，這種類型的集合會用來指出位的 ON 或 OF光圈值。</span><span class="sxs-lookup"><span data-stu-id="120df-121">Typically, this type of set is used to indicate the ON or OFF value of BITs.</span></span>

<span data-ttu-id="120df-122">當指定位集時，網路監視器只會顯示 **集合** 結構陣列中包含的位。</span><span class="sxs-lookup"><span data-stu-id="120df-122">When a BIT set is specified, Network Monitor displays only the BITs included in the array of **SET** structures.</span></span> <span data-ttu-id="120df-123">不在 **集合** 結構中的位則不會顯示。</span><span class="sxs-lookup"><span data-stu-id="120df-123">BITs that are not in the **SET** structure are not displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="120df-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="120df-124">Requirements</span></span>



| <span data-ttu-id="120df-125">需求</span><span class="sxs-lookup"><span data-stu-id="120df-125">Requirement</span></span> | <span data-ttu-id="120df-126">值</span><span class="sxs-lookup"><span data-stu-id="120df-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="120df-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="120df-127">Minimum supported client</span></span><br/> | <span data-ttu-id="120df-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="120df-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="120df-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="120df-129">Minimum supported server</span></span><br/> | <span data-ttu-id="120df-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="120df-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="120df-131">標頭</span><span class="sxs-lookup"><span data-stu-id="120df-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="120df-132"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="120df-132"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="120df-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="120df-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="120df-134">SET</span><span class="sxs-lookup"><span data-stu-id="120df-134">SET</span></span>](set.md)
</dt> </dl>

 

 




