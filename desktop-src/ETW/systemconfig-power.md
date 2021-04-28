---
description: SystemConfig_Power 類別-此類別是電源設定事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 7065b0b0-9a1d-4fce-a494-5762d5efb239
title: SystemConfig_Power 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Power
- SystemConfig_Power.s1
- SystemConfig_Power.s2
- SystemConfig_Power.s3
- SystemConfig_Power.s4
- SystemConfig_Power.s5
- SystemConfig_Power.Pad1
- SystemConfig_Power.Pad2
- SystemConfig_Power.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: d7338faad8c313847ad7db7aaac5d4000abba5be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106066"
---
# <a name="systemconfig_power-class"></a><span data-ttu-id="0b9a9-104">SystemConfig \_ Power 類別</span><span class="sxs-lookup"><span data-stu-id="0b9a9-104">SystemConfig\_Power class</span></span>

<span data-ttu-id="0b9a9-105">此類別是電源設定事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="0b9a9-105">This class is the event type class for power configuration events.</span></span>

<span data-ttu-id="0b9a9-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="0b9a9-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b9a9-107">語法</span><span class="sxs-lookup"><span data-stu-id="0b9a9-107">Syntax</span></span>

``` syntax
[EventType(16), EventTypeName("Power")]
class SystemConfig_Power : SystemConfig
{
  uint8 s1;
  uint8 s2;
  uint8 s3;
  uint8 s4;
  uint8 s5;
  uint8 Pad1;
  uint8 Pad2;
  uint8 Pad3;
};
```

## <a name="members"></a><span data-ttu-id="0b9a9-108">成員</span><span class="sxs-lookup"><span data-stu-id="0b9a9-108">Members</span></span>

<span data-ttu-id="0b9a9-109">**SystemConfig \_ Power** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0b9a9-109">The **SystemConfig\_Power** class has these types of members:</span></span>

-   [<span data-ttu-id="0b9a9-110">屬性</span><span class="sxs-lookup"><span data-stu-id="0b9a9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b9a9-111">屬性</span><span class="sxs-lookup"><span data-stu-id="0b9a9-111">Properties</span></span>

<span data-ttu-id="0b9a9-112">**SystemConfig \_ Power** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0b9a9-112">The **SystemConfig\_Power** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b9a9-113">Pad1</span><span class="sxs-lookup"><span data-stu-id="0b9a9-113">Pad1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b9a9-114">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="0b9a9-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0b9a9-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b9a9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b9a9-116">限定詞： WmiDataId (6) </span><span class="sxs-lookup"><span data-stu-id="0b9a9-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="0b9a9-117">未使用。</span><span class="sxs-lookup"><span data-stu-id="0b9a9-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b9a9-118">Pad2</span><span class="sxs-lookup"><span data-stu-id="0b9a9-118">Pad2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b9a9-119">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="0b9a9-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0b9a9-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b9a9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b9a9-121">限定詞： WmiDataId (7) </span><span class="sxs-lookup"><span data-stu-id="0b9a9-121">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="0b9a9-122">未使用。</span><span class="sxs-lookup"><span data-stu-id="0b9a9-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b9a9-123">Pad3</span><span class="sxs-lookup"><span data-stu-id="0b9a9-123">Pad3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b9a9-124">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="0b9a9-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0b9a9-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b9a9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b9a9-126">限定詞： WmiDataId (8) </span><span class="sxs-lookup"><span data-stu-id="0b9a9-126">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="0b9a9-127">未使用。</span><span class="sxs-lookup"><span data-stu-id="0b9a9-127">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b9a9-128">s1</span><span class="sxs-lookup"><span data-stu-id="0b9a9-128">s1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b9a9-129">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="0b9a9-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0b9a9-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b9a9-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b9a9-131">限定詞： WmiDataId (1) </span><span class="sxs-lookup"><span data-stu-id="0b9a9-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="0b9a9-132">True 表示系統支援睡眠狀態 S1。</span><span class="sxs-lookup"><span data-stu-id="0b9a9-132">True indicates the system supports sleep state S1.</span></span>

</dd> <dt>

<span data-ttu-id="0b9a9-133">s2</span><span class="sxs-lookup"><span data-stu-id="0b9a9-133">s2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b9a9-134">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="0b9a9-134">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0b9a9-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b9a9-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b9a9-136">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="0b9a9-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="0b9a9-137">True 表示系統支援睡眠狀態 S2。</span><span class="sxs-lookup"><span data-stu-id="0b9a9-137">True indicates the system supports sleep state S2.</span></span>

</dd> <dt>

<span data-ttu-id="0b9a9-138">s3</span><span class="sxs-lookup"><span data-stu-id="0b9a9-138">s3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b9a9-139">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="0b9a9-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0b9a9-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b9a9-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b9a9-141">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="0b9a9-141">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="0b9a9-142">True 表示系統支援睡眠狀態 S3。</span><span class="sxs-lookup"><span data-stu-id="0b9a9-142">True indicates the system supports sleep state S3.</span></span>

</dd> <dt>

<span data-ttu-id="0b9a9-143">s4</span><span class="sxs-lookup"><span data-stu-id="0b9a9-143">s4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b9a9-144">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="0b9a9-144">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0b9a9-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b9a9-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b9a9-146">限定詞： WmiDataId (4) </span><span class="sxs-lookup"><span data-stu-id="0b9a9-146">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="0b9a9-147">True 表示系統支援睡眠狀態 S4。</span><span class="sxs-lookup"><span data-stu-id="0b9a9-147">True indicates the system supports sleep state S4.</span></span>

</dd> <dt>

<span data-ttu-id="0b9a9-148">s5</span><span class="sxs-lookup"><span data-stu-id="0b9a9-148">s5</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b9a9-149">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="0b9a9-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0b9a9-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b9a9-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b9a9-151">限定詞： WmiDataId (5) </span><span class="sxs-lookup"><span data-stu-id="0b9a9-151">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="0b9a9-152">True 表示系統支援睡眠狀態 S5。</span><span class="sxs-lookup"><span data-stu-id="0b9a9-152">True indicates the system supports sleep state S5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b9a9-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b9a9-153">Requirements</span></span>



| <span data-ttu-id="0b9a9-154">需求</span><span class="sxs-lookup"><span data-stu-id="0b9a9-154">Requirement</span></span> | <span data-ttu-id="0b9a9-155">值</span><span class="sxs-lookup"><span data-stu-id="0b9a9-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0b9a9-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b9a9-156">Minimum supported client</span></span><br/> | <span data-ttu-id="0b9a9-157">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b9a9-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0b9a9-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b9a9-158">Minimum supported server</span></span><br/> | <span data-ttu-id="0b9a9-159">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b9a9-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0b9a9-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b9a9-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b9a9-161">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="0b9a9-161">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




