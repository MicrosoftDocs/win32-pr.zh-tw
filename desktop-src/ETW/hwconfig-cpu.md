---
description: HWConfig \_ cpu 類別是 cpu 配置事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: a94714c6-009c-4300-a0a0-b7b3ce94f91e
title: HWConfig_CPU 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_CPU
- HWConfig_CPU.MHz
- HWConfig_CPU.NumberOfProcessors
- HWConfig_CPU.MemSize
- HWConfig_CPU.PageSize
- HWConfig_CPU.AllocationGranularity
- HWConfig_CPU.ComputerName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 493952e25080d4a64e018477ca1b45033c8747af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972509"
---
# <a name="hwconfig_cpu-class"></a><span data-ttu-id="6270e-104">HWConfig \_ CPU 類別</span><span class="sxs-lookup"><span data-stu-id="6270e-104">HWConfig\_CPU class</span></span>

<span data-ttu-id="6270e-105">**HWConfig \_ cpu** 類別是 cpu 配置事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="6270e-105">The **HWConfig\_CPU** class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="6270e-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="6270e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6270e-107">語法</span><span class="sxs-lookup"><span data-stu-id="6270e-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("CPU")]
class HWConfig_CPU : HWConfig
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  string ComputerName;
};
```

## <a name="members"></a><span data-ttu-id="6270e-108">成員</span><span class="sxs-lookup"><span data-stu-id="6270e-108">Members</span></span>

<span data-ttu-id="6270e-109">**HWConfig \_ CPU** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6270e-109">The **HWConfig\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="6270e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6270e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6270e-111">屬性</span><span class="sxs-lookup"><span data-stu-id="6270e-111">Properties</span></span>

<span data-ttu-id="6270e-112">**HWConfig \_ CPU** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6270e-112">The **HWConfig\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6270e-113">AllocationGranularity</span><span class="sxs-lookup"><span data-stu-id="6270e-113">AllocationGranularity</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6270e-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6270e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6270e-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6270e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6270e-116">限定詞： WmiDataId (5) </span><span class="sxs-lookup"><span data-stu-id="6270e-116">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="6270e-117">配置給虛擬記憶體的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="6270e-117">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="6270e-118">ComputerName</span><span class="sxs-lookup"><span data-stu-id="6270e-118">ComputerName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6270e-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6270e-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6270e-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6270e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6270e-121">限定詞： WmiDataId (6) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="6270e-121">Qualifiers: WmiDataId(6), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="6270e-122">電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="6270e-122">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="6270e-123">MemSize</span><span class="sxs-lookup"><span data-stu-id="6270e-123">MemSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6270e-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6270e-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6270e-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6270e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6270e-126">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="6270e-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="6270e-127">作業系統可用的實體記憶體總量。</span><span class="sxs-lookup"><span data-stu-id="6270e-127">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="6270e-128">MHz</span><span class="sxs-lookup"><span data-stu-id="6270e-128">MHz</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6270e-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6270e-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6270e-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6270e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6270e-131">限定詞： WmiDataId (1) </span><span class="sxs-lookup"><span data-stu-id="6270e-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="6270e-132">處理器的最大速度（以 mhz 為單位）。</span><span class="sxs-lookup"><span data-stu-id="6270e-132">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="6270e-133">NumberOfProcessors</span><span class="sxs-lookup"><span data-stu-id="6270e-133">NumberOfProcessors</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6270e-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6270e-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6270e-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6270e-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6270e-136">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="6270e-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="6270e-137">電腦上的處理器數目。</span><span class="sxs-lookup"><span data-stu-id="6270e-137">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="6270e-138">PageSize</span><span class="sxs-lookup"><span data-stu-id="6270e-138">PageSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6270e-139">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6270e-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6270e-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6270e-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6270e-141">限定詞： WmiDataId (4) </span><span class="sxs-lookup"><span data-stu-id="6270e-141">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="6270e-142">交換頁面的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6270e-142">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6270e-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="6270e-143">Requirements</span></span>



| <span data-ttu-id="6270e-144">需求</span><span class="sxs-lookup"><span data-stu-id="6270e-144">Requirement</span></span> | <span data-ttu-id="6270e-145">值</span><span class="sxs-lookup"><span data-stu-id="6270e-145">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="6270e-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6270e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="6270e-147">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6270e-147">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6270e-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6270e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="6270e-149">都不支援</span><span class="sxs-lookup"><span data-stu-id="6270e-149">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="6270e-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6270e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6270e-151">**HWConfig**</span><span class="sxs-lookup"><span data-stu-id="6270e-151">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




