---
description: 此類別是事件種類類別，可標示磁片 i/o 讀取、寫入和清除事件的開頭。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 96543ef9-cc2b-4d9a-86a8-f2458439e4d8
title: DiskIo_TypeGroup2 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup2
- DiskIo_TypeGroup2.Irp
- DiskIo_TypeGroup2.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: ea08f32106c935be628bcdcd22e39ab92a0566e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511016"
---
# <a name="diskio_typegroup2-class"></a><span data-ttu-id="65330-104">DiskIo \_ TypeGroup2 類別</span><span class="sxs-lookup"><span data-stu-id="65330-104">DiskIo\_TypeGroup2 class</span></span>

<span data-ttu-id="65330-105">此類別是事件種類類別，可標示磁片 i/o 讀取、寫入和清除事件的開頭。</span><span class="sxs-lookup"><span data-stu-id="65330-105">This class is the event type class that marks the beginning of the disk I/O read, write, and flush events.</span></span>

<span data-ttu-id="65330-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="65330-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="65330-107">語法</span><span class="sxs-lookup"><span data-stu-id="65330-107">Syntax</span></span>

``` syntax
[EventType{12, 13, 15}, EventTypeName{"ReadInit", "WriteInit", "FlushInit"}]
class DiskIo_TypeGroup2 : DiskIo
{
  uint32 Irp;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a><span data-ttu-id="65330-108">成員</span><span class="sxs-lookup"><span data-stu-id="65330-108">Members</span></span>

<span data-ttu-id="65330-109">**DiskIo \_ TypeGroup2** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="65330-109">The **DiskIo\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="65330-110">屬性</span><span class="sxs-lookup"><span data-stu-id="65330-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="65330-111">屬性</span><span class="sxs-lookup"><span data-stu-id="65330-111">Properties</span></span>

<span data-ttu-id="65330-112">**DiskIo \_ TypeGroup2** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="65330-112">The **DiskIo\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="65330-113">**Irp**</span><span class="sxs-lookup"><span data-stu-id="65330-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65330-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="65330-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="65330-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="65330-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65330-116">限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (1) ， [**指標**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="65330-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="65330-117">I/o 要求封包。</span><span class="sxs-lookup"><span data-stu-id="65330-117">I/O request packet.</span></span> <span data-ttu-id="65330-118">這個屬性會識別 IO 活動。</span><span class="sxs-lookup"><span data-stu-id="65330-118">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="65330-119">**IssuingThreadId**</span><span class="sxs-lookup"><span data-stu-id="65330-119">**IssuingThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65330-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="65330-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="65330-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="65330-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65330-122">限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (2) </span><span class="sxs-lookup"><span data-stu-id="65330-122">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="65330-123">發行執行緒的識別碼。</span><span class="sxs-lookup"><span data-stu-id="65330-123">The identifier of the issuing thread.</span></span>

<span data-ttu-id="65330-124">**Windows server 2008 R2、Windows server 2008、windows 7 和 Windows Vista：** 不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="65330-124">**Windows Server 2008 R2, Windows Server 2008, Windows 7 and Windows Vista:** This property is not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65330-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="65330-125">Requirements</span></span>



| <span data-ttu-id="65330-126">需求</span><span class="sxs-lookup"><span data-stu-id="65330-126">Requirement</span></span> | <span data-ttu-id="65330-127">值</span><span class="sxs-lookup"><span data-stu-id="65330-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="65330-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65330-128">Minimum supported client</span></span><br/> | <span data-ttu-id="65330-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65330-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="65330-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65330-130">Minimum supported server</span></span><br/> | <span data-ttu-id="65330-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65330-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="65330-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65330-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65330-133">**DiskIo**</span><span class="sxs-lookup"><span data-stu-id="65330-133">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




