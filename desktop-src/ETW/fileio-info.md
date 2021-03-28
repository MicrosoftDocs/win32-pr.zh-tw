---
description: 這個類別是檔案資訊事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 41ae1f8a-a90f-43d0-a848-a2c095f046d4
title: FileIo_Info 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Info
- FileIo_Info.IrpPtr
- FileIo_Info.TTID
- FileIo_Info.FileObject
- FileIo_Info.FileKey
- FileIo_Info.ExtraInfo
- FileIo_Info.InfoClass
api_type:
- NA
api_location: ''
ms.openlocfilehash: 985986132abe432e1adefb51939b8ace1aa48c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973557"
---
# <a name="fileio_info-class"></a><span data-ttu-id="79983-104">FileIo \_ 資訊類別</span><span class="sxs-lookup"><span data-stu-id="79983-104">FileIo\_Info class</span></span>

<span data-ttu-id="79983-105">這個類別是檔案資訊事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="79983-105">This class is the event type class for file information event.</span></span>

<span data-ttu-id="79983-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="79983-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="79983-107">語法</span><span class="sxs-lookup"><span data-stu-id="79983-107">Syntax</span></span>

``` syntax
[EventType{69, 70, 71, 74, 75}, EventTypeName{"SetInfo", "Delete", "Rename", "QueryInfo", "FSControl"}]
class FileIo_Info : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 ExtraInfo;
  uint32 InfoClass;
};
```

## <a name="members"></a><span data-ttu-id="79983-108">成員</span><span class="sxs-lookup"><span data-stu-id="79983-108">Members</span></span>

<span data-ttu-id="79983-109">**FileIo \_ Info** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="79983-109">The **FileIo\_Info** class has these types of members:</span></span>

-   [<span data-ttu-id="79983-110">屬性</span><span class="sxs-lookup"><span data-stu-id="79983-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="79983-111">屬性</span><span class="sxs-lookup"><span data-stu-id="79983-111">Properties</span></span>

<span data-ttu-id="79983-112">**FileIo \_ Info** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="79983-112">The **FileIo\_Info** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="79983-113">**>extrainfo**</span><span class="sxs-lookup"><span data-stu-id="79983-113">**ExtraInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79983-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="79983-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79983-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="79983-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79983-116">限定詞： WmiDataId (5) ，指標</span><span class="sxs-lookup"><span data-stu-id="79983-116">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="79983-117">針對 FileDispositionInformation 要求，此欄位包含要求的配置。</span><span class="sxs-lookup"><span data-stu-id="79983-117">For FileDispositionInformation requests, this field contains the requested disposition.</span></span> <span data-ttu-id="79983-118">針對 FileEndOfFileInformation 和 FileAllocationInformation 要求，此欄位包含指定的檔案大小。</span><span class="sxs-lookup"><span data-stu-id="79983-118">For FileEndOfFileInformation and FileAllocationInformation requests, this field contains the specified file size.</span></span>

</dd> <dt>

<span data-ttu-id="79983-119">**FileKey**</span><span class="sxs-lookup"><span data-stu-id="79983-119">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79983-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="79983-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79983-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="79983-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79983-122">限定詞： WmiDataId (4) ，指標</span><span class="sxs-lookup"><span data-stu-id="79983-122">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="79983-123">若要判斷檔案名，請將這個屬性的值與 [**FileIo \_ name**](fileio-name.md)事件的 **FileObject** 屬性比對。</span><span class="sxs-lookup"><span data-stu-id="79983-123">To determine the file name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="79983-124">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="79983-124">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79983-125">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="79983-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79983-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="79983-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79983-127">限定詞： WmiDataId (3) ，指標</span><span class="sxs-lookup"><span data-stu-id="79983-127">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="79983-128">可在檔案建立和關閉事件之間，用來將作業相互關聯至相同開啟檔案物件實例的識別碼。</span><span class="sxs-lookup"><span data-stu-id="79983-128">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="79983-129">**InfoClass**</span><span class="sxs-lookup"><span data-stu-id="79983-129">**InfoClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79983-130">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="79983-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79983-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="79983-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79983-132">限定詞： WmiDataId (6) </span><span class="sxs-lookup"><span data-stu-id="79983-132">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="79983-133">要求的檔案資訊類別。</span><span class="sxs-lookup"><span data-stu-id="79983-133">Requested file information class.</span></span>

</dd> <dt>

<span data-ttu-id="79983-134">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="79983-134">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79983-135">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="79983-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79983-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="79983-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79983-137">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="79983-137">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="79983-138">IO 要求封包。</span><span class="sxs-lookup"><span data-stu-id="79983-138">IO request packet.</span></span> <span data-ttu-id="79983-139">這個屬性會識別 IO 活動。</span><span class="sxs-lookup"><span data-stu-id="79983-139">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="79983-140">**TTID**</span><span class="sxs-lookup"><span data-stu-id="79983-140">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79983-141">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="79983-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79983-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="79983-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79983-143">限定詞： WmiDataId (2) ，指標</span><span class="sxs-lookup"><span data-stu-id="79983-143">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="79983-144">執行作業之執行緒的執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="79983-144">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79983-145">備註</span><span class="sxs-lookup"><span data-stu-id="79983-145">Remarks</span></span>

<span data-ttu-id="79983-146">設定資訊和查詢資訊事件表示已設定或查詢檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="79983-146">Set information and query information events indicate that the file attributes were set or queried.</span></span> <span data-ttu-id="79983-147">發出 FSCTL 命令時，會記錄檔案系統控制項 (FSControl) 事件。</span><span class="sxs-lookup"><span data-stu-id="79983-147">A file system control (FSControl) event is recorded when a FSCTL command is issued.</span></span>

## <a name="requirements"></a><span data-ttu-id="79983-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="79983-148">Requirements</span></span>



| <span data-ttu-id="79983-149">需求</span><span class="sxs-lookup"><span data-stu-id="79983-149">Requirement</span></span> | <span data-ttu-id="79983-150">值</span><span class="sxs-lookup"><span data-stu-id="79983-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="79983-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="79983-151">Minimum supported client</span></span><br/> | <span data-ttu-id="79983-152">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79983-152">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="79983-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="79983-153">Minimum supported server</span></span><br/> | <span data-ttu-id="79983-154">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79983-154">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="79983-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79983-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79983-156">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="79983-156">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




