---
description: 這個類別是 file read 和 write 事件的事件型別類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 88c380fb-e043-40ab-aa74-550bce43c52b
title: FileIo_ReadWrite 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_ReadWrite
- FileIo_ReadWrite.Offset
- FileIo_ReadWrite.IrpPtr
- FileIo_ReadWrite.TTID
- FileIo_ReadWrite.FileObject
- FileIo_ReadWrite.FileKey
- FileIo_ReadWrite.IoSize
- FileIo_ReadWrite.IoFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: c684444ea35efe0fee9c38b15be8fe7e45e9a102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973556"
---
# <a name="fileio_readwrite-class"></a><span data-ttu-id="dbfbe-104">FileIo \_ ReadWrite 類別</span><span class="sxs-lookup"><span data-stu-id="dbfbe-104">FileIo\_ReadWrite class</span></span>

<span data-ttu-id="dbfbe-105">這個類別是 file read 和 write 事件的事件型別類別。</span><span class="sxs-lookup"><span data-stu-id="dbfbe-105">This class is the event type class for file read and write events.</span></span>

<span data-ttu-id="dbfbe-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="dbfbe-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbfbe-107">語法</span><span class="sxs-lookup"><span data-stu-id="dbfbe-107">Syntax</span></span>

``` syntax
[EventType{67, 68}, EventTypeName{"Read", "Write"}]
class FileIo_ReadWrite : FileIo
{
  uint64 Offset;
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 IoSize;
  uint32 IoFlags;
};
```

## <a name="members"></a><span data-ttu-id="dbfbe-108">成員</span><span class="sxs-lookup"><span data-stu-id="dbfbe-108">Members</span></span>

<span data-ttu-id="dbfbe-109">**FileIo \_ ReadWrite** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="dbfbe-109">The **FileIo\_ReadWrite** class has these types of members:</span></span>

-   [<span data-ttu-id="dbfbe-110">屬性</span><span class="sxs-lookup"><span data-stu-id="dbfbe-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dbfbe-111">屬性</span><span class="sxs-lookup"><span data-stu-id="dbfbe-111">Properties</span></span>

<span data-ttu-id="dbfbe-112">**FileIo \_ ReadWrite** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="dbfbe-112">The **FileIo\_ReadWrite** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dbfbe-113">**FileKey**</span><span class="sxs-lookup"><span data-stu-id="dbfbe-113">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfbe-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="dbfbe-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbfbe-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dbfbe-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbfbe-116">限定詞： WmiDataId (5) ，指標</span><span class="sxs-lookup"><span data-stu-id="dbfbe-116">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="dbfbe-117">若要判斷檔案名，請將這個屬性的值與 [**FileIo \_ name**](fileio-name.md)事件的 **FileObject** 屬性比對。</span><span class="sxs-lookup"><span data-stu-id="dbfbe-117">To determine the file name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="dbfbe-118">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="dbfbe-118">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfbe-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="dbfbe-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbfbe-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dbfbe-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbfbe-121">限定詞： WmiDataId (4) ，指標</span><span class="sxs-lookup"><span data-stu-id="dbfbe-121">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="dbfbe-122">可在檔案建立和關閉事件之間，用來將作業相互關聯至相同開啟檔案物件實例的識別碼。</span><span class="sxs-lookup"><span data-stu-id="dbfbe-122">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="dbfbe-123">**IoFlags**</span><span class="sxs-lookup"><span data-stu-id="dbfbe-123">**IoFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfbe-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="dbfbe-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbfbe-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dbfbe-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbfbe-126">限定詞： WmiDataId (7) </span><span class="sxs-lookup"><span data-stu-id="dbfbe-126">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="dbfbe-127">為此作業指定的 IO 要求封包旗標。</span><span class="sxs-lookup"><span data-stu-id="dbfbe-127">IO request packet flags specified for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="dbfbe-128">**IoSize**</span><span class="sxs-lookup"><span data-stu-id="dbfbe-128">**IoSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfbe-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="dbfbe-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbfbe-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dbfbe-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbfbe-131">限定詞： WmiDataId (6) </span><span class="sxs-lookup"><span data-stu-id="dbfbe-131">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="dbfbe-132">要求的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="dbfbe-132">Number of bytes requested.</span></span>

</dd> <dt>

<span data-ttu-id="dbfbe-133">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="dbfbe-133">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfbe-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="dbfbe-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbfbe-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dbfbe-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbfbe-136">限定詞： WmiDataId (2) ，指標</span><span class="sxs-lookup"><span data-stu-id="dbfbe-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="dbfbe-137">IO 要求封包。</span><span class="sxs-lookup"><span data-stu-id="dbfbe-137">IO request packet.</span></span> <span data-ttu-id="dbfbe-138">這個屬性會識別 IO 活動。</span><span class="sxs-lookup"><span data-stu-id="dbfbe-138">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="dbfbe-139">**Offset**</span><span class="sxs-lookup"><span data-stu-id="dbfbe-139">**Offset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfbe-140">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="dbfbe-140">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dbfbe-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dbfbe-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbfbe-142">限定詞： WmiDataId (1) </span><span class="sxs-lookup"><span data-stu-id="dbfbe-142">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="dbfbe-143">正在啟動所要求作業的檔案位移。</span><span class="sxs-lookup"><span data-stu-id="dbfbe-143">Starting file offset for the requested operation.</span></span>

</dd> <dt>

<span data-ttu-id="dbfbe-144">**TTID**</span><span class="sxs-lookup"><span data-stu-id="dbfbe-144">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfbe-145">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="dbfbe-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbfbe-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dbfbe-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbfbe-147">限定詞： WmiDataId (3) ，指標</span><span class="sxs-lookup"><span data-stu-id="dbfbe-147">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="dbfbe-148">執行作業之執行緒的執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="dbfbe-148">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dbfbe-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="dbfbe-149">Requirements</span></span>



| <span data-ttu-id="dbfbe-150">需求</span><span class="sxs-lookup"><span data-stu-id="dbfbe-150">Requirement</span></span> | <span data-ttu-id="dbfbe-151">值</span><span class="sxs-lookup"><span data-stu-id="dbfbe-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dbfbe-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dbfbe-152">Minimum supported client</span></span><br/> | <span data-ttu-id="dbfbe-153">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dbfbe-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dbfbe-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dbfbe-154">Minimum supported server</span></span><br/> | <span data-ttu-id="dbfbe-155">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dbfbe-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dbfbe-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dbfbe-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbfbe-157">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="dbfbe-157">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




