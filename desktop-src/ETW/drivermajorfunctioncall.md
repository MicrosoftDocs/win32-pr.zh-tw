---
description: 這個類別是驅動程式主要函式呼叫事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 8c913145-ac50-4d40-8519-5fed79d977ba
title: DriverMajorFunctionCall 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverMajorFunctionCall
- DriverMajorFunctionCall.MajorFunction
- DriverMajorFunctionCall.MinorFunction
- DriverMajorFunctionCall.RoutineAddr
- DriverMajorFunctionCall.FileObject
- DriverMajorFunctionCall.Irp
- DriverMajorFunctionCall.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: c944b11c9019ba5244850f035bfc7c02d5ca3350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971944"
---
# <a name="drivermajorfunctioncall-class"></a><span data-ttu-id="fb348-104">DriverMajorFunctionCall 類別</span><span class="sxs-lookup"><span data-stu-id="fb348-104">DriverMajorFunctionCall class</span></span>

<span data-ttu-id="fb348-105">這個類別是驅動程式主要函式呼叫事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="fb348-105">This class is the event type class for driver major function call events.</span></span>

<span data-ttu-id="fb348-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="fb348-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb348-107">語法</span><span class="sxs-lookup"><span data-stu-id="fb348-107">Syntax</span></span>

``` syntax
[EventType{34}, EventTypeName{"DrvMjFnCall"}]
class DriverMajorFunctionCall : DiskIo
{
  uint32 MajorFunction;
  uint32 MinorFunction;
  uint32 RoutineAddr;
  uint32 FileObject;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="fb348-108">成員</span><span class="sxs-lookup"><span data-stu-id="fb348-108">Members</span></span>

<span data-ttu-id="fb348-109">**DriverMajorFunctionCall** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fb348-109">The **DriverMajorFunctionCall** class has these types of members:</span></span>

-   [<span data-ttu-id="fb348-110">屬性</span><span class="sxs-lookup"><span data-stu-id="fb348-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb348-111">屬性</span><span class="sxs-lookup"><span data-stu-id="fb348-111">Properties</span></span>

<span data-ttu-id="fb348-112">**DriverMajorFunctionCall** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fb348-112">The **DriverMajorFunctionCall** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fb348-113">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="fb348-113">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb348-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fb348-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fb348-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fb348-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb348-116">限定詞： WmiDataId (4) ，指標</span><span class="sxs-lookup"><span data-stu-id="fb348-116">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="fb348-117">將 this 指標的值符合 [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md)事件中的 **FileObject** 指標值，以判斷 i/o 作業的類型。</span><span class="sxs-lookup"><span data-stu-id="fb348-117">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> <dt>

<span data-ttu-id="fb348-118">**Irp**</span><span class="sxs-lookup"><span data-stu-id="fb348-118">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb348-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fb348-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fb348-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fb348-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb348-121">限定詞： WmiDataId (5) ，指標</span><span class="sxs-lookup"><span data-stu-id="fb348-121">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="fb348-122">IO 要求封包。</span><span class="sxs-lookup"><span data-stu-id="fb348-122">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="fb348-123">**MajorFunction**</span><span class="sxs-lookup"><span data-stu-id="fb348-123">**MajorFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb348-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fb348-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fb348-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fb348-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb348-126">限定詞： WmiDataId (1) </span><span class="sxs-lookup"><span data-stu-id="fb348-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="fb348-127">識別所呼叫之主要函式的程式碼。</span><span class="sxs-lookup"><span data-stu-id="fb348-127">Code that identifies the major function being called.</span></span>

</dd> <dt>

<span data-ttu-id="fb348-128">**MinorFunction**</span><span class="sxs-lookup"><span data-stu-id="fb348-128">**MinorFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb348-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fb348-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fb348-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fb348-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb348-131">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="fb348-131">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="fb348-132">Idenitifies 所呼叫之次要函式的程式碼。</span><span class="sxs-lookup"><span data-stu-id="fb348-132">Code that idenitifies the minor function being called.</span></span>

</dd> <dt>

<span data-ttu-id="fb348-133">**RoutineAddr**</span><span class="sxs-lookup"><span data-stu-id="fb348-133">**RoutineAddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb348-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fb348-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fb348-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fb348-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb348-136">限定詞： WmiDataId (3) ，指標</span><span class="sxs-lookup"><span data-stu-id="fb348-136">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="fb348-137">要呼叫的驅動程式函式的位址。</span><span class="sxs-lookup"><span data-stu-id="fb348-137">Address of the driver function being called.</span></span>

</dd> <dt>

<span data-ttu-id="fb348-138">**UniqMatchId**</span><span class="sxs-lookup"><span data-stu-id="fb348-138">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb348-139">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fb348-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fb348-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fb348-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb348-141">限定詞： WmiDataId (6) </span><span class="sxs-lookup"><span data-stu-id="fb348-141">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="fb348-142">可唯一識別要求的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fb348-142">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="fb348-143">您可以使用這個識別碼，將其他驅動程式事件相互關聯，例如 [**DriverCompleteRequest**](drivercompleterequest.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="fb348-143">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fb348-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb348-144">Requirements</span></span>



| <span data-ttu-id="fb348-145">需求</span><span class="sxs-lookup"><span data-stu-id="fb348-145">Requirement</span></span> | <span data-ttu-id="fb348-146">值</span><span class="sxs-lookup"><span data-stu-id="fb348-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fb348-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb348-147">Minimum supported client</span></span><br/> | <span data-ttu-id="fb348-148">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb348-148">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fb348-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb348-149">Minimum supported server</span></span><br/> | <span data-ttu-id="fb348-150">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb348-150">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fb348-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb348-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb348-152">**DiskIo**</span><span class="sxs-lookup"><span data-stu-id="fb348-152">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




