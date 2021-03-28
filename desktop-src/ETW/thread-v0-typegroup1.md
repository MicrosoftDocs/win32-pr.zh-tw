---
description: 這個類別是執行緒事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: cc668fef-48fe-4948-8fe5-4351f7a033d1
title: Thread_V0_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V0_TypeGroup1
- Thread_V0_TypeGroup1.TThreadId
- Thread_V0_TypeGroup1.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f6fa7ae1f50e005fe8f66e918a4a8360a0e8f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972484"
---
# <a name="thread_v0_typegroup1-class"></a><span data-ttu-id="0519e-104">Thread \_ V0 \_ TypeGroup1 類別</span><span class="sxs-lookup"><span data-stu-id="0519e-104">Thread\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="0519e-105">這個類別是執行緒事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="0519e-105">This class is the event type class for thread events.</span></span>

<span data-ttu-id="0519e-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="0519e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0519e-107">語法</span><span class="sxs-lookup"><span data-stu-id="0519e-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_V0_TypeGroup1 : Thread_V0
{
  uint32 TThreadId;
  uint32 ProcessId;
};
```

## <a name="members"></a><span data-ttu-id="0519e-108">成員</span><span class="sxs-lookup"><span data-stu-id="0519e-108">Members</span></span>

<span data-ttu-id="0519e-109">**Thread \_ V0 \_ TypeGroup1** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0519e-109">The **Thread\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="0519e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="0519e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0519e-111">屬性</span><span class="sxs-lookup"><span data-stu-id="0519e-111">Properties</span></span>

<span data-ttu-id="0519e-112">**Thread \_ V0 \_ TypeGroup1** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0519e-112">The **Thread\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0519e-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="0519e-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0519e-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0519e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0519e-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0519e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0519e-116">限定詞： WmiDataId (2) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="0519e-116">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="0519e-117">事件所涉及之執行緒的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="0519e-117">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="0519e-118">TThreadId</span><span class="sxs-lookup"><span data-stu-id="0519e-118">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0519e-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0519e-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0519e-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0519e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0519e-121">限定詞： WmiDataId (1) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="0519e-121">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="0519e-122">事件所涉及之執行緒的執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="0519e-122">Thread identifier of the thread involved in the event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0519e-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="0519e-123">Requirements</span></span>



| <span data-ttu-id="0519e-124">需求</span><span class="sxs-lookup"><span data-stu-id="0519e-124">Requirement</span></span> | <span data-ttu-id="0519e-125">值</span><span class="sxs-lookup"><span data-stu-id="0519e-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0519e-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0519e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0519e-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0519e-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0519e-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0519e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0519e-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0519e-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0519e-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0519e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0519e-131">**執行緒 \_ V0**</span><span class="sxs-lookup"><span data-stu-id="0519e-131">**Thread\_V0**</span></span>](thread-v0.md)
</dt> </dl>

 

 




