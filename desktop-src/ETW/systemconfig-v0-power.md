---
description: 此類別是電源設定事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: b3391435-dac0-4c48-b788-eb4d4a7aa635
title: SystemConfig_V0_Power 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Power
- SystemConfig_V0_Power.s1
- SystemConfig_V0_Power.s2
- SystemConfig_V0_Power.s3
- SystemConfig_V0_Power.s4
- SystemConfig_V0_Power.s5
- SystemConfig_V0_Power.Pad1
- SystemConfig_V0_Power.Pad2
- SystemConfig_V0_Power.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2e42af68ad12857d65d776b7a73794d2d13b2b48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972105"
---
# <a name="systemconfig_v0_power-class"></a><span data-ttu-id="2bbf0-104">SystemConfig \_ V0 \_ Power 類別</span><span class="sxs-lookup"><span data-stu-id="2bbf0-104">SystemConfig\_V0\_Power class</span></span>

<span data-ttu-id="2bbf0-105">此類別是電源設定事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-105">This class is the event type class for power configuration events.</span></span>

<span data-ttu-id="2bbf0-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bbf0-107">語法</span><span class="sxs-lookup"><span data-stu-id="2bbf0-107">Syntax</span></span>

``` syntax
[EventType(16), EventTypeName("Power")]
class SystemConfig_V0_Power : SystemConfig_V0
{
  boolean s1;
  boolean s2;
  boolean s3;
  boolean s4;
  boolean s5;
  uint8   Pad1;
  uint8   Pad2;
  uint8   Pad3;
};
```

## <a name="members"></a><span data-ttu-id="2bbf0-108">成員</span><span class="sxs-lookup"><span data-stu-id="2bbf0-108">Members</span></span>

<span data-ttu-id="2bbf0-109">**SystemConfig \_ V0 \_ Power** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2bbf0-109">The **SystemConfig\_V0\_Power** class has these types of members:</span></span>

-   [<span data-ttu-id="2bbf0-110">屬性</span><span class="sxs-lookup"><span data-stu-id="2bbf0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2bbf0-111">屬性</span><span class="sxs-lookup"><span data-stu-id="2bbf0-111">Properties</span></span>

<span data-ttu-id="2bbf0-112">**SystemConfig \_ V0 \_ Power** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-112">The **SystemConfig\_V0\_Power** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2bbf0-113">Pad1</span><span class="sxs-lookup"><span data-stu-id="2bbf0-113">Pad1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bbf0-114">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="2bbf0-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2bbf0-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2bbf0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bbf0-116">限定詞： WmiDataId (6) </span><span class="sxs-lookup"><span data-stu-id="2bbf0-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="2bbf0-117">保留的。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="2bbf0-118">Pad2</span><span class="sxs-lookup"><span data-stu-id="2bbf0-118">Pad2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bbf0-119">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="2bbf0-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2bbf0-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2bbf0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bbf0-121">限定詞： WmiDataId (7) </span><span class="sxs-lookup"><span data-stu-id="2bbf0-121">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="2bbf0-122">保留的。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="2bbf0-123">Pad3</span><span class="sxs-lookup"><span data-stu-id="2bbf0-123">Pad3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bbf0-124">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="2bbf0-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2bbf0-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2bbf0-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bbf0-126">限定詞： WmiDataId (8) </span><span class="sxs-lookup"><span data-stu-id="2bbf0-126">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="2bbf0-127">保留的。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-127">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="2bbf0-128">s1</span><span class="sxs-lookup"><span data-stu-id="2bbf0-128">s1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bbf0-129">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2bbf0-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2bbf0-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2bbf0-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bbf0-131">限定詞： WmiDataId (1) </span><span class="sxs-lookup"><span data-stu-id="2bbf0-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="2bbf0-132">True 表示系統支援睡眠狀態 S1。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-132">True indicates the system supports sleep state S1.</span></span>

</dd> <dt>

<span data-ttu-id="2bbf0-133">s2</span><span class="sxs-lookup"><span data-stu-id="2bbf0-133">s2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bbf0-134">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2bbf0-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2bbf0-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2bbf0-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bbf0-136">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="2bbf0-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="2bbf0-137">True 表示系統支援睡眠狀態 S2。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-137">True indicates the system supports sleep state S2.</span></span>

</dd> <dt>

<span data-ttu-id="2bbf0-138">s3</span><span class="sxs-lookup"><span data-stu-id="2bbf0-138">s3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bbf0-139">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2bbf0-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2bbf0-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2bbf0-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bbf0-141">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="2bbf0-141">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="2bbf0-142">True 表示系統支援睡眠狀態 S3。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-142">True indicates the system supports sleep state S3.</span></span>

</dd> <dt>

<span data-ttu-id="2bbf0-143">s4</span><span class="sxs-lookup"><span data-stu-id="2bbf0-143">s4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bbf0-144">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2bbf0-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2bbf0-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2bbf0-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bbf0-146">限定詞： WmiDataId (4) </span><span class="sxs-lookup"><span data-stu-id="2bbf0-146">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="2bbf0-147">True 表示系統支援睡眠狀態 S4。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-147">True indicates the system supports sleep state S4.</span></span>

</dd> <dt>

<span data-ttu-id="2bbf0-148">s5</span><span class="sxs-lookup"><span data-stu-id="2bbf0-148">s5</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bbf0-149">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2bbf0-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2bbf0-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2bbf0-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bbf0-151">限定詞： WmiDataId (5) </span><span class="sxs-lookup"><span data-stu-id="2bbf0-151">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="2bbf0-152">True 表示系統支援睡眠狀態 S5。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-152">True indicates the system supports sleep state S5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2bbf0-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="2bbf0-153">Requirements</span></span>



| <span data-ttu-id="2bbf0-154">需求</span><span class="sxs-lookup"><span data-stu-id="2bbf0-154">Requirement</span></span> | <span data-ttu-id="2bbf0-155">值</span><span class="sxs-lookup"><span data-stu-id="2bbf0-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2bbf0-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2bbf0-156">Minimum supported client</span></span><br/> | <span data-ttu-id="2bbf0-157">都不支援</span><span class="sxs-lookup"><span data-stu-id="2bbf0-157">None supported</span></span><br/>                            |
| <span data-ttu-id="2bbf0-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2bbf0-158">Minimum supported server</span></span><br/> | <span data-ttu-id="2bbf0-159">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2bbf0-159">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2bbf0-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2bbf0-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bbf0-161">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="2bbf0-161">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




