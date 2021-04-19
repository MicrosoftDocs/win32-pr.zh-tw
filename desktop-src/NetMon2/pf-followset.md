---
description: PF \_ FOLLOWSET 結構會定義可能在通訊協定之前或之後的通訊協定。
ms.assetid: ef444af9-edae-4547-9548-8a682c279f08
title: 'PF_FOLLOWSET 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f5c286d3b137df24f7da7f0fc5ae269a7a3d946d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984216"
---
# <a name="pf_followset-structure"></a><span data-ttu-id="02ed9-103">PF \_ FOLLOWSET 結構</span><span class="sxs-lookup"><span data-stu-id="02ed9-103">PF\_FOLLOWSET structure</span></span>

<span data-ttu-id="02ed9-104">**PF \_ FOLLOWSET** 結構會定義可能在通訊協定之前或之後的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="02ed9-104">The **PF\_FOLLOWSET** structure defines the protocols that may precede or follow a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="02ed9-105">語法</span><span class="sxs-lookup"><span data-stu-id="02ed9-105">Syntax</span></span>


```C++
typedef struct _PF_FOLLOWSET {
  DWORD          nEntries;
  PF_FOLLOWENTRY Entry[];
} PF_FOLLOWSET, *PPF_FOLLOWSET;
```



## <a name="members"></a><span data-ttu-id="02ed9-106">成員</span><span class="sxs-lookup"><span data-stu-id="02ed9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="02ed9-107">**nEntries**</span><span class="sxs-lookup"><span data-stu-id="02ed9-107">**nEntries**</span></span>
</dt> <dd>

<span data-ttu-id="02ed9-108">清單中的通訊協定數目。</span><span class="sxs-lookup"><span data-stu-id="02ed9-108">Number of protocols in the list.</span></span>

</dd> <dt>

<span data-ttu-id="02ed9-109">**進入**</span><span class="sxs-lookup"><span data-stu-id="02ed9-109">**Entry**</span></span>
</dt> <dd>

<span data-ttu-id="02ed9-110">描述每個通訊協定的 [PF \_ FOLLOWENTRY](pf-followentry.md) 結構陣列。</span><span class="sxs-lookup"><span data-stu-id="02ed9-110">Array of [PF\_FOLLOWENTRY](pf-followentry.md) structures that describe each protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02ed9-111">備註</span><span class="sxs-lookup"><span data-stu-id="02ed9-111">Remarks</span></span>

<span data-ttu-id="02ed9-112">[Pf \_ PARSERINFO](pf-parserinfo.md)結構會使用 **pf \_ FOLLOWSET** 結構來列出剖析器偵測到的通訊協定之前或之後的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="02ed9-112">The [PF\_PARSERINFO](pf-parserinfo.md) structure uses the **PF\_FOLLOWSET** structure to list the protocols that may precede or follow the protocol that the parser detects.</span></span>

<span data-ttu-id="02ed9-113">網路監視器使用 **PF \_ FOLLOWSET** 結構中的資訊來更新下列特定剖析器的集合。</span><span class="sxs-lookup"><span data-stu-id="02ed9-113">Network Monitor uses the information in the **PF\_FOLLOWSET** structure to update the follow sets of specific parsers.</span></span> <span data-ttu-id="02ed9-114">您必須使用 **HeapAlloc** 來配置 **PF \_ FOLLOWSET** 結構。</span><span class="sxs-lookup"><span data-stu-id="02ed9-114">The **PF\_FOLLOWSET** structure must be allocated using **HeapAlloc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="02ed9-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="02ed9-115">Requirements</span></span>



| <span data-ttu-id="02ed9-116">需求</span><span class="sxs-lookup"><span data-stu-id="02ed9-116">Requirement</span></span> | <span data-ttu-id="02ed9-117">值</span><span class="sxs-lookup"><span data-stu-id="02ed9-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="02ed9-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02ed9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="02ed9-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02ed9-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="02ed9-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02ed9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="02ed9-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02ed9-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="02ed9-122">標頭</span><span class="sxs-lookup"><span data-stu-id="02ed9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="02ed9-123"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="02ed9-123"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02ed9-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02ed9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02ed9-125">PF \_ FOLLOWENTRY</span><span class="sxs-lookup"><span data-stu-id="02ed9-125">PF\_FOLLOWENTRY</span></span>](pf-followentry.md)
</dt> <dt>

[<span data-ttu-id="02ed9-126">PF \_ PARSERINFO</span><span class="sxs-lookup"><span data-stu-id="02ed9-126">PF\_PARSERINFO</span></span>](pf-parserinfo.md)
</dt> </dl>

 

 




