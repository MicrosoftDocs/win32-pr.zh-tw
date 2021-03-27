---
description: 這個類別是檔案操作結束事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 3925d5bf-f412-4248-a61f-e667efa9debd
title: FileIo_OpEnd 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_OpEnd
- FileIo_OpEnd.IrpPtr
- FileIo_OpEnd.ExtraInfo
- FileIo_OpEnd.NtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: d3f1c495cf44b84f8d7661b40cadec6ea255c6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694260"
---
# <a name="fileio_opend-class"></a><span data-ttu-id="99f52-104">FileIo \_ OpEnd 類別</span><span class="sxs-lookup"><span data-stu-id="99f52-104">FileIo\_OpEnd class</span></span>

<span data-ttu-id="99f52-105">這個類別是檔案操作結束事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="99f52-105">This class is the event type class for file operation end events.</span></span>

<span data-ttu-id="99f52-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="99f52-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="99f52-107">語法</span><span class="sxs-lookup"><span data-stu-id="99f52-107">Syntax</span></span>

``` syntax
[EventType{76}, EventTypeName{"OperationEnd"}]
class FileIo_OpEnd : FileIo
{
  uint32 IrpPtr;
  uint32 ExtraInfo;
  uint32 NtStatus;
};
```

## <a name="members"></a><span data-ttu-id="99f52-108">成員</span><span class="sxs-lookup"><span data-stu-id="99f52-108">Members</span></span>

<span data-ttu-id="99f52-109">**FileIo \_ OpEnd** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="99f52-109">The **FileIo\_OpEnd** class has these types of members:</span></span>

-   [<span data-ttu-id="99f52-110">屬性</span><span class="sxs-lookup"><span data-stu-id="99f52-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="99f52-111">屬性</span><span class="sxs-lookup"><span data-stu-id="99f52-111">Properties</span></span>

<span data-ttu-id="99f52-112">**FileIo \_ OpEnd** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="99f52-112">The **FileIo\_OpEnd** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="99f52-113">**>extrainfo**</span><span class="sxs-lookup"><span data-stu-id="99f52-113">**ExtraInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99f52-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="99f52-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="99f52-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="99f52-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="99f52-116">限定詞： WmiDataId (2) ，指標</span><span class="sxs-lookup"><span data-stu-id="99f52-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="99f52-117">檔案系統針對作業所傳回的額外資訊。</span><span class="sxs-lookup"><span data-stu-id="99f52-117">Extra information returned by the file system for the operation.</span></span> <span data-ttu-id="99f52-118">例如，讀取要求是所讀取的實際位元組數目。</span><span class="sxs-lookup"><span data-stu-id="99f52-118">For example for a read request, the actual number of bytes that were read.</span></span>

</dd> <dt>

<span data-ttu-id="99f52-119">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="99f52-119">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99f52-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="99f52-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="99f52-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="99f52-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="99f52-122">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="99f52-122">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="99f52-123">IO 要求封包。</span><span class="sxs-lookup"><span data-stu-id="99f52-123">IO request packet.</span></span> <span data-ttu-id="99f52-124">這個屬性會識別正在結束的 IO 活動。</span><span class="sxs-lookup"><span data-stu-id="99f52-124">This property identifies the IO activity that is ending.</span></span>

</dd> <dt>

<span data-ttu-id="99f52-125">**NtStatus**</span><span class="sxs-lookup"><span data-stu-id="99f52-125">**NtStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99f52-126">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="99f52-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="99f52-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="99f52-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="99f52-128">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="99f52-128">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="99f52-129">從作業傳回值。</span><span class="sxs-lookup"><span data-stu-id="99f52-129">Return value from the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99f52-130">備註</span><span class="sxs-lookup"><span data-stu-id="99f52-130">Remarks</span></span>

<span data-ttu-id="99f52-131">[**FileIo**](fileio.md) 事件會在作業開始時記錄。</span><span class="sxs-lookup"><span data-stu-id="99f52-131">[**FileIo**](fileio.md) events are logged at the beginning of the operation.</span></span> <span data-ttu-id="99f52-132">OpEnd 事件可以個別啟用，以指出這些作業的結尾。</span><span class="sxs-lookup"><span data-stu-id="99f52-132">OpEnd events can be enabled separately to indicate the end of those operations.</span></span> <span data-ttu-id="99f52-133">Irp 可以用來將開始和結束事件相互關聯。</span><span class="sxs-lookup"><span data-stu-id="99f52-133">Irp can be used to correlate the begin and end events.</span></span>

## <a name="requirements"></a><span data-ttu-id="99f52-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="99f52-134">Requirements</span></span>



| <span data-ttu-id="99f52-135">需求</span><span class="sxs-lookup"><span data-stu-id="99f52-135">Requirement</span></span> | <span data-ttu-id="99f52-136">值</span><span class="sxs-lookup"><span data-stu-id="99f52-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="99f52-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99f52-137">Minimum supported client</span></span><br/> | <span data-ttu-id="99f52-138">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99f52-138">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="99f52-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99f52-139">Minimum supported server</span></span><br/> | <span data-ttu-id="99f52-140">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99f52-140">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="99f52-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99f52-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99f52-142">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="99f52-142">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




