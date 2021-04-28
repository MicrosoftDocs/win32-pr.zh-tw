---
description: SystemConfig_V0_CPU 類別-此類別是 CPU 配置事件的事件種類類別。
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
ms.openlocfilehash: de3b63def40cb6ead40f6f4c95625603cfc581ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105986"
---
# <a name="systemconfig_v0_cpu-class"></a><span data-ttu-id="5c130-103">SystemConfig \_ V0 \_ CPU 類別</span><span class="sxs-lookup"><span data-stu-id="5c130-103">SystemConfig\_V0\_CPU class</span></span>

<span data-ttu-id="5c130-104">此類別是 CPU 配置事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="5c130-104">This class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="5c130-105">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="5c130-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c130-106">語法</span><span class="sxs-lookup"><span data-stu-id="5c130-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="5c130-107">成員</span><span class="sxs-lookup"><span data-stu-id="5c130-107">Members</span></span>

<span data-ttu-id="5c130-108">**SystemConfig \_ V0 \_ CPU** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5c130-108">The **SystemConfig\_V0\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="5c130-109">屬性</span><span class="sxs-lookup"><span data-stu-id="5c130-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5c130-110">屬性</span><span class="sxs-lookup"><span data-stu-id="5c130-110">Properties</span></span>

<span data-ttu-id="5c130-111">**SystemConfig \_ V0 \_ CPU** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5c130-111">The **SystemConfig\_V0\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c130-112">**AllocationGranularity**</span><span class="sxs-lookup"><span data-stu-id="5c130-112">**AllocationGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c130-113">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5c130-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c130-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c130-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c130-115">限定詞： **WmiDataId** (5) </span><span class="sxs-lookup"><span data-stu-id="5c130-115">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="5c130-116">配置給虛擬記憶體的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="5c130-116">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="5c130-117">**ComputerName**</span><span class="sxs-lookup"><span data-stu-id="5c130-117">**ComputerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c130-118">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="5c130-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="5c130-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c130-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c130-120">限定詞： **WmiDataId** (6) ， **最大** (256) </span><span class="sxs-lookup"><span data-stu-id="5c130-120">Qualifiers: **WmiDataId** (6), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="5c130-121">電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c130-121">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="5c130-122">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="5c130-122">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c130-123">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="5c130-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="5c130-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c130-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c130-125">限定詞： **WmiDataId** (7) ， **最大** (132) </span><span class="sxs-lookup"><span data-stu-id="5c130-125">Qualifiers: **WmiDataId** (7), **Max** (132)</span></span>
</dt> </dl>

<span data-ttu-id="5c130-126">電腦所屬之網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c130-126">Name of the domain in which the computer is a member.</span></span>

</dd> <dt>

<span data-ttu-id="5c130-127">**MemSize**</span><span class="sxs-lookup"><span data-stu-id="5c130-127">**MemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c130-128">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5c130-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c130-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c130-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c130-130">限定詞： **WmiDataId** (3) </span><span class="sxs-lookup"><span data-stu-id="5c130-130">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="5c130-131">作業系統可用的實體記憶體總量。</span><span class="sxs-lookup"><span data-stu-id="5c130-131">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="5c130-132">**MHz**</span><span class="sxs-lookup"><span data-stu-id="5c130-132">**MHz**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c130-133">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5c130-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c130-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c130-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c130-135">限定詞： **WmiDataId** (1) </span><span class="sxs-lookup"><span data-stu-id="5c130-135">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="5c130-136">處理器的最大速度（以 mhz 為單位）。</span><span class="sxs-lookup"><span data-stu-id="5c130-136">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="5c130-137">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="5c130-137">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c130-138">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5c130-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c130-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c130-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c130-140">限定詞： **WmiDataId** (2) </span><span class="sxs-lookup"><span data-stu-id="5c130-140">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="5c130-141">電腦上的處理器數目。</span><span class="sxs-lookup"><span data-stu-id="5c130-141">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="5c130-142">**PageSize**</span><span class="sxs-lookup"><span data-stu-id="5c130-142">**PageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c130-143">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5c130-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c130-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c130-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c130-145">限定詞： **WmiDataId** (4) </span><span class="sxs-lookup"><span data-stu-id="5c130-145">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="5c130-146">交換頁面的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5c130-146">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c130-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c130-147">Requirements</span></span>



| <span data-ttu-id="5c130-148">需求</span><span class="sxs-lookup"><span data-stu-id="5c130-148">Requirement</span></span> | <span data-ttu-id="5c130-149">值</span><span class="sxs-lookup"><span data-stu-id="5c130-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5c130-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c130-150">Minimum supported client</span></span><br/> | <span data-ttu-id="5c130-151">都不支援</span><span class="sxs-lookup"><span data-stu-id="5c130-151">None supported</span></span><br/>                            |
| <span data-ttu-id="5c130-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c130-152">Minimum supported server</span></span><br/> | <span data-ttu-id="5c130-153">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c130-153">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5c130-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c130-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c130-155">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="5c130-155">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




