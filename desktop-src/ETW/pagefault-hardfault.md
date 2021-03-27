---
description: 這個類別是硬分頁錯誤事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 9837cc45-6485-46c3-a5d9-0d33e443cd32
title: PageFault_HardFault 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_HardFault
- PageFault_HardFault.InitialTime
- PageFault_HardFault.ReadOffset
- PageFault_HardFault.VirtualAddress
- PageFault_HardFault.FileObject
- PageFault_HardFault.TThreadId
- PageFault_HardFault.ByteCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: 08afd3df20260a8ede63f4d741b3045ce3a39c1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944570"
---
# <a name="pagefault_hardfault-class"></a><span data-ttu-id="6e204-104">PageFault \_ HardFault 類別</span><span class="sxs-lookup"><span data-stu-id="6e204-104">PageFault\_HardFault class</span></span>

<span data-ttu-id="6e204-105">這個類別是硬分頁錯誤事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="6e204-105">This class is the event type class for hard page fault events.</span></span>

<span data-ttu-id="6e204-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="6e204-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e204-107">語法</span><span class="sxs-lookup"><span data-stu-id="6e204-107">Syntax</span></span>

``` syntax
[EventType{32}, EventTypeName{"HardFault"}]
class PageFault_HardFault : PageFault_V2
{
  object InitialTime;
  uint64 ReadOffset;
  uint32 VirtualAddress;
  uint32 FileObject;
  uint32 TThreadId;
  uint32 ByteCount;
};
```

## <a name="members"></a><span data-ttu-id="6e204-108">成員</span><span class="sxs-lookup"><span data-stu-id="6e204-108">Members</span></span>

<span data-ttu-id="6e204-109">**PageFault \_ HardFault** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6e204-109">The **PageFault\_HardFault** class has these types of members:</span></span>

-   [<span data-ttu-id="6e204-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6e204-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6e204-111">屬性</span><span class="sxs-lookup"><span data-stu-id="6e204-111">Properties</span></span>

<span data-ttu-id="6e204-112">**PageFault \_ HardFault** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6e204-112">The **PageFault\_HardFault** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6e204-113">**ByteCount**</span><span class="sxs-lookup"><span data-stu-id="6e204-113">**ByteCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e204-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6e204-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e204-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6e204-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e204-116">限定詞： WmiDataId (6) </span><span class="sxs-lookup"><span data-stu-id="6e204-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="6e204-117">從 ReadOffset 讀取來滿足錯誤的資料量。</span><span class="sxs-lookup"><span data-stu-id="6e204-117">Amount of data read from ReadOffset to satisfy the fault.</span></span>

</dd> <dt>

<span data-ttu-id="6e204-118">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="6e204-118">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e204-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6e204-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e204-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6e204-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e204-121">限定詞： WmiDataId (4) ，指標</span><span class="sxs-lookup"><span data-stu-id="6e204-121">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6e204-122">將 this 指標的值與 [**FileIo \_ Name**](fileio-name.md)事件中的 **FileObject** 指標值比對，以判斷檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e204-122">Match the value of this pointer to the **FileObject** pointer value in a [**FileIo\_Name**](fileio-name.md) event to determine the name of the file.</span></span>

</dd> <dt>

<span data-ttu-id="6e204-123">**InitialTime**</span><span class="sxs-lookup"><span data-stu-id="6e204-123">**InitialTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e204-124">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="6e204-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="6e204-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6e204-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e204-126">限定詞： WmiDataId (1) ，副檔名 ( "WmiTime" ) </span><span class="sxs-lookup"><span data-stu-id="6e204-126">Qualifiers: WmiDataId(1), Extension("WmiTime")</span></span>
</dt> </dl>

<span data-ttu-id="6e204-127">發生分頁錯誤的開始時間戳。</span><span class="sxs-lookup"><span data-stu-id="6e204-127">Start time stamp at which page fault occurred.</span></span>

</dd> <dt>

<span data-ttu-id="6e204-128">**ReadOffset**</span><span class="sxs-lookup"><span data-stu-id="6e204-128">**ReadOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e204-129">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="6e204-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6e204-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6e204-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e204-131">限定詞： WmiDataId (2) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="6e204-131">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="6e204-132">從中讀取資料以滿足錯誤的檔案位移。</span><span class="sxs-lookup"><span data-stu-id="6e204-132">File offset from which data was read to satisfy fault.</span></span>

</dd> <dt>

<span data-ttu-id="6e204-133">**TThreadId**</span><span class="sxs-lookup"><span data-stu-id="6e204-133">**TThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e204-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6e204-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e204-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6e204-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e204-136">限定詞： WmiDataId (5) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="6e204-136">Qualifiers: WmiDataId(5), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="6e204-137">發生分頁錯誤之執行緒的執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e204-137">Thread identifier of the thread that encountered the page fault.</span></span>

</dd> <dt>

<span data-ttu-id="6e204-138">**VirtualAddress**</span><span class="sxs-lookup"><span data-stu-id="6e204-138">**VirtualAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e204-139">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6e204-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e204-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6e204-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e204-141">限定詞： WmiDataId (3) ，指標</span><span class="sxs-lookup"><span data-stu-id="6e204-141">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6e204-142">錯誤的位址。</span><span class="sxs-lookup"><span data-stu-id="6e204-142">Faulting address.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6e204-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e204-143">Requirements</span></span>



| <span data-ttu-id="6e204-144">需求</span><span class="sxs-lookup"><span data-stu-id="6e204-144">Requirement</span></span> | <span data-ttu-id="6e204-145">值</span><span class="sxs-lookup"><span data-stu-id="6e204-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6e204-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e204-146">Minimum supported client</span></span><br/> | <span data-ttu-id="6e204-147">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e204-147">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6e204-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e204-148">Minimum supported server</span></span><br/> | <span data-ttu-id="6e204-149">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e204-149">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6e204-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e204-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e204-151">**PageFault \_ V2**</span><span class="sxs-lookup"><span data-stu-id="6e204-151">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




