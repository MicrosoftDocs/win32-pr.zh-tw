---
description: 這個類別是插斷服務常式的事件種類類別， (ISR) 事件。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 2c7ccace-3384-43f4-905e-e7eeeee6f87b
title: ISR 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISR
- ISR.InitialTime
- ISR.Routine
- ISR.ReturnValue
- ISR.Vector
- ISR.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5e27d5aa2712f8493b80ea11884aae1d0ef7abee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973309"
---
# <a name="isr-class"></a><span data-ttu-id="1eec6-104">ISR 類別</span><span class="sxs-lookup"><span data-stu-id="1eec6-104">ISR class</span></span>

<span data-ttu-id="1eec6-105">這個類別是插斷服務常式的事件種類類別， (ISR) 事件。</span><span class="sxs-lookup"><span data-stu-id="1eec6-105">This class is the event type class for interrupt service routine (ISR) events.</span></span>

<span data-ttu-id="1eec6-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="1eec6-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eec6-107">語法</span><span class="sxs-lookup"><span data-stu-id="1eec6-107">Syntax</span></span>

``` syntax
[EventType{67}, EventTypeName{"ISR"}]
class ISR : PerfInfo
{
  object InitialTime;
  uint32 Routine;
  uint8  ReturnValue;
  uint8  Vector;
  uint16 Reserved;
};
```

## <a name="members"></a><span data-ttu-id="1eec6-108">成員</span><span class="sxs-lookup"><span data-stu-id="1eec6-108">Members</span></span>

<span data-ttu-id="1eec6-109">**ISR** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1eec6-109">The **ISR** class has these types of members:</span></span>

-   [<span data-ttu-id="1eec6-110">屬性</span><span class="sxs-lookup"><span data-stu-id="1eec6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1eec6-111">屬性</span><span class="sxs-lookup"><span data-stu-id="1eec6-111">Properties</span></span>

<span data-ttu-id="1eec6-112">**ISR** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1eec6-112">The **ISR** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1eec6-113">**InitialTime**</span><span class="sxs-lookup"><span data-stu-id="1eec6-113">**InitialTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eec6-114">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="1eec6-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="1eec6-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1eec6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eec6-116">限定詞： WmiDataId (1) ，副檔名 ( "WmiTime" ) </span><span class="sxs-lookup"><span data-stu-id="1eec6-116">Qualifiers: WmiDataId(1), Extension("WmiTime")</span></span>
</dt> </dl>

<span data-ttu-id="1eec6-117">ISR 進入時間。</span><span class="sxs-lookup"><span data-stu-id="1eec6-117">ISR entry time.</span></span>

</dd> <dt>

<span data-ttu-id="1eec6-118">**已保留**</span><span class="sxs-lookup"><span data-stu-id="1eec6-118">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eec6-119">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1eec6-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1eec6-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1eec6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eec6-121">限定詞： WmiDataId (5) ，指標</span><span class="sxs-lookup"><span data-stu-id="1eec6-121">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1eec6-122">保留的。</span><span class="sxs-lookup"><span data-stu-id="1eec6-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="1eec6-123">**ReturnValue**</span><span class="sxs-lookup"><span data-stu-id="1eec6-123">**ReturnValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eec6-124">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="1eec6-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1eec6-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1eec6-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eec6-126">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="1eec6-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="1eec6-127">布林值，指出是否已宣告中斷 (如果已宣告中斷) ，則為 True。</span><span class="sxs-lookup"><span data-stu-id="1eec6-127">Boolean indicating if the interrupt was claimed (is True if the interrupt was claimed).</span></span>

</dd> <dt>

<span data-ttu-id="1eec6-128">**常規**</span><span class="sxs-lookup"><span data-stu-id="1eec6-128">**Routine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eec6-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1eec6-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eec6-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1eec6-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eec6-131">限定詞： WmiDataId (2) ，指標</span><span class="sxs-lookup"><span data-stu-id="1eec6-131">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1eec6-132">ISR 常式的位址。</span><span class="sxs-lookup"><span data-stu-id="1eec6-132">Address of ISR routine.</span></span> <span data-ttu-id="1eec6-133">使用具有影像事件的位址，以找出已啟動的映射。</span><span class="sxs-lookup"><span data-stu-id="1eec6-133">Use the address with the Image events to find which image started.</span></span>

</dd> <dt>

<span data-ttu-id="1eec6-134">**向量**</span><span class="sxs-lookup"><span data-stu-id="1eec6-134">**Vector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eec6-135">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="1eec6-135">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1eec6-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1eec6-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eec6-137">限定詞： WmiDataId (4) </span><span class="sxs-lookup"><span data-stu-id="1eec6-137">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="1eec6-138">從中斷描述中繼資料表中指派了 ISR 常式的向量。</span><span class="sxs-lookup"><span data-stu-id="1eec6-138">Vector from interrupt descriptor table to which ISR routine is assigned.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1eec6-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="1eec6-139">Requirements</span></span>



| <span data-ttu-id="1eec6-140">需求</span><span class="sxs-lookup"><span data-stu-id="1eec6-140">Requirement</span></span> | <span data-ttu-id="1eec6-141">值</span><span class="sxs-lookup"><span data-stu-id="1eec6-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1eec6-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1eec6-142">Minimum supported client</span></span><br/> | <span data-ttu-id="1eec6-143">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1eec6-143">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1eec6-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1eec6-144">Minimum supported server</span></span><br/> | <span data-ttu-id="1eec6-145">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1eec6-145">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




