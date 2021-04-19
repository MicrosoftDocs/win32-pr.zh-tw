---
description: 加上標籤的 \_ 位元組結構會定義加上標籤的位配對。 當偵測到特定的位元組屬性值時，就會顯示標記位組的標籤。
ms.assetid: 6dc6a773-da75-4ffe-878f-b30ceef2acb1
title: 'LABELED_BYTE 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BYTE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4768e605892b9bfe2a3df67fbdea862f67dc1a16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997849"
---
# <a name="labeled_byte-structure"></a><span data-ttu-id="57ab0-104">標記的 \_ 位元組結構</span><span class="sxs-lookup"><span data-stu-id="57ab0-104">LABELED\_BYTE structure</span></span>

<span data-ttu-id="57ab0-105">加上 **標籤的 \_ 位元組** 結構會定義加上標籤的位配對。</span><span class="sxs-lookup"><span data-stu-id="57ab0-105">The **LABELED\_BYTE** structure defines a labeled BIT pair.</span></span> <span data-ttu-id="57ab0-106">當偵測到特定的位元組屬性值時，就會顯示標記位組的 **標籤** 。</span><span class="sxs-lookup"><span data-stu-id="57ab0-106">The **Label** of the labeled BIT pair is displayed when a specific byte property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="57ab0-107">語法</span><span class="sxs-lookup"><span data-stu-id="57ab0-107">Syntax</span></span>


```C++
typedef struct _LABELED_BYTE {
  BYTE  Value;
  LPSTR Label;
} LABELED_BYTE, *LPLABELED_BYTE;
```



## <a name="members"></a><span data-ttu-id="57ab0-108">成員</span><span class="sxs-lookup"><span data-stu-id="57ab0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="57ab0-109">**值**</span><span class="sxs-lookup"><span data-stu-id="57ab0-109">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="57ab0-110">您要偵測之屬性的位元組值。</span><span class="sxs-lookup"><span data-stu-id="57ab0-110">BYTE value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="57ab0-111">**標籤**</span><span class="sxs-lookup"><span data-stu-id="57ab0-111">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="57ab0-112">偵測到 **值** 成員中指定的值時，所顯示的文字描述或標籤。</span><span class="sxs-lookup"><span data-stu-id="57ab0-112">Textual description or label that is displayed when the value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57ab0-113">備註</span><span class="sxs-lookup"><span data-stu-id="57ab0-113">Remarks</span></span>

<span data-ttu-id="57ab0-114">[Set](set.md)結構的 **lpLabeledByteTable** 成員會指向定義一個或多個位元組值組之 **標籤** 成員的 **集合** 結構陣列。</span><span class="sxs-lookup"><span data-stu-id="57ab0-114">The **lpLabeledByteTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more **Label** members of the BYTE value pairs.</span></span> <span data-ttu-id="57ab0-115">當您想要顯示標籤來取代在通訊協定封包中找到的特定位元組值時，會使用這些配對。</span><span class="sxs-lookup"><span data-stu-id="57ab0-115">These pairs are used when you want to display a label in place of a specific BYTE value that is found in the protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="57ab0-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="57ab0-116">Requirements</span></span>



| <span data-ttu-id="57ab0-117">需求</span><span class="sxs-lookup"><span data-stu-id="57ab0-117">Requirement</span></span> | <span data-ttu-id="57ab0-118">值</span><span class="sxs-lookup"><span data-stu-id="57ab0-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="57ab0-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57ab0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="57ab0-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57ab0-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="57ab0-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57ab0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="57ab0-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57ab0-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="57ab0-123">標頭</span><span class="sxs-lookup"><span data-stu-id="57ab0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="57ab0-124"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="57ab0-124"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57ab0-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57ab0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57ab0-126">SET</span><span class="sxs-lookup"><span data-stu-id="57ab0-126">SET</span></span>](set.md)
</dt> </dl>

 

 




