---
description: HWConfig \_ LogDisk 類別是邏輯磁片設定事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 2b7038fa-2f20-4bb5-bac1-76b272b3421c
title: HWConfig_LogDisk 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_LogDisk
- HWConfig_LogDisk.DiskNumber
- HWConfig_LogDisk.Pad
- HWConfig_LogDisk.StartOffset
- HWConfig_LogDisk.PartitionSize
api_type:
- NA
api_location: ''
ms.openlocfilehash: dce4faed913d01f76ff23177b2dad42ea74e5c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513917"
---
# <a name="hwconfig_logdisk-class"></a><span data-ttu-id="b015e-104">HWConfig \_ LogDisk 類別</span><span class="sxs-lookup"><span data-stu-id="b015e-104">HWConfig\_LogDisk class</span></span>

<span data-ttu-id="b015e-105">**HWConfig \_ LogDisk** 類別是邏輯磁片設定事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="b015e-105">The **HWConfig\_LogDisk** class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="b015e-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="b015e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b015e-107">語法</span><span class="sxs-lookup"><span data-stu-id="b015e-107">Syntax</span></span>

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class HWConfig_LogDisk : HWConfig
{
  uint32 DiskNumber;
  uint32 Pad;
  uint64 StartOffset;
  uint64 PartitionSize;
};
```

## <a name="members"></a><span data-ttu-id="b015e-108">成員</span><span class="sxs-lookup"><span data-stu-id="b015e-108">Members</span></span>

<span data-ttu-id="b015e-109">**HWConfig \_ LogDisk** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b015e-109">The **HWConfig\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="b015e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b015e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b015e-111">屬性</span><span class="sxs-lookup"><span data-stu-id="b015e-111">Properties</span></span>

<span data-ttu-id="b015e-112">**HWConfig \_ LogDisk** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b015e-112">The **HWConfig\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b015e-113">DiskNumber</span><span class="sxs-lookup"><span data-stu-id="b015e-113">DiskNumber</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b015e-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b015e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b015e-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b015e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b015e-116">限定詞： WmiDataId (1) </span><span class="sxs-lookup"><span data-stu-id="b015e-116">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="b015e-117">包含此分割區之磁片的索引編號。</span><span class="sxs-lookup"><span data-stu-id="b015e-117">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="b015e-118">Pad</span><span class="sxs-lookup"><span data-stu-id="b015e-118">Pad</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b015e-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b015e-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b015e-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b015e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b015e-121">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="b015e-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="b015e-122">保留的。</span><span class="sxs-lookup"><span data-stu-id="b015e-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="b015e-123">PartitionSize</span><span class="sxs-lookup"><span data-stu-id="b015e-123">PartitionSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b015e-124">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b015e-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b015e-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b015e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b015e-126">限定詞： WmiDataId (4) </span><span class="sxs-lookup"><span data-stu-id="b015e-126">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="b015e-127">分割區的總大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b015e-127">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b015e-128">Startoffset 位置</span><span class="sxs-lookup"><span data-stu-id="b015e-128">StartOffset</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b015e-129">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b015e-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b015e-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b015e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b015e-131">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="b015e-131">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="b015e-132">從磁片開頭開始，資料分割的位移 (位元組) 。</span><span class="sxs-lookup"><span data-stu-id="b015e-132">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b015e-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="b015e-133">Requirements</span></span>



| <span data-ttu-id="b015e-134">需求</span><span class="sxs-lookup"><span data-stu-id="b015e-134">Requirement</span></span> | <span data-ttu-id="b015e-135">值</span><span class="sxs-lookup"><span data-stu-id="b015e-135">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="b015e-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b015e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b015e-137">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b015e-137">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b015e-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b015e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b015e-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="b015e-139">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="b015e-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b015e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b015e-141">**HWConfig**</span><span class="sxs-lookup"><span data-stu-id="b015e-141">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




