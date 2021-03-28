---
description: 這個類別是 IDE 通道事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 2265a4a6-4377-4aa9-926a-def6e8eda998
title: SystemConfig_IDEChannel 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IDEChannel
- SystemConfig_IDEChannel.TargetId
- SystemConfig_IDEChannel.DeviceType
- SystemConfig_IDEChannel.DeviceTimingMode
- SystemConfig_IDEChannel.LocationInformationLen
- SystemConfig_IDEChannel.LocationInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60cdfcec8f62e6fb96dcedc895d874f01a209430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511581"
---
# <a name="systemconfig_idechannel-class"></a><span data-ttu-id="c53f8-104">SystemConfig \_ IDEChannel 類別</span><span class="sxs-lookup"><span data-stu-id="c53f8-104">SystemConfig\_IDEChannel class</span></span>

<span data-ttu-id="c53f8-105">這個類別是 IDE 通道事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="c53f8-105">This class is the event type class for IDE channel events.</span></span>

<span data-ttu-id="c53f8-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="c53f8-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c53f8-107">語法</span><span class="sxs-lookup"><span data-stu-id="c53f8-107">Syntax</span></span>

``` syntax
[EventType(23), EventTypeName("IDEChannel")]
class SystemConfig_IDEChannel : SystemConfig
{
  uint32 TargetId;
  uint32 DeviceType;
  uint32 DeviceTimingMode;
  uint32 LocationInformationLen;
  string LocationInformation;
};
```

## <a name="members"></a><span data-ttu-id="c53f8-108">成員</span><span class="sxs-lookup"><span data-stu-id="c53f8-108">Members</span></span>

<span data-ttu-id="c53f8-109">**SystemConfig \_ IDEChannel** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c53f8-109">The **SystemConfig\_IDEChannel** class has these types of members:</span></span>

