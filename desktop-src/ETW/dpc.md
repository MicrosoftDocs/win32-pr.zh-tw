---
description: 這個類別是 (DPC) 事件之裝置延遲程序呼叫的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 46010179-7f0a-47dd-95fd-04d30fc597ba
title: DPC 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DPC
- DPC.InitialTime
- DPC.Routine
api_type:
- NA
api_location: ''
ms.openlocfilehash: e0e756c2b41499a6e5b82129d609befc41d5e916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847776"
---
# <a name="dpc-class"></a><span data-ttu-id="819e3-104">DPC 類別</span><span class="sxs-lookup"><span data-stu-id="819e3-104">DPC class</span></span>

<span data-ttu-id="819e3-105">這個類別是 (DPC) 事件之裝置延遲程序呼叫的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="819e3-105">This class is the event type class for device deferred procedure call (DPC) events.</span></span>

<span data-ttu-id="819e3-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="819e3-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="819e3-107">語法</span><span class="sxs-lookup"><span data-stu-id="819e3-107">Syntax</span></span>

``` syntax
[EventType{66, 68, 69}, EventTypeName{"ThreadDPC", "DPC", "TimerDPC"}]
class DPC : PerfInfo
{
  object InitialTime;
  uint32 Routine;
};
```

## <a name="members"></a><span data-ttu-id="819e3-108">成員</span><span class="sxs-lookup"><span data-stu-id="819e3-108">Members</span></span>

<span data-ttu-id="819e3-109">**DPC** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="819e3-109">The **DPC** class has these types of members:</span></span>

-   [<span data-ttu-id="819e3-110">屬性</span><span class="sxs-lookup"><span data-stu-id="819e3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="819e3-111">屬性</span><span class="sxs-lookup"><span data-stu-id="819e3-111">Properties</span></span>

<span data-ttu-id="819e3-112">**DPC** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="819e3-112">The **DPC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="819e3-113">**InitialTime**</span><span class="sxs-lookup"><span data-stu-id="819e3-113">**InitialTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="819e3-114">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="819e3-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="819e3-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="819e3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="819e3-116">限定詞： WmiDataId (1) ，副檔名 ( "WmiTime" ) </span><span class="sxs-lookup"><span data-stu-id="819e3-116">Qualifiers: WmiDataId(1), Extension("WmiTime")</span></span>
</dt> </dl>

<span data-ttu-id="819e3-117">DPC 進入時間。</span><span class="sxs-lookup"><span data-stu-id="819e3-117">DPC entry time.</span></span>

</dd> <dt>

<span data-ttu-id="819e3-118">**常規**</span><span class="sxs-lookup"><span data-stu-id="819e3-118">**Routine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="819e3-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="819e3-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="819e3-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="819e3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="819e3-121">限定詞： WmiDataId (2) ，指標</span><span class="sxs-lookup"><span data-stu-id="819e3-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="819e3-122">DPC 常式的位址。</span><span class="sxs-lookup"><span data-stu-id="819e3-122">Address of DPC routine.</span></span> <span data-ttu-id="819e3-123">使用具有影像事件的位址，以找出已啟動的映射。</span><span class="sxs-lookup"><span data-stu-id="819e3-123">Use the address with the Image events to find which image started.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="819e3-124">備註</span><span class="sxs-lookup"><span data-stu-id="819e3-124">Remarks</span></span>

<span data-ttu-id="819e3-125">輸入 DPC 時，會記錄這些事件。</span><span class="sxs-lookup"><span data-stu-id="819e3-125">These events are logged when a DPC is entered.</span></span> <span data-ttu-id="819e3-126">您可以使用這些事件來監視和驗證驅動程式和核心模式元件的行為。</span><span class="sxs-lookup"><span data-stu-id="819e3-126">You use these events to monitor and verify the behavior of drivers and kernel-mode components.</span></span> <span data-ttu-id="819e3-127">例如，您可以使用 DPC、ISR 和 Image 事件來判斷在高中斷層級花費太多時間的元件。</span><span class="sxs-lookup"><span data-stu-id="819e3-127">For example, you can use DPC, ISR, and Image events to determine those components that spend too much time at high interrupt levels.</span></span> <span data-ttu-id="819e3-128">DPC 和 ISR 事件具有進入時間戳記，可用來計算常式的持續時間。</span><span class="sxs-lookup"><span data-stu-id="819e3-128">DPC and ISR events have an entry time stamp which is used to compute the duration of the routines.</span></span> <span data-ttu-id="819e3-129">系統會讀取影像事件，以建立對應至特定模組的記憶體區域。</span><span class="sxs-lookup"><span data-stu-id="819e3-129">The image events are read to construct the memory regions that map to certain modules.</span></span> <span data-ttu-id="819e3-130">您可以使用對應來找出包含中斷常式的模組。</span><span class="sxs-lookup"><span data-stu-id="819e3-130">You can use the mapping to locate the module that contains the interrupt routine.</span></span>

<span data-ttu-id="819e3-131">TimerDPC 事件會記錄當 DPC 過期而引發的 DPC，以及執行緒 DPC 執行時的 ThreadDPC 事件記錄。</span><span class="sxs-lookup"><span data-stu-id="819e3-131">The TimerDPC event records when a DPC fires as a result of a timer expiration and the ThreadDPC event records when a threaded DPC executes.</span></span>

## <a name="requirements"></a><span data-ttu-id="819e3-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="819e3-132">Requirements</span></span>



| <span data-ttu-id="819e3-133">需求</span><span class="sxs-lookup"><span data-stu-id="819e3-133">Requirement</span></span> | <span data-ttu-id="819e3-134">值</span><span class="sxs-lookup"><span data-stu-id="819e3-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="819e3-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="819e3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="819e3-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="819e3-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="819e3-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="819e3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="819e3-138">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="819e3-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




