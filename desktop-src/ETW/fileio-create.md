---
description: 這個類別是 file create 事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 83465072-3dae-4a39-8a36-1512025b79df
title: FileIo_Create 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Create
- FileIo_Create.IrpPtr
- FileIo_Create.TTID
- FileIo_Create.FileObject
- FileIo_Create.CreateOptions
- FileIo_Create.FileAttributes
- FileIo_Create.ShareAccess
- FileIo_Create.OpenPath
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f8a42e9dee1c49817d578ab73a221c013f69aef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972204"
---
# <a name="fileio_create-class"></a><span data-ttu-id="7e95d-104">FileIo \_ Create 類別</span><span class="sxs-lookup"><span data-stu-id="7e95d-104">FileIo\_Create class</span></span>

<span data-ttu-id="7e95d-105">這個類別是 file create 事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="7e95d-105">This class is the event type class for the file create event.</span></span>

<span data-ttu-id="7e95d-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="7e95d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e95d-107">語法</span><span class="sxs-lookup"><span data-stu-id="7e95d-107">Syntax</span></span>

``` syntax
[EventType{64}, EventTypeName{"Create"}]
class FileIo_Create : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 CreateOptions;
  uint32 FileAttributes;
  uint32 ShareAccess;
  string OpenPath;
};
```

## <a name="members"></a><span data-ttu-id="7e95d-108">成員</span><span class="sxs-lookup"><span data-stu-id="7e95d-108">Members</span></span>

<span data-ttu-id="7e95d-109">**FileIo \_ Create** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7e95d-109">The **FileIo\_Create** class has these types of members:</span></span>

-   [<span data-ttu-id="7e95d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="7e95d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e95d-111">屬性</span><span class="sxs-lookup"><span data-stu-id="7e95d-111">Properties</span></span>

<span data-ttu-id="7e95d-112">**FileIo \_ Create** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7e95d-112">The **FileIo\_Create** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e95d-113">**CreateOptions**</span><span class="sxs-lookup"><span data-stu-id="7e95d-113">**CreateOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e95d-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7e95d-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e95d-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7e95d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e95d-116">限定詞： WmiDataId (4) </span><span class="sxs-lookup"><span data-stu-id="7e95d-116">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="7e95d-117">傳遞至 *CreateOptions* 和 *CreateDispositions* 參數的值會傳遞給 [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) 函數。</span><span class="sxs-lookup"><span data-stu-id="7e95d-117">Values passed in the *CreateOptions* and *CreateDispositions* parameters to the [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) function.</span></span>

</dd> <dt>

<span data-ttu-id="7e95d-118">**FileAttributes**</span><span class="sxs-lookup"><span data-stu-id="7e95d-118">**FileAttributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e95d-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7e95d-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e95d-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7e95d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e95d-121">限定詞： WmiDataId (5) </span><span class="sxs-lookup"><span data-stu-id="7e95d-121">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="7e95d-122">傳遞至 [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile)函數的 *FileAttributes* 參數值。</span><span class="sxs-lookup"><span data-stu-id="7e95d-122">Value passed in the *FileAttributes* parameter to the [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) function.</span></span>

</dd> <dt>

<span data-ttu-id="7e95d-123">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="7e95d-123">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e95d-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7e95d-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e95d-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7e95d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e95d-126">限定詞： WmiDataId (3) ，指標</span><span class="sxs-lookup"><span data-stu-id="7e95d-126">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="7e95d-127">可在檔案建立和關閉事件之間，用來將作業相互關聯至相同開啟檔案物件實例的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e95d-127">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="7e95d-128">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="7e95d-128">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e95d-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7e95d-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e95d-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7e95d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e95d-131">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="7e95d-131">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="7e95d-132">IO 要求封包。</span><span class="sxs-lookup"><span data-stu-id="7e95d-132">IO request packet.</span></span> <span data-ttu-id="7e95d-133">這個屬性會識別 IO 活動。</span><span class="sxs-lookup"><span data-stu-id="7e95d-133">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="7e95d-134">**OpenPath**</span><span class="sxs-lookup"><span data-stu-id="7e95d-134">**OpenPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e95d-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7e95d-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e95d-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7e95d-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e95d-137">限定詞： WmiDataId (7) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="7e95d-137">Qualifiers: WmiDataId(7), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="7e95d-138">檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="7e95d-138">Path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="7e95d-139">**ShareAccess**</span><span class="sxs-lookup"><span data-stu-id="7e95d-139">**ShareAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e95d-140">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7e95d-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e95d-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7e95d-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e95d-142">限定詞： WmiDataId (6) </span><span class="sxs-lookup"><span data-stu-id="7e95d-142">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="7e95d-143">傳遞至 [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile)函數的 *ShareAccess* 參數值。</span><span class="sxs-lookup"><span data-stu-id="7e95d-143">Value passed in the *ShareAccess* parameter to the [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) function.</span></span>

</dd> <dt>

<span data-ttu-id="7e95d-144">**TTID**</span><span class="sxs-lookup"><span data-stu-id="7e95d-144">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e95d-145">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7e95d-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e95d-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7e95d-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e95d-147">限定詞： WmiDataId (2) ，指標</span><span class="sxs-lookup"><span data-stu-id="7e95d-147">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="7e95d-148">建立檔案之執行緒的執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e95d-148">Thread identifier of the thread that is creating the file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e95d-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e95d-149">Requirements</span></span>



| <span data-ttu-id="7e95d-150">需求</span><span class="sxs-lookup"><span data-stu-id="7e95d-150">Requirement</span></span> | <span data-ttu-id="7e95d-151">值</span><span class="sxs-lookup"><span data-stu-id="7e95d-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7e95d-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7e95d-152">Minimum supported client</span></span><br/> | <span data-ttu-id="7e95d-153">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e95d-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7e95d-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7e95d-154">Minimum supported server</span></span><br/> | <span data-ttu-id="7e95d-155">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e95d-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7e95d-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e95d-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e95d-157">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="7e95d-157">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 
