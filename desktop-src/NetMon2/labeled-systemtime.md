---
description: 加上標籤的 \_ SYSTEMTIME 結構會定義在偵測到特定的 SYSTEMTIME 屬性值時所顯示的標籤。
ms.assetid: 307b490a-af8e-4f2a-a45a-33a84fcb4d5c
title: 'LABELED_SYSTEMTIME 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_SYSTEMTIME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4484d5ec55f700410eb80d11d2249cceceef43ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852711"
---
# <a name="labeled_systemtime-structure"></a><span data-ttu-id="21a97-103">標記的 \_ SYSTEMTIME 結構</span><span class="sxs-lookup"><span data-stu-id="21a97-103">LABELED\_SYSTEMTIME structure</span></span>

<span data-ttu-id="21a97-104">加上 **標籤的 \_ SYSTEMTIME** 結構會定義在偵測到特定的 SYSTEMTIME 屬性值時所顯示的標籤。</span><span class="sxs-lookup"><span data-stu-id="21a97-104">The **LABELED\_SYSTEMTIME** structure defines a label that is displayed when a specific SYSTEMTIME property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="21a97-105">語法</span><span class="sxs-lookup"><span data-stu-id="21a97-105">Syntax</span></span>


```C++
typedef struct _LABELED_SYSTEMTIME {
  SYSTEMTIME Value;
  LPSTR      Label;
} LABELED_SYSTEMTIME, *LPLABELED_SYSTEMTIME;
```



## <a name="members"></a><span data-ttu-id="21a97-106">成員</span><span class="sxs-lookup"><span data-stu-id="21a97-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="21a97-107">**值**</span><span class="sxs-lookup"><span data-stu-id="21a97-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="21a97-108">您要偵測之屬性的 SYSTEMTIME 值。</span><span class="sxs-lookup"><span data-stu-id="21a97-108">SYSTEMTIME value of a property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="21a97-109">**標籤**</span><span class="sxs-lookup"><span data-stu-id="21a97-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="21a97-110">偵測到在 **值** 成員中指定的 SYSTEMTIME 值時，所顯示的文字描述或標籤。</span><span class="sxs-lookup"><span data-stu-id="21a97-110">Textual description or label that is displayed when the SYSTEMTIME value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21a97-111">備註</span><span class="sxs-lookup"><span data-stu-id="21a97-111">Remarks</span></span>

<span data-ttu-id="21a97-112">[Set](set.md)結構的 **lpLabeledSystemTimeTable** 成員會指向定義一或多個標籤值 **組的集合** 結構陣列。</span><span class="sxs-lookup"><span data-stu-id="21a97-112">The **lpLabeledSystemTimeTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more label value pairs.</span></span> <span data-ttu-id="21a97-113">當您想要顯示標籤來取代在通訊協定封包中找到的特定 LARGEINT 值時，會使用配對。</span><span class="sxs-lookup"><span data-stu-id="21a97-113">The pairs are used when you want to display a label in place of a specific LARGEINT value that is found in the protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="21a97-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="21a97-114">Requirements</span></span>



| <span data-ttu-id="21a97-115">需求</span><span class="sxs-lookup"><span data-stu-id="21a97-115">Requirement</span></span> | <span data-ttu-id="21a97-116">值</span><span class="sxs-lookup"><span data-stu-id="21a97-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="21a97-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="21a97-117">Minimum supported client</span></span><br/> | <span data-ttu-id="21a97-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21a97-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="21a97-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="21a97-119">Minimum supported server</span></span><br/> | <span data-ttu-id="21a97-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21a97-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="21a97-121">標頭</span><span class="sxs-lookup"><span data-stu-id="21a97-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="21a97-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="21a97-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21a97-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21a97-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21a97-124">SET</span><span class="sxs-lookup"><span data-stu-id="21a97-124">SET</span></span>](set.md)
</dt> </dl>

 

 




