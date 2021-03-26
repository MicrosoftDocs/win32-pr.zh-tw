---
description: 此類別是 CPU 配置事件的事件種類類別。
ms.assetid: 9ca77676-ff0e-4c47-ae4e-f8192376d3ca
title: SystemConfig_V0_CPU 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_CPU
- SystemConfig_V0_CPU.MHz
- SystemConfig_V0_CPU.NumberOfProcessors
- SystemConfig_V0_CPU.MemSize
- SystemConfig_V0_CPU.PageSize
- SystemConfig_V0_CPU.AllocationGranularity
- SystemConfig_V0_CPU.ComputerName
- SystemConfig_V0_CPU.DomainName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6963201f76afa40e9b1741dc2936fa2ab4433a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945072"
---
# <a name="systemconfig_v0_cpu-class"></a><span data-ttu-id="411ba-103">SystemConfig \_ V0 \_ CPU 類別</span><span class="sxs-lookup"><span data-stu-id="411ba-103">SystemConfig\_V0\_CPU class</span></span>

<span data-ttu-id="411ba-104">此類別是 CPU 配置事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="411ba-104">This class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="411ba-105">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="411ba-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="411ba-106">語法</span><span class="sxs-lookup"><span data-stu-id="411ba-106">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("CPU")]
class SystemConfig_V0_CPU : SystemConfig_V0
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  char16 ComputerName[];
  char16 DomainName[];
};
```

## <a name="members"></a><span data-ttu-id="411ba-107">成員</span><span class="sxs-lookup"><span data-stu-id="411ba-107">Members</span></span>

<span data-ttu-id="411ba-108">**SystemConfig \_ V0 \_ CPU** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="411ba-108">The **SystemConfig\_V0\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="411ba-109">屬性</span><span class="sxs-lookup"><span data-stu-id="411ba-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="411ba-110">屬性</span><span class="sxs-lookup"><span data-stu-id="411ba-110">Properties</span></span>

<span data-ttu-id="411ba-111">**SystemConfig \_ V0 \_ CPU** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="411ba-111">The **SystemConfig\_V0\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="411ba-112">**AllocationGranularity**</span><span class="sxs-lookup"><span data-stu-id="411ba-112">**AllocationGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="411ba-113">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="411ba-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="411ba-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="411ba-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="411ba-115">限定詞： **WmiDataId** (5) </span><span class="sxs-lookup"><span data-stu-id="411ba-115">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="411ba-116">配置給虛擬記憶體的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="411ba-116">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="411ba-117">**ComputerName**</span><span class="sxs-lookup"><span data-stu-id="411ba-117">**ComputerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="411ba-118">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="411ba-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="411ba-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="411ba-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="411ba-120">限定詞： **WmiDataId** (6) ， **最大** (256) </span><span class="sxs-lookup"><span data-stu-id="411ba-120">Qualifiers: **WmiDataId** (6), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="411ba-121">電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="411ba-121">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="411ba-122">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="411ba-122">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="411ba-123">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="411ba-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="411ba-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="411ba-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="411ba-125">限定詞： **WmiDataId** (7) ， **最大** (132) </span><span class="sxs-lookup"><span data-stu-id="411ba-125">Qualifiers: **WmiDataId** (7), **Max** (132)</span></span>
</dt> </dl>

<span data-ttu-id="411ba-126">電腦所屬之網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="411ba-126">Name of the domain in which the computer is a member.</span></span>

</dd> <dt>

<span data-ttu-id="411ba-127">**MemSize**</span><span class="sxs-lookup"><span data-stu-id="411ba-127">**MemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="411ba-128">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="411ba-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="411ba-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="411ba-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="411ba-130">限定詞： **WmiDataId** (3) </span><span class="sxs-lookup"><span data-stu-id="411ba-130">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="411ba-131">作業系統可用的實體記憶體總量。</span><span class="sxs-lookup"><span data-stu-id="411ba-131">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="411ba-132">**MHz**</span><span class="sxs-lookup"><span data-stu-id="411ba-132">**MHz**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="411ba-133">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="411ba-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="411ba-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="411ba-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="411ba-135">限定詞： **WmiDataId** (1) </span><span class="sxs-lookup"><span data-stu-id="411ba-135">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="411ba-136">處理器的最大速度（以 mhz 為單位）。</span><span class="sxs-lookup"><span data-stu-id="411ba-136">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="411ba-137">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="411ba-137">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="411ba-138">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="411ba-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="411ba-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="411ba-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="411ba-140">限定詞： **WmiDataId** (2) </span><span class="sxs-lookup"><span data-stu-id="411ba-140">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="411ba-141">電腦上的處理器數目。</span><span class="sxs-lookup"><span data-stu-id="411ba-141">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="411ba-142">**PageSize**</span><span class="sxs-lookup"><span data-stu-id="411ba-142">**PageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="411ba-143">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="411ba-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="411ba-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="411ba-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="411ba-145">限定詞： **WmiDataId** (4) </span><span class="sxs-lookup"><span data-stu-id="411ba-145">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="411ba-146">交換頁面的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="411ba-146">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="411ba-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="411ba-147">Requirements</span></span>



| <span data-ttu-id="411ba-148">需求</span><span class="sxs-lookup"><span data-stu-id="411ba-148">Requirement</span></span> | <span data-ttu-id="411ba-149">值</span><span class="sxs-lookup"><span data-stu-id="411ba-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="411ba-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="411ba-150">Minimum supported client</span></span><br/> | <span data-ttu-id="411ba-151">都不支援</span><span class="sxs-lookup"><span data-stu-id="411ba-151">None supported</span></span><br/>                            |
| <span data-ttu-id="411ba-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="411ba-152">Minimum supported server</span></span><br/> | <span data-ttu-id="411ba-153">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="411ba-153">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="411ba-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="411ba-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="411ba-155">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="411ba-155">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