-   [<span data-ttu-id="c53f8-110">屬性</span><span class="sxs-lookup"><span data-stu-id="c53f8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c53f8-111">屬性</span><span class="sxs-lookup"><span data-stu-id="c53f8-111">Properties</span></span>

<span data-ttu-id="c53f8-112">**SystemConfig \_ IDEChannel** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c53f8-112">The **SystemConfig\_IDEChannel** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c53f8-113">**DeviceTimingMode**</span><span class="sxs-lookup"><span data-stu-id="c53f8-113">**DeviceTimingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c53f8-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c53f8-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c53f8-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c53f8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c53f8-116">限定詞： WmiDataId (3) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="c53f8-116">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="c53f8-117">IDE 可以運作的模式。</span><span class="sxs-lookup"><span data-stu-id="c53f8-117">The mode in which the IDE could function.</span></span> <span data-ttu-id="c53f8-118">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="c53f8-118">The following are the possible values:</span></span>

-   <span data-ttu-id="c53f8-119">PIO \_ MODE0 (0x1) </span><span class="sxs-lookup"><span data-stu-id="c53f8-119">PIO\_MODE0 (0x1)</span></span>
-   <span data-ttu-id="c53f8-120">PIO \_ 模式 1 (0x2) </span><span class="sxs-lookup"><span data-stu-id="c53f8-120">PIO\_MODE1 (0x2)</span></span>
-   <span data-ttu-id="c53f8-121">PIO \_ MODE2 (0x4) </span><span class="sxs-lookup"><span data-stu-id="c53f8-121">PIO\_MODE2 (0x4)</span></span>
-   <span data-ttu-id="c53f8-122">PIO \_ MODE3 (0x8) </span><span class="sxs-lookup"><span data-stu-id="c53f8-122">PIO\_MODE3 (0x8)</span></span>
-   <span data-ttu-id="c53f8-123">PIO \_ MODE4 (0x10) </span><span class="sxs-lookup"><span data-stu-id="c53f8-123">PIO\_MODE4 (0x10)</span></span>
-   <span data-ttu-id="c53f8-124">SWDMA \_ MODE0 (0x20) </span><span class="sxs-lookup"><span data-stu-id="c53f8-124">SWDMA\_MODE0 (0x20)</span></span>
-   <span data-ttu-id="c53f8-125">SWDMA \_ 模式 1 (0x40) </span><span class="sxs-lookup"><span data-stu-id="c53f8-125">SWDMA\_MODE1 (0x40)</span></span>
-   <span data-ttu-id="c53f8-126">SWDMA \_ MODE2 (0x80) </span><span class="sxs-lookup"><span data-stu-id="c53f8-126">SWDMA\_MODE2 (0x80)</span></span>
-   <span data-ttu-id="c53f8-127">MWDMA \_ MODE0 (0x100) </span><span class="sxs-lookup"><span data-stu-id="c53f8-127">MWDMA\_MODE0 (0x100)</span></span>
-   <span data-ttu-id="c53f8-128">MWDMA \_ MODE2 (0x200) </span><span class="sxs-lookup"><span data-stu-id="c53f8-128">MWDMA\_MODE2 (0x200)</span></span>
-   <span data-ttu-id="c53f8-129">MWDMA \_ MODE3 (0x400) </span><span class="sxs-lookup"><span data-stu-id="c53f8-129">MWDMA\_MODE3 (0x400)</span></span>
-   <span data-ttu-id="c53f8-130">UDMA \_ MODE0 (0x800) </span><span class="sxs-lookup"><span data-stu-id="c53f8-130">UDMA\_MODE0 (0x800)</span></span>
-   <span data-ttu-id="c53f8-131">UDMA \_ 模式 1 (0x1000) </span><span class="sxs-lookup"><span data-stu-id="c53f8-131">UDMA\_MODE1 (0x1000)</span></span>
-   <span data-ttu-id="c53f8-132">UDMA \_ MODE2 (0x2000) </span><span class="sxs-lookup"><span data-stu-id="c53f8-132">UDMA\_MODE2 (0x2000)</span></span>
-   <span data-ttu-id="c53f8-133">UDMA \_ MODE3 (0x4000) </span><span class="sxs-lookup"><span data-stu-id="c53f8-133">UDMA\_MODE3 (0x4000)</span></span>
-   <span data-ttu-id="c53f8-134">UDMA \_ MODE4 (0x8000) </span><span class="sxs-lookup"><span data-stu-id="c53f8-134">UDMA\_MODE4 (0x8000)</span></span>
-   <span data-ttu-id="c53f8-135">UDMA \_ MODE5 (0x10000) </span><span class="sxs-lookup"><span data-stu-id="c53f8-135">UDMA\_MODE5 (0x10000)</span></span>

</dd> <dt>

<span data-ttu-id="c53f8-136">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="c53f8-136">**DeviceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c53f8-137">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c53f8-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c53f8-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c53f8-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c53f8-139">限定詞： WmiDataId (2) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="c53f8-139">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="c53f8-140">裝置類型。</span><span class="sxs-lookup"><span data-stu-id="c53f8-140">The device type.</span></span> <span data-ttu-id="c53f8-141">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="c53f8-141">The following are the possible values:</span></span>

-   <span data-ttu-id="c53f8-142">ATA (1) </span><span class="sxs-lookup"><span data-stu-id="c53f8-142">ATA (1)</span></span>
-   <span data-ttu-id="c53f8-143">ATAPI (2) </span><span class="sxs-lookup"><span data-stu-id="c53f8-143">ATAPI (2)</span></span>

</dd> <dt>

<span data-ttu-id="c53f8-144">**LocationInformation**</span><span class="sxs-lookup"><span data-stu-id="c53f8-144">**LocationInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c53f8-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c53f8-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c53f8-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c53f8-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c53f8-147">限定詞： WmiDataId (5) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="c53f8-147">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="c53f8-148">IDE 通道 (例如，主要通道、次要通道等) 。</span><span class="sxs-lookup"><span data-stu-id="c53f8-148">The IDE channel (for example, Primary Channel, Secondary Channel, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="c53f8-149">**LocationInformationLen**</span><span class="sxs-lookup"><span data-stu-id="c53f8-149">**LocationInformationLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c53f8-150">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c53f8-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c53f8-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c53f8-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c53f8-152">限定詞： WmiDataId (4) </span><span class="sxs-lookup"><span data-stu-id="c53f8-152">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="c53f8-153">**LocationInformation** 字串的長度。</span><span class="sxs-lookup"><span data-stu-id="c53f8-153">Length of the **LocationInformation** string.</span></span>

</dd> <dt>

<span data-ttu-id="c53f8-154">**TargetId**</span><span class="sxs-lookup"><span data-stu-id="c53f8-154">**TargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c53f8-155">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c53f8-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c53f8-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c53f8-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c53f8-157">限定詞： WmiDataId (1) </span><span class="sxs-lookup"><span data-stu-id="c53f8-157">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="c53f8-158">磁片的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c53f8-158">The identifier of the disk.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c53f8-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="c53f8-159">Requirements</span></span>



| <span data-ttu-id="c53f8-160">需求</span><span class="sxs-lookup"><span data-stu-id="c53f8-160">Requirement</span></span> | <span data-ttu-id="c53f8-161">值</span><span class="sxs-lookup"><span data-stu-id="c53f8-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c53f8-162">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c53f8-162">Minimum supported client</span></span><br/> | <span data-ttu-id="c53f8-163">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c53f8-163">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c53f8-164">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c53f8-164">Minimum supported server</span></span><br/> | <span data-ttu-id="c53f8-165">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c53f8-165">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c53f8-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c53f8-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c53f8-167">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="c53f8-167">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




