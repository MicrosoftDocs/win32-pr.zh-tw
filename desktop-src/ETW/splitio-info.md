---
description: 這個類別是分割 IO 事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 0eb1f712-8b1c-4de1-b701-5c7dbabb0f55
title: SplitIo_Info 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo_Info
- SplitIo_Info.ParentIrp
- SplitIo_Info.ChildIrp
api_type:
- NA
api_location: ''
ms.openlocfilehash: 469c8f04664f72b88e5a4378cb318b52f32fba24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851864"
---
# <a name="splitio_info-class"></a><span data-ttu-id="46d41-104">SplitIo \_ 資訊類別</span><span class="sxs-lookup"><span data-stu-id="46d41-104">SplitIo\_Info class</span></span>

<span data-ttu-id="46d41-105">這個類別是分割 IO 事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="46d41-105">This class is the event type class for split IO events.</span></span>

<span data-ttu-id="46d41-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="46d41-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="46d41-107">語法</span><span class="sxs-lookup"><span data-stu-id="46d41-107">Syntax</span></span>

``` syntax
[EventType{32}, EventTypeName{"VolMgr"}]
class SplitIo_Info : SplitIo
{
  uint32 ParentIrp;
  uint32 ChildIrp;
};
```

## <a name="members"></a><span data-ttu-id="46d41-108">成員</span><span class="sxs-lookup"><span data-stu-id="46d41-108">Members</span></span>

<span data-ttu-id="46d41-109">**SplitIo \_ Info** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="46d41-109">The **SplitIo\_Info** class has these types of members:</span></span>

-   [<span data-ttu-id="46d41-110">屬性</span><span class="sxs-lookup"><span data-stu-id="46d41-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46d41-111">屬性</span><span class="sxs-lookup"><span data-stu-id="46d41-111">Properties</span></span>

<span data-ttu-id="46d41-112">**SplitIo \_ Info** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="46d41-112">The **SplitIo\_Info** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46d41-113">**ChildIrp**</span><span class="sxs-lookup"><span data-stu-id="46d41-113">**ChildIrp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46d41-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="46d41-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46d41-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46d41-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46d41-116">限定詞： WmiDataId (2) ，指標</span><span class="sxs-lookup"><span data-stu-id="46d41-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="46d41-117">子 IO 要求封包。</span><span class="sxs-lookup"><span data-stu-id="46d41-117">Child IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="46d41-118">**ParentIrp**</span><span class="sxs-lookup"><span data-stu-id="46d41-118">**ParentIrp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46d41-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="46d41-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46d41-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46d41-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46d41-121">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="46d41-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="46d41-122">父 IO 要求封包。</span><span class="sxs-lookup"><span data-stu-id="46d41-122">Parent IO request packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46d41-123">備註</span><span class="sxs-lookup"><span data-stu-id="46d41-123">Remarks</span></span>

<span data-ttu-id="46d41-124">指出磁片區管理員將 IRP 分割成兩個 Irp。</span><span class="sxs-lookup"><span data-stu-id="46d41-124">Indicates that the volume manager split the IRP into two IRPs.</span></span>

## <a name="requirements"></a><span data-ttu-id="46d41-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="46d41-125">Requirements</span></span>



| <span data-ttu-id="46d41-126">需求</span><span class="sxs-lookup"><span data-stu-id="46d41-126">Requirement</span></span> | <span data-ttu-id="46d41-127">值</span><span class="sxs-lookup"><span data-stu-id="46d41-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="46d41-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46d41-128">Minimum supported client</span></span><br/> | <span data-ttu-id="46d41-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46d41-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="46d41-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46d41-130">Minimum supported server</span></span><br/> | <span data-ttu-id="46d41-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46d41-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




