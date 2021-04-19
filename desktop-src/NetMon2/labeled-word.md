---
description: 加上標籤的 \_ 單字結構會定義在偵測到特定單字屬性值時所顯示的標籤。
ms.assetid: bfb1d34e-4a07-493f-8e43-508b77cce581
title: 'LABELED_WORD 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_WORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 445b24245d2e9d15c1c2b6d69de20c464cbf1724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985003"
---
# <a name="labeled_word-structure"></a><span data-ttu-id="6b23e-103">標記的 \_ WORD 結構</span><span class="sxs-lookup"><span data-stu-id="6b23e-103">LABELED\_WORD structure</span></span>

<span data-ttu-id="6b23e-104">加上 **標籤的 \_ 單字** 結構會定義在偵測到特定單字屬性值時所顯示的標籤。</span><span class="sxs-lookup"><span data-stu-id="6b23e-104">The **LABELED\_WORD** structure defines a label that is displayed when a specific WORD property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b23e-105">語法</span><span class="sxs-lookup"><span data-stu-id="6b23e-105">Syntax</span></span>


```C++
typedef struct _LABELED_WORD {
  WORD  Value;
  LPSTR Label;
} LABELED_WORD, *LPLABELED_WORD;
```



## <a name="members"></a><span data-ttu-id="6b23e-106">成員</span><span class="sxs-lookup"><span data-stu-id="6b23e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6b23e-107">**值**</span><span class="sxs-lookup"><span data-stu-id="6b23e-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="6b23e-108">您要偵測之屬性的文字值。</span><span class="sxs-lookup"><span data-stu-id="6b23e-108">WORD value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="6b23e-109">**標籤**</span><span class="sxs-lookup"><span data-stu-id="6b23e-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="6b23e-110">偵測到 **值** 成員中指定的文字值時，所顯示的文字描述或標籤。</span><span class="sxs-lookup"><span data-stu-id="6b23e-110">Textual description or label that is displayed when the WORD value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b23e-111">備註</span><span class="sxs-lookup"><span data-stu-id="6b23e-111">Remarks</span></span>

<span data-ttu-id="6b23e-112">[Set](set.md)結構的 **lpLabeledWordTable** 成員會指向設定結構的陣列，以定義一或多個標籤值組。</span><span class="sxs-lookup"><span data-stu-id="6b23e-112">The **lpLabeledWordTable** member of the [SET](set.md) structure points to an array of SET structures to define one or more label value pairs.</span></span> <span data-ttu-id="6b23e-113">當您想要顯示標籤來取代在通訊協定封包中找到的特定字組值時，會使用這些配對。</span><span class="sxs-lookup"><span data-stu-id="6b23e-113">These pairs are used when you want to display a label in place of a specific WORD value that is found in a protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b23e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b23e-114">Requirements</span></span>



| <span data-ttu-id="6b23e-115">需求</span><span class="sxs-lookup"><span data-stu-id="6b23e-115">Requirement</span></span> | <span data-ttu-id="6b23e-116">值</span><span class="sxs-lookup"><span data-stu-id="6b23e-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6b23e-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6b23e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6b23e-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b23e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6b23e-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6b23e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6b23e-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b23e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6b23e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="6b23e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b23e-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="6b23e-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b23e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b23e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b23e-124">SET</span><span class="sxs-lookup"><span data-stu-id="6b23e-124">SET</span></span>](set.md)
</dt> </dl>

 

 




