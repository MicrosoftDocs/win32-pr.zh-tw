---
description: 這個類別是取樣設定檔事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 75ea1e5e-2554-40bb-aa9d-c6d4942c5801
title: SampledProfile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SampledProfile
- SampledProfile.InstructionPointer
- SampledProfile.ThreadId
- SampledProfile.Count
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3d7a69eef1a2a7988569ffcd930b73a559e18d90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973649"
---
# <a name="sampledprofile-class"></a><span data-ttu-id="38511-104">SampledProfile 類別</span><span class="sxs-lookup"><span data-stu-id="38511-104">SampledProfile class</span></span>

<span data-ttu-id="38511-105">這個類別是取樣設定檔事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="38511-105">This class is the event type class for sampled profile events.</span></span>

<span data-ttu-id="38511-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="38511-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="38511-107">語法</span><span class="sxs-lookup"><span data-stu-id="38511-107">Syntax</span></span>

``` syntax
[EventType{46}, EventTypeName{"SampleProfile"}]
class SampledProfile : PerfInfo
{
  uint32 InstructionPointer;
  uint32 ThreadId;
  uint32 Count;
};
```

## <a name="members"></a><span data-ttu-id="38511-108">成員</span><span class="sxs-lookup"><span data-stu-id="38511-108">Members</span></span>

<span data-ttu-id="38511-109">**SampledProfile** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="38511-109">The **SampledProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="38511-110">屬性</span><span class="sxs-lookup"><span data-stu-id="38511-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38511-111">屬性</span><span class="sxs-lookup"><span data-stu-id="38511-111">Properties</span></span>

<span data-ttu-id="38511-112">**SampledProfile** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="38511-112">The **SampledProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38511-113">**Count**</span><span class="sxs-lookup"><span data-stu-id="38511-113">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38511-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="38511-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38511-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="38511-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38511-116">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="38511-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="38511-117">未使用。</span><span class="sxs-lookup"><span data-stu-id="38511-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="38511-118">**InstructionPointer**</span><span class="sxs-lookup"><span data-stu-id="38511-118">**InstructionPointer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38511-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="38511-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38511-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="38511-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38511-121">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="38511-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="38511-122">取樣處理器時正在執行之映射的位址。</span><span class="sxs-lookup"><span data-stu-id="38511-122">Address of the image that was running at the time the processor was sampled.</span></span>

</dd> <dt>

<span data-ttu-id="38511-123">**ThreadId**</span><span class="sxs-lookup"><span data-stu-id="38511-123">**ThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38511-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="38511-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38511-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="38511-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38511-126">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="38511-126">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="38511-127">取樣處理器時正在執行之執行緒的執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="38511-127">Thread identifier of the thread that was running at the time the processor was sampled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38511-128">備註</span><span class="sxs-lookup"><span data-stu-id="38511-128">Remarks</span></span>

<span data-ttu-id="38511-129">這些事件會提供取樣的執行設定檔。</span><span class="sxs-lookup"><span data-stu-id="38511-129">These events provide a sampled execution profile.</span></span> <span data-ttu-id="38511-130">事件會記錄在處理器上執行的專案。</span><span class="sxs-lookup"><span data-stu-id="38511-130">The event records what was being executed on the processor.</span></span> <span data-ttu-id="38511-131">您可以使用影像事件來識別包含該指令的二進位模組。</span><span class="sxs-lookup"><span data-stu-id="38511-131">You can use the Image events to identify the binary module containing that instruction.</span></span> <span data-ttu-id="38511-132">然後，您可以使用這項資訊，在追蹤期間產生執行設定檔。</span><span class="sxs-lookup"><span data-stu-id="38511-132">You can then use this information to produce an execution profile for the duration of the trace.</span></span>

## <a name="requirements"></a><span data-ttu-id="38511-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="38511-133">Requirements</span></span>



| <span data-ttu-id="38511-134">需求</span><span class="sxs-lookup"><span data-stu-id="38511-134">Requirement</span></span> | <span data-ttu-id="38511-135">值</span><span class="sxs-lookup"><span data-stu-id="38511-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="38511-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38511-136">Minimum supported client</span></span><br/> | <span data-ttu-id="38511-137">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38511-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="38511-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38511-138">Minimum supported server</span></span><br/> | <span data-ttu-id="38511-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38511-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




