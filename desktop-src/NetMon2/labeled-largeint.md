---
description: 加上標籤的 \_ LARGEINT 結構會定義在偵測到特定的 LARGEINT 屬性值時所顯示的標籤。
ms.assetid: ca565be0-96bb-4265-9422-793db0723563
title: 'LABELED_LARGEINT 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_LARGEINT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4de92c3e67567ef86bb3d46905e595bd9d54c194
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026813"
---
# <a name="labeled_largeint-structure"></a><span data-ttu-id="293e6-103">標記的 \_ LARGEINT 結構</span><span class="sxs-lookup"><span data-stu-id="293e6-103">LABELED\_LARGEINT structure</span></span>

<span data-ttu-id="293e6-104">加上 **標籤的 \_ LARGEINT** 結構會定義在偵測到特定的 LARGEINT 屬性值時所顯示的標籤。</span><span class="sxs-lookup"><span data-stu-id="293e6-104">The **LABELED\_LARGEINT** structure defines a label that is displayed when a specific LARGEINT property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="293e6-105">語法</span><span class="sxs-lookup"><span data-stu-id="293e6-105">Syntax</span></span>


```C++
typedef struct _LABELED_LARGEINT {
  LARGE_INTEGER Value;
  LPSTR         Label;
} LABELED_LARGEINT, *LPLABELED_LARGEINT;
```



## <a name="members"></a><span data-ttu-id="293e6-106">成員</span><span class="sxs-lookup"><span data-stu-id="293e6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="293e6-107">**值**</span><span class="sxs-lookup"><span data-stu-id="293e6-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="293e6-108">您要偵測之屬性的 LARGEINT 值。</span><span class="sxs-lookup"><span data-stu-id="293e6-108">LARGEINT value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="293e6-109">**標籤**</span><span class="sxs-lookup"><span data-stu-id="293e6-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="293e6-110">偵測到在 **值** 成員中指定的 LARGEINT 值時，所顯示的文字描述或標籤。</span><span class="sxs-lookup"><span data-stu-id="293e6-110">Textual description or label that is displayed when the LARGEINT value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="293e6-111">備註</span><span class="sxs-lookup"><span data-stu-id="293e6-111">Remarks</span></span>

<span data-ttu-id="293e6-112">[集合](set.md)結構的 **lpLabeledLargeIntTable** 成員會指向定義一或多個 LARGEINT 值配對之 **標籤** 成員的 **集合** 結構陣列。</span><span class="sxs-lookup"><span data-stu-id="293e6-112">The **lpLabeledLargeIntTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more **Label** members of the LARGEINT value pairs.</span></span> <span data-ttu-id="293e6-113">當您想要顯示標籤來取代在通訊協定封包中找到的特定 LARGEINT 值時，會使用配對。</span><span class="sxs-lookup"><span data-stu-id="293e6-113">The pairs are used when you want to display a label in place of a specific LARGEINT value that is found in a protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="293e6-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="293e6-114">Requirements</span></span>



| <span data-ttu-id="293e6-115">需求</span><span class="sxs-lookup"><span data-stu-id="293e6-115">Requirement</span></span> | <span data-ttu-id="293e6-116">值</span><span class="sxs-lookup"><span data-stu-id="293e6-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="293e6-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="293e6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="293e6-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="293e6-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="293e6-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="293e6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="293e6-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="293e6-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="293e6-121">標頭</span><span class="sxs-lookup"><span data-stu-id="293e6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="293e6-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="293e6-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="293e6-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="293e6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="293e6-124">SET</span><span class="sxs-lookup"><span data-stu-id="293e6-124">SET</span></span>](set.md)
</dt> </dl>

 

 




