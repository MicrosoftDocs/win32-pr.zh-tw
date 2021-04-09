---
description: PF \_ FOLLOWENTRY 結構會定義網路監視器新增至一組剖析器的通訊協定。
ms.assetid: 931ae70f-8c5e-4b7a-aae6-64a33dac3b23
title: 'PF_FOLLOWENTRY 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f93ec4784fc8d0f92f68fdff3914e230ffd3cdce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850147"
---
# <a name="pf_followentry-structure"></a><span data-ttu-id="ca441-103">PF \_ FOLLOWENTRY 結構</span><span class="sxs-lookup"><span data-stu-id="ca441-103">PF\_FOLLOWENTRY structure</span></span>

<span data-ttu-id="ca441-104">**PF \_ FOLLOWENTRY** 結構會定義網路監視器新增至一組剖析器的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="ca441-104">The **PF\_FOLLOWENTRY** structure defines a protocol that Network Monitor adds to the follow set of a parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca441-105">語法</span><span class="sxs-lookup"><span data-stu-id="ca441-105">Syntax</span></span>


```C++
typedef struct _PF_FOLLOWENTRY {
  char szProtocol[MAX_PROTOCOL_NAME_LEN];
} PF_FOLLOWENTRY, *PPF_FOLLOWENTRY;
```



## <a name="members"></a><span data-ttu-id="ca441-106">成員</span><span class="sxs-lookup"><span data-stu-id="ca441-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ca441-107">**szProtocol**</span><span class="sxs-lookup"><span data-stu-id="ca441-107">**szProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="ca441-108">通訊協定的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca441-108">The name of the protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca441-109">備註</span><span class="sxs-lookup"><span data-stu-id="ca441-109">Remarks</span></span>

<span data-ttu-id="ca441-110">[Pf \_ FOLLOWSET](pf-followset.md)結構會使用 **pf \_ FOLLOWENTRY** 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="ca441-110">The [PF\_FOLLOWSET](pf-followset.md) structure uses an array of **PF\_FOLLOWENTRY** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca441-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca441-111">Requirements</span></span>



| <span data-ttu-id="ca441-112">需求</span><span class="sxs-lookup"><span data-stu-id="ca441-112">Requirement</span></span> | <span data-ttu-id="ca441-113">值</span><span class="sxs-lookup"><span data-stu-id="ca441-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ca441-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ca441-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ca441-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca441-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ca441-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ca441-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ca441-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca441-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ca441-118">標頭</span><span class="sxs-lookup"><span data-stu-id="ca441-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca441-119"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="ca441-119"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca441-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca441-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca441-121">PF \_ FOLLOWSET</span><span class="sxs-lookup"><span data-stu-id="ca441-121">PF\_FOLLOWSET</span></span>](pf-followset.md)
</dt> </dl>

 

 




