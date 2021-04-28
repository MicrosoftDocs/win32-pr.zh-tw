---
description: SystemConfig_CPU 類別-此類別是 CPU 配置事件的事件種類類別。
ms.assetid: 5a24be04-9e5e-4ba9-baaf-b58b79ad947b
title: SystemConfig_CPU 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_CPU
- SystemConfig_CPU.MHz
- SystemConfig_CPU.NumberOfProcessors
- SystemConfig_CPU.MemSize
- SystemConfig_CPU.PageSize
- SystemConfig_CPU.AllocationGranularity
- SystemConfig_CPU.ComputerName
- SystemConfig_CPU.DomainName
- SystemConfig_CPU.HyperThreadingFlag
api_type:
- NA
api_location: ''
ms.openlocfilehash: 07efa01bf58aeadfdfe12cd5db4d010a7f6dbca0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106116"
---
# <a name="systemconfig_cpu-class"></a><span data-ttu-id="c0449-103">SystemConfig \_ CPU 類別</span><span class="sxs-lookup"><span data-stu-id="c0449-103">SystemConfig\_CPU class</span></span>

<span data-ttu-id="c0449-104">此類別是 CPU 配置事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="c0449-104">This class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="c0449-105">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="c0449-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0449-106">語法</span><span class="sxs-lookup"><span data-stu-id="c0449-106">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("CPU")]
class SystemConfig_CPU : SystemConfig
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  char16 ComputerName[];
  char16 DomainName[];
  uint32 HyperThreadingFlag;
};
```

## <a name="members"></a><span data-ttu-id="c0449-107">成員</span><span class="sxs-lookup"><span data-stu-id="c0449-107">Members</span></span>

<span data-ttu-id="c0449-108">**SystemConfig \_ CPU** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c0449-108">The **SystemConfig\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="c0449-109">屬性</span><span class="sxs-lookup"><span data-stu-id="c0449-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c0449-110">屬性</span><span class="sxs-lookup"><span data-stu-id="c0449-110">Properties</span></span>

<span data-ttu-id="c0449-111">**SystemConfig \_ CPU** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c0449-111">The **SystemConfig\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c0449-112">**AllocationGranularity**</span><span class="sxs-lookup"><span data-stu-id="c0449-112">**AllocationGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0449-113">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c0449-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0449-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0449-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0449-115">限定詞： **WmiDataId** (5) </span><span class="sxs-lookup"><span data-stu-id="c0449-115">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="c0449-116">配置給虛擬記憶體的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="c0449-116">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="c0449-117">**ComputerName**</span><span class="sxs-lookup"><span data-stu-id="c0449-117">**ComputerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0449-118">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="c0449-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="c0449-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0449-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0449-120">限定詞： **WmiDataId** (6) ， **最大** (256) ， **格式 ( "s" )**</span><span class="sxs-lookup"><span data-stu-id="c0449-120">Qualifiers: **WmiDataId** (6), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="c0449-121">電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0449-121">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="c0449-122">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="c0449-122">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0449-123">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="c0449-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="c0449-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0449-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0449-125">限定詞： **WmiDataId** (7) ， **最大** (132) ， **格式 ( "s" )**</span><span class="sxs-lookup"><span data-stu-id="c0449-125">Qualifiers: **WmiDataId** (7), **Max** (132), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="c0449-126">電腦所屬之網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0449-126">Name of the domain in which the computer is a member.</span></span>

</dd> <dt>

<span data-ttu-id="c0449-127">**HyperThreadingFlag**</span><span class="sxs-lookup"><span data-stu-id="c0449-127">**HyperThreadingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0449-128">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c0449-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0449-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0449-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0449-130">限定詞： **WmiDataId** (8) ，指標</span><span class="sxs-lookup"><span data-stu-id="c0449-130">Qualifiers: **WmiDataId** (8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c0449-131">表示處理器的超執行緒選項是開啟或關閉。</span><span class="sxs-lookup"><span data-stu-id="c0449-131">Indicates if the hyper-threading option is on or off for a processor.</span></span> <span data-ttu-id="c0449-132">每個位會反映電腦上 CPU 的超執行緒狀態。</span><span class="sxs-lookup"><span data-stu-id="c0449-132">Each bit reflects the hyper-threading state of a CPU on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="c0449-133">**MemSize**</span><span class="sxs-lookup"><span data-stu-id="c0449-133">**MemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0449-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c0449-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0449-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0449-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0449-136">限定詞： **WmiDataId** (3) </span><span class="sxs-lookup"><span data-stu-id="c0449-136">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="c0449-137">作業系統可用的實體記憶體總量。</span><span class="sxs-lookup"><span data-stu-id="c0449-137">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="c0449-138">**MHz**</span><span class="sxs-lookup"><span data-stu-id="c0449-138">**MHz**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0449-139">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c0449-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0449-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0449-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0449-141">限定詞： **WmiDataId** (1) </span><span class="sxs-lookup"><span data-stu-id="c0449-141">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="c0449-142">處理器的最大速度（以 mhz 為單位）。</span><span class="sxs-lookup"><span data-stu-id="c0449-142">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="c0449-143">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="c0449-143">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0449-144">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c0449-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0449-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0449-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0449-146">限定詞： **WmiDataId** (2) </span><span class="sxs-lookup"><span data-stu-id="c0449-146">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="c0449-147">電腦上的處理器數目。</span><span class="sxs-lookup"><span data-stu-id="c0449-147">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="c0449-148">**PageSize**</span><span class="sxs-lookup"><span data-stu-id="c0449-148">**PageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0449-149">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c0449-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0449-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0449-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0449-151">限定詞： **WmiDataId** (4) </span><span class="sxs-lookup"><span data-stu-id="c0449-151">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="c0449-152">交換頁面的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c0449-152">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0449-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0449-153">Requirements</span></span>



| <span data-ttu-id="c0449-154">需求</span><span class="sxs-lookup"><span data-stu-id="c0449-154">Requirement</span></span> | <span data-ttu-id="c0449-155">值</span><span class="sxs-lookup"><span data-stu-id="c0449-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c0449-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0449-156">Minimum supported client</span></span><br/> | <span data-ttu-id="c0449-157">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0449-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c0449-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0449-158">Minimum supported server</span></span><br/> | <span data-ttu-id="c0449-159">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0449-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c0449-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0449-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0449-161">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="c0449-161">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




