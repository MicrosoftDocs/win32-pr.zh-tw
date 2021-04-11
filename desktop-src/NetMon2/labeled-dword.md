---
description: 加上標籤的 \_ dword 結構會定義在偵測到特定的 dword 屬性值時所顯示的標籤。
ms.assetid: 1aed3226-6d69-41b0-860b-4ffb5b905f1a
title: 'LABELED_DWORD 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_DWORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0bec068622683172116bf8c4f6e88450d5752920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193915"
---
# <a name="labeled_dword-structure"></a><span data-ttu-id="2ba47-103">標記的 \_ DWORD 結構</span><span class="sxs-lookup"><span data-stu-id="2ba47-103">LABELED\_DWORD structure</span></span>

<span data-ttu-id="2ba47-104">加上 **標籤的 \_ dword** 結構會定義在偵測到特定的 dword 屬性值時所顯示的標籤。</span><span class="sxs-lookup"><span data-stu-id="2ba47-104">The **LABELED\_DWORD** structure defines a label that is displayed when a specific DWORD property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ba47-105">語法</span><span class="sxs-lookup"><span data-stu-id="2ba47-105">Syntax</span></span>


```C++
typedef struct _LABELED_DWORD {
  DWORD Value;
  LPSTR Label;
} LABELED_DWORD, *LPLABELED_DWORD;
```



## <a name="members"></a><span data-ttu-id="2ba47-106">成員</span><span class="sxs-lookup"><span data-stu-id="2ba47-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2ba47-107">**值**</span><span class="sxs-lookup"><span data-stu-id="2ba47-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="2ba47-108">您要偵測之屬性的 DWORD 值。</span><span class="sxs-lookup"><span data-stu-id="2ba47-108">DWORD value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="2ba47-109">**標籤**</span><span class="sxs-lookup"><span data-stu-id="2ba47-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="2ba47-110">偵測到在 **值** 成員中指定的 DWORD 值時所顯示的文字描述或標籤。</span><span class="sxs-lookup"><span data-stu-id="2ba47-110">Textual description or label that is displayed when the DWORD value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ba47-111">備註</span><span class="sxs-lookup"><span data-stu-id="2ba47-111">Remarks</span></span>

<span data-ttu-id="2ba47-112">[Set](set.md)結構的 **lpLabeledDwordTable** 成員會指向定義一個或多個 DWORD 值組之 **Label** 成員的 **集合** 結構陣列。</span><span class="sxs-lookup"><span data-stu-id="2ba47-112">The **lpLabeledDwordTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more **Label** members of the DWORD value pairs.</span></span> <span data-ttu-id="2ba47-113">當您想要顯示標籤來取代在通訊協定封包中找到的特定 DWORD 值時，會使用配對。</span><span class="sxs-lookup"><span data-stu-id="2ba47-113">The pairs are used when you want to display a label in place of a specific DWORD value that is found in the protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ba47-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ba47-114">Requirements</span></span>



| <span data-ttu-id="2ba47-115">需求</span><span class="sxs-lookup"><span data-stu-id="2ba47-115">Requirement</span></span> | <span data-ttu-id="2ba47-116">值</span><span class="sxs-lookup"><span data-stu-id="2ba47-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2ba47-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ba47-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2ba47-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ba47-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2ba47-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ba47-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2ba47-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ba47-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2ba47-121">標頭</span><span class="sxs-lookup"><span data-stu-id="2ba47-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ba47-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="2ba47-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ba47-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ba47-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ba47-124">SET</span><span class="sxs-lookup"><span data-stu-id="2ba47-124">SET</span></span>](set.md)
</dt> </dl>

 

 




