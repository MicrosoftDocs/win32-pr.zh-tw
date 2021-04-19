---
description: 觸發程式結構指出驅動程式在指定時間所要採取的動作。
ms.assetid: 63541796-b0d8-456c-8544-697fedbe05f7
title: '觸發程式結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TRIGGER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: d9b385557e3c34bdf75f2bf959d4e5e3e47e0750
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985021"
---
# <a name="trigger-structure"></a><span data-ttu-id="b507f-103">觸發程式結構</span><span class="sxs-lookup"><span data-stu-id="b507f-103">TRIGGER structure</span></span>

<span data-ttu-id="b507f-104">**觸發** 程式結構指出驅動程式在指定時間所要採取的動作。</span><span class="sxs-lookup"><span data-stu-id="b507f-104">The **TRIGGER** structure indicates an action to be taken by the driver at a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="b507f-105">語法</span><span class="sxs-lookup"><span data-stu-id="b507f-105">Syntax</span></span>


```C++
typedef struct _TRIGGER {
  BOOL         TriggerActive;
  BYTE         TriggerType;
  BYTE         TriggerAction;
  DWORD        TriggerFlags;
  PATTERNMATCH TriggerPatternMatch;
  DWORD        TriggerBufferSize;
  DWORD        Reserved;
} TRIGGER, *LPTRIGGER;
```



## <a name="members"></a><span data-ttu-id="b507f-106">成員</span><span class="sxs-lookup"><span data-stu-id="b507f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b507f-107">**TriggerActive**</span><span class="sxs-lookup"><span data-stu-id="b507f-107">**TriggerActive**</span></span>
</dt> <dd>

<span data-ttu-id="b507f-108">布林值，決定是否要由驅動程式來注意觸發程式。</span><span class="sxs-lookup"><span data-stu-id="b507f-108">A Boolean value that determines if the trigger should be paid attention to by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="b507f-109">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="b507f-109">**TriggerType**</span></span>
</dt> <dd>

<span data-ttu-id="b507f-110">觸發程式的 op 程式碼。</span><span class="sxs-lookup"><span data-stu-id="b507f-110">The op code of the trigger.</span></span>

</dd> <dt>

<span data-ttu-id="b507f-111">**TriggerAction**</span><span class="sxs-lookup"><span data-stu-id="b507f-111">**TriggerAction**</span></span>
</dt> <dd>

<span data-ttu-id="b507f-112">觸發程式在引發時所要採取的動作。</span><span class="sxs-lookup"><span data-stu-id="b507f-112">Action that the trigger is to take if it is fired.</span></span>

</dd> <dt>

<span data-ttu-id="b507f-113">**TriggerFlags**</span><span class="sxs-lookup"><span data-stu-id="b507f-113">**TriggerFlags**</span></span>
</dt> <dd>

<span data-ttu-id="b507f-114">觸發程式旗標。</span><span class="sxs-lookup"><span data-stu-id="b507f-114">Trigger flags.</span></span>

</dd> <dt>

<span data-ttu-id="b507f-115">**TriggerPatternMatch**</span><span class="sxs-lookup"><span data-stu-id="b507f-115">**TriggerPatternMatch**</span></span>
</dt> <dd>

<span data-ttu-id="b507f-116">觸發程式模式相符。</span><span class="sxs-lookup"><span data-stu-id="b507f-116">The trigger pattern match.</span></span>

</dd> <dt>

<span data-ttu-id="b507f-117">**TriggerBufferSize**</span><span class="sxs-lookup"><span data-stu-id="b507f-117">**TriggerBufferSize**</span></span>
</dt> <dd>

<span data-ttu-id="b507f-118">觸發緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="b507f-118">Trigger buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="b507f-119">**已保留**</span><span class="sxs-lookup"><span data-stu-id="b507f-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="b507f-120">保留的。</span><span class="sxs-lookup"><span data-stu-id="b507f-120">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b507f-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b507f-121">Requirements</span></span>



| <span data-ttu-id="b507f-122">需求</span><span class="sxs-lookup"><span data-stu-id="b507f-122">Requirement</span></span> | <span data-ttu-id="b507f-123">值</span><span class="sxs-lookup"><span data-stu-id="b507f-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b507f-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b507f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b507f-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b507f-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b507f-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b507f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b507f-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b507f-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b507f-128">標頭</span><span class="sxs-lookup"><span data-stu-id="b507f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b507f-129"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="b507f-129"><dt>Netmon.h</dt></span></span> </dl> |



 

 




