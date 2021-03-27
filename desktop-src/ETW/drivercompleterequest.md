---
description: 此類別是驅動程式完成要求事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: c9c9be05-c1c6-4d77-a47a-44a61ebfcdc7
title: DriverCompleteRequest 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompleteRequest
- DriverCompleteRequest.RoutineAddr
- DriverCompleteRequest.Irp
- DriverCompleteRequest.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 57cf49d0e37dc870c0eb46c31ef39e0d81689811
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971948"
---
# <a name="drivercompleterequest-class"></a><span data-ttu-id="ff3fd-104">DriverCompleteRequest 類別</span><span class="sxs-lookup"><span data-stu-id="ff3fd-104">DriverCompleteRequest class</span></span>

<span data-ttu-id="ff3fd-105">此類別是驅動程式完成要求事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="ff3fd-105">This class is the event type class for driver complete request events.</span></span>

<span data-ttu-id="ff3fd-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="ff3fd-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff3fd-107">語法</span><span class="sxs-lookup"><span data-stu-id="ff3fd-107">Syntax</span></span>

``` syntax
[EventType{52}, EventTypeName{"DrvComplReq"}]
class DriverCompleteRequest : DiskIo
{
  uint32 RoutineAddr;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="ff3fd-108">成員</span><span class="sxs-lookup"><span data-stu-id="ff3fd-108">Members</span></span>

<span data-ttu-id="ff3fd-109">**DriverCompleteRequest** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ff3fd-109">The **DriverCompleteRequest** class has these types of members:</span></span>

-   [<span data-ttu-id="ff3fd-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ff3fd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ff3fd-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ff3fd-111">Properties</span></span>

<span data-ttu-id="ff3fd-112">**DriverCompleteRequest** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ff3fd-112">The **DriverCompleteRequest** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ff3fd-113">**Irp**</span><span class="sxs-lookup"><span data-stu-id="ff3fd-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff3fd-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ff3fd-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ff3fd-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ff3fd-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff3fd-116">限定詞： WmiDataId (2) ，指標</span><span class="sxs-lookup"><span data-stu-id="ff3fd-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="ff3fd-117">IO 要求封包。</span><span class="sxs-lookup"><span data-stu-id="ff3fd-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="ff3fd-118">**RoutineAddr**</span><span class="sxs-lookup"><span data-stu-id="ff3fd-118">**RoutineAddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff3fd-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ff3fd-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ff3fd-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ff3fd-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff3fd-121">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="ff3fd-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="ff3fd-122">要呼叫的驅動程式函式的位址。</span><span class="sxs-lookup"><span data-stu-id="ff3fd-122">Address of the driver function being called.</span></span>

</dd> <dt>

<span data-ttu-id="ff3fd-123">**UniqMatchId**</span><span class="sxs-lookup"><span data-stu-id="ff3fd-123">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff3fd-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ff3fd-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ff3fd-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ff3fd-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff3fd-126">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="ff3fd-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="ff3fd-127">可唯一識別要求的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ff3fd-127">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="ff3fd-128">您可以使用這個識別碼，將其他驅動程式事件相互關聯，例如 [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="ff3fd-128">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff3fd-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff3fd-129">Requirements</span></span>



| <span data-ttu-id="ff3fd-130">需求</span><span class="sxs-lookup"><span data-stu-id="ff3fd-130">Requirement</span></span> | <span data-ttu-id="ff3fd-131">值</span><span class="sxs-lookup"><span data-stu-id="ff3fd-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ff3fd-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff3fd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ff3fd-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff3fd-133">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ff3fd-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff3fd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ff3fd-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff3fd-135">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ff3fd-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff3fd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff3fd-137">**DiskIo**</span><span class="sxs-lookup"><span data-stu-id="ff3fd-137">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




