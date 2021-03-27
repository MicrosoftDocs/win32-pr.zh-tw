---
description: 這個類別是執行緒啟動事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 412de56f-4f54-46e8-ab60-d47371247e79
title: Thread_V1_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup1
- Thread_V1_TypeGroup1.ProcessId
- Thread_V1_TypeGroup1.TThreadId
- Thread_V1_TypeGroup1.StackBase
- Thread_V1_TypeGroup1.StackLimit
- Thread_V1_TypeGroup1.UserStackBase
- Thread_V1_TypeGroup1.UserStackLimit
- Thread_V1_TypeGroup1.StartAddr
- Thread_V1_TypeGroup1.Win32StartAddr
- Thread_V1_TypeGroup1.WaitMode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 13c419b417b614eb9022d1cb7c09a84ca705b3dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944485"
---
# <a name="thread_v1_typegroup1-class"></a><span data-ttu-id="6e6a8-104">Thread \_ V1 \_ TypeGroup1 類別</span><span class="sxs-lookup"><span data-stu-id="6e6a8-104">Thread\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="6e6a8-105">這個類別是執行緒啟動事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="6e6a8-105">This class is the event type class for thread start events.</span></span>

<span data-ttu-id="6e6a8-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="6e6a8-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e6a8-107">語法</span><span class="sxs-lookup"><span data-stu-id="6e6a8-107">Syntax</span></span>

``` syntax
[EventType{1, 3}, EventTypeName{"Start", "DCStart"}]
class Thread_V1_TypeGroup1 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  sint8  WaitMode;
};
```

## <a name="members"></a><span data-ttu-id="6e6a8-108">成員</span><span class="sxs-lookup"><span data-stu-id="6e6a8-108">Members</span></span>

<span data-ttu-id="6e6a8-109">**Thread \_ V1 \_ TypeGroup1** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6e6a8-109">The **Thread\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="6e6a8-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6e6a8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6e6a8-111">屬性</span><span class="sxs-lookup"><span data-stu-id="6e6a8-111">Properties</span></span>

<span data-ttu-id="6e6a8-112">**Thread \_ V1 \_ TypeGroup1** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6e6a8-112">The **Thread\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6e6a8-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="6e6a8-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e6a8-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6e6a8-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e6a8-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6e6a8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e6a8-116">限定詞： WmiDataId (1) </span><span class="sxs-lookup"><span data-stu-id="6e6a8-116">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="6e6a8-117">事件所涉及之執行緒的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e6a8-117">Process identifier of the thread involved in the event.</span></span>

<span data-ttu-id="6e6a8-118">**Windows Server 2003：** 包含 ( "x" ) 限定詞的格式。</span><span class="sxs-lookup"><span data-stu-id="6e6a8-118">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="6e6a8-119">StackBase</span><span class="sxs-lookup"><span data-stu-id="6e6a8-119">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e6a8-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6e6a8-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e6a8-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6e6a8-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e6a8-122">限定詞： WmiDataId (3) ，指標</span><span class="sxs-lookup"><span data-stu-id="6e6a8-122">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6e6a8-123">執行緒堆疊的基底位址。</span><span class="sxs-lookup"><span data-stu-id="6e6a8-123">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="6e6a8-124">StackLimit</span><span class="sxs-lookup"><span data-stu-id="6e6a8-124">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e6a8-125">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6e6a8-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e6a8-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6e6a8-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e6a8-127">限定詞： WmiDataId (4) ，指標</span><span class="sxs-lookup"><span data-stu-id="6e6a8-127">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6e6a8-128">執行緒堆疊的限制。</span><span class="sxs-lookup"><span data-stu-id="6e6a8-128">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="6e6a8-129">StartAddr</span><span class="sxs-lookup"><span data-stu-id="6e6a8-129">StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e6a8-130">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6e6a8-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e6a8-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6e6a8-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e6a8-132">限定詞： WmiDataId (7) ，指標</span><span class="sxs-lookup"><span data-stu-id="6e6a8-132">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6e6a8-133">追蹤開始的記憶體位址。</span><span class="sxs-lookup"><span data-stu-id="6e6a8-133">Memory address at which the trace starts.</span></span>

</dd> <dt>

<span data-ttu-id="6e6a8-134">TThreadId</span><span class="sxs-lookup"><span data-stu-id="6e6a8-134">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e6a8-135">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6e6a8-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e6a8-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6e6a8-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e6a8-137">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="6e6a8-137">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="6e6a8-138">事件所涉及之執行緒的執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e6a8-138">Thread identifier of the thread involved in the event.</span></span>

<span data-ttu-id="6e6a8-139">**Windows Server 2003：** 包含 ( "x" ) 限定詞的格式。</span><span class="sxs-lookup"><span data-stu-id="6e6a8-139">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="6e6a8-140">UserStackBase</span><span class="sxs-lookup"><span data-stu-id="6e6a8-140">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e6a8-141">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6e6a8-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e6a8-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6e6a8-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e6a8-143">限定詞： WmiDataId (5) ，指標</span><span class="sxs-lookup"><span data-stu-id="6e6a8-143">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6e6a8-144">執行緒使用者模式堆疊的基底位址。</span><span class="sxs-lookup"><span data-stu-id="6e6a8-144">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="6e6a8-145">UserStackLimit</span><span class="sxs-lookup"><span data-stu-id="6e6a8-145">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e6a8-146">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6e6a8-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e6a8-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6e6a8-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e6a8-148">限定詞： WmiDataId (6) ，指標</span><span class="sxs-lookup"><span data-stu-id="6e6a8-148">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6e6a8-149">執行緒使用者模式堆疊的限制。</span><span class="sxs-lookup"><span data-stu-id="6e6a8-149">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="6e6a8-150">WaitMode</span><span class="sxs-lookup"><span data-stu-id="6e6a8-150">WaitMode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e6a8-151">資料類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="6e6a8-151">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="6e6a8-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6e6a8-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e6a8-153">限定詞： WmiDataId (9) ，Format ( "c" ) </span><span class="sxs-lookup"><span data-stu-id="6e6a8-153">Qualifiers: WmiDataId(9), Format("c")</span></span>
</dt> </dl>

<span data-ttu-id="6e6a8-154">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e6a8-154">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="6e6a8-155">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="6e6a8-155">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e6a8-156">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6e6a8-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e6a8-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6e6a8-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e6a8-158">限定詞： WmiDataId (8) ，指標</span><span class="sxs-lookup"><span data-stu-id="6e6a8-158">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6e6a8-159">此執行緒要執行之函式的起始位址。</span><span class="sxs-lookup"><span data-stu-id="6e6a8-159">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6e6a8-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e6a8-160">Requirements</span></span>



| <span data-ttu-id="6e6a8-161">需求</span><span class="sxs-lookup"><span data-stu-id="6e6a8-161">Requirement</span></span> | <span data-ttu-id="6e6a8-162">值</span><span class="sxs-lookup"><span data-stu-id="6e6a8-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6e6a8-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e6a8-163">Minimum supported client</span></span><br/> | <span data-ttu-id="6e6a8-164">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e6a8-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6e6a8-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e6a8-165">Minimum supported server</span></span><br/> | <span data-ttu-id="6e6a8-166">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e6a8-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6e6a8-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e6a8-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e6a8-168">**執行緒 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="6e6a8-168">**Thread\_V1**</span></span>](thread-v1.md)
</dt> </dl>

 

 




