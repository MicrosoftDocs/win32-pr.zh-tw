---
description: 此類別是中斷要求 (IRQ) 事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 9d4692e8-f19f-478c-a003-396722e426c3
title: SystemConfig_IRQ 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IRQ
- SystemConfig_IRQ.IRQAffinity
- SystemConfig_IRQ.IRQNum
- SystemConfig_IRQ.DeviceDescriptionLen
- SystemConfig_IRQ.DeviceDescription
api_type:
- NA
api_location: ''
ms.openlocfilehash: e1dd674c34c06259bc343615c17d165be3f57d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972168"
---
# <a name="systemconfig_irq-class"></a><span data-ttu-id="6c9a2-104">SystemConfig \_ IRQ 類別</span><span class="sxs-lookup"><span data-stu-id="6c9a2-104">SystemConfig\_IRQ class</span></span>

<span data-ttu-id="6c9a2-105">此類別是中斷要求 (IRQ) 事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="6c9a2-105">This class is the event type class for interrupt request (IRQ) events.</span></span>

<span data-ttu-id="6c9a2-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="6c9a2-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c9a2-107">語法</span><span class="sxs-lookup"><span data-stu-id="6c9a2-107">Syntax</span></span>

``` syntax
[EventType(21), EventTypeName("IRQ")]
class SystemConfig_IRQ : SystemConfig
{
  uint64 IRQAffinity;
  uint32 IRQNum;
  uint32 DeviceDescriptionLen;
  string DeviceDescription;
};
```

## <a name="members"></a><span data-ttu-id="6c9a2-108">成員</span><span class="sxs-lookup"><span data-stu-id="6c9a2-108">Members</span></span>

<span data-ttu-id="6c9a2-109">**SystemConfig \_ IRQ** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6c9a2-109">The **SystemConfig\_IRQ** class has these types of members:</span></span>

-   [<span data-ttu-id="6c9a2-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6c9a2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c9a2-111">屬性</span><span class="sxs-lookup"><span data-stu-id="6c9a2-111">Properties</span></span>

<span data-ttu-id="6c9a2-112">**SystemConfig \_ IRQ** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6c9a2-112">The **SystemConfig\_IRQ** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c9a2-113">**DeviceDescription**</span><span class="sxs-lookup"><span data-stu-id="6c9a2-113">**DeviceDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c9a2-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6c9a2-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c9a2-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c9a2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c9a2-116">限定詞： WmiDataId (4) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="6c9a2-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="6c9a2-117">提出要求之裝置或軟體的描述。</span><span class="sxs-lookup"><span data-stu-id="6c9a2-117">Description of the device or software making the request.</span></span>

</dd> <dt>

<span data-ttu-id="6c9a2-118">**DeviceDescriptionLen**</span><span class="sxs-lookup"><span data-stu-id="6c9a2-118">**DeviceDescriptionLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c9a2-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6c9a2-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c9a2-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c9a2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c9a2-121">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="6c9a2-121">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="6c9a2-122">**DeviceDescription** 中字串的長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="6c9a2-122">Length, in characters, of the string in **DeviceDescription**.</span></span>

</dd> <dt>

<span data-ttu-id="6c9a2-123">**IRQAffinity**</span><span class="sxs-lookup"><span data-stu-id="6c9a2-123">**IRQAffinity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c9a2-124">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="6c9a2-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6c9a2-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c9a2-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c9a2-126">限定詞： WmiDataId (1) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="6c9a2-126">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="6c9a2-127">IRQ 親和性遮罩。</span><span class="sxs-lookup"><span data-stu-id="6c9a2-127">IRQ affinity mask.</span></span> <span data-ttu-id="6c9a2-128">相似性遮罩會識別可以接收 IRQ (或處理器群組) 的特定處理器。</span><span class="sxs-lookup"><span data-stu-id="6c9a2-128">The affinity mask identifies the specific processors (or groups of processors) that can receive the IRQ.</span></span>

</dd> <dt>

<span data-ttu-id="6c9a2-129">**IRQNum**</span><span class="sxs-lookup"><span data-stu-id="6c9a2-129">**IRQNum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c9a2-130">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6c9a2-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c9a2-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c9a2-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c9a2-132">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="6c9a2-132">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="6c9a2-133">中斷要求行號。</span><span class="sxs-lookup"><span data-stu-id="6c9a2-133">Interrupt request line number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c9a2-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c9a2-134">Requirements</span></span>



| <span data-ttu-id="6c9a2-135">需求</span><span class="sxs-lookup"><span data-stu-id="6c9a2-135">Requirement</span></span> | <span data-ttu-id="6c9a2-136">值</span><span class="sxs-lookup"><span data-stu-id="6c9a2-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6c9a2-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c9a2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6c9a2-138">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c9a2-138">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6c9a2-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c9a2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6c9a2-140">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c9a2-140">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c9a2-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c9a2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c9a2-142">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="6c9a2-142">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




