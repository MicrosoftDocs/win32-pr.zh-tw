---
description: 此類別是列舉目錄和目錄通知事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 08458385-6066-4523-a053-aceb5e5d6f10
title: FileIo_DirEnum 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_DirEnum
- FileIo_DirEnum.IrpPtr
- FileIo_DirEnum.TTID
- FileIo_DirEnum.FileObject
- FileIo_DirEnum.FileKey
- FileIo_DirEnum.Length
- FileIo_DirEnum.InfoClass
- FileIo_DirEnum.FileIndex
- FileIo_DirEnum.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 12f8fd8b4629ac11e7316caae0690982c210e4bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972201"
---
# <a name="fileio_direnum-class"></a><span data-ttu-id="1a378-104">FileIo \_ DirEnum 類別</span><span class="sxs-lookup"><span data-stu-id="1a378-104">FileIo\_DirEnum class</span></span>

<span data-ttu-id="1a378-105">此類別是列舉目錄和目錄通知事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="1a378-105">This class is the event type class for the enumerate directory and directory notification events.</span></span>

<span data-ttu-id="1a378-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="1a378-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a378-107">語法</span><span class="sxs-lookup"><span data-stu-id="1a378-107">Syntax</span></span>

``` syntax
[EventType{72, 77}, EventTypeName{"DirEnum", "DirNotify"}]
class FileIo_DirEnum : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 Length;
  uint32 InfoClass;
  uint32 FileIndex;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="1a378-108">成員</span><span class="sxs-lookup"><span data-stu-id="1a378-108">Members</span></span>

<span data-ttu-id="1a378-109">**FileIo \_ DirEnum** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1a378-109">The **FileIo\_DirEnum** class has these types of members:</span></span>

-   [<span data-ttu-id="1a378-110">屬性</span><span class="sxs-lookup"><span data-stu-id="1a378-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a378-111">屬性</span><span class="sxs-lookup"><span data-stu-id="1a378-111">Properties</span></span>

<span data-ttu-id="1a378-112">**FileIo \_ DirEnum** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1a378-112">The **FileIo\_DirEnum** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1a378-113">**FileIndex**</span><span class="sxs-lookup"><span data-stu-id="1a378-113">**FileIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a378-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a378-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a378-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a378-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a378-116">限定詞： WmiDataId (7) </span><span class="sxs-lookup"><span data-stu-id="1a378-116">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="1a378-117">要從中繼續目錄列舉的檔案索引。</span><span class="sxs-lookup"><span data-stu-id="1a378-117">File index from which to continue directory enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="1a378-118">**FileKey**</span><span class="sxs-lookup"><span data-stu-id="1a378-118">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a378-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a378-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a378-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a378-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a378-121">限定詞： WmiDataId (4) ，指標</span><span class="sxs-lookup"><span data-stu-id="1a378-121">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1a378-122">若要判斷目錄名稱，請將這個屬性的值與 [**FileIo \_ name**](fileio-name.md)事件的 **FileObject** 屬性比對。</span><span class="sxs-lookup"><span data-stu-id="1a378-122">To determine the directory name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="1a378-123">**FileName**</span><span class="sxs-lookup"><span data-stu-id="1a378-123">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a378-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1a378-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a378-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a378-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a378-126">限定詞： WmiDataId (8) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="1a378-126">Qualifiers: WmiDataId(8), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="1a378-127">為目錄列舉指定的模式。</span><span class="sxs-lookup"><span data-stu-id="1a378-127">Pattern specified for directory enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="1a378-128">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="1a378-128">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a378-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a378-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a378-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a378-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a378-131">限定詞： WmiDataId (3) ，指標</span><span class="sxs-lookup"><span data-stu-id="1a378-131">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1a378-132">可在檔案建立和關閉事件之間，用來將作業相互關聯至相同開啟檔案物件實例的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1a378-132">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="1a378-133">**InfoClass**</span><span class="sxs-lookup"><span data-stu-id="1a378-133">**InfoClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a378-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a378-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a378-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a378-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a378-136">限定詞： WmiDataId (6) ，指標</span><span class="sxs-lookup"><span data-stu-id="1a378-136">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1a378-137">要求的目錄列舉資訊類別。</span><span class="sxs-lookup"><span data-stu-id="1a378-137">Requested directory enumeration information class.</span></span>

</dd> <dt>

<span data-ttu-id="1a378-138">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="1a378-138">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a378-139">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a378-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a378-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a378-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a378-141">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="1a378-141">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1a378-142">IO 要求封包。</span><span class="sxs-lookup"><span data-stu-id="1a378-142">IO request packet.</span></span> <span data-ttu-id="1a378-143">這個屬性會識別 IO 活動。</span><span class="sxs-lookup"><span data-stu-id="1a378-143">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="1a378-144">**長度**</span><span class="sxs-lookup"><span data-stu-id="1a378-144">**Length**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a378-145">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a378-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a378-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a378-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a378-147">限定詞： WmiDataId (5) </span><span class="sxs-lookup"><span data-stu-id="1a378-147">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="1a378-148">查詢緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1a378-148">Size of the query buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1a378-149">**TTID**</span><span class="sxs-lookup"><span data-stu-id="1a378-149">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a378-150">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a378-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a378-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a378-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a378-152">限定詞： WmiDataId (2) ，指標</span><span class="sxs-lookup"><span data-stu-id="1a378-152">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1a378-153">執行作業之執行緒的執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="1a378-153">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a378-154">備註</span><span class="sxs-lookup"><span data-stu-id="1a378-154">Remarks</span></span>

<span data-ttu-id="1a378-155">列舉目錄或將目錄變更通知分別傳送至已註冊的接聽程式時，會記錄目錄列舉和目錄通知事件。</span><span class="sxs-lookup"><span data-stu-id="1a378-155">Directory enumeration and directory notification events are recorded when a directory is enumerated or a directory change notification is sent to registered listeners, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a378-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a378-156">Requirements</span></span>



| <span data-ttu-id="1a378-157">需求</span><span class="sxs-lookup"><span data-stu-id="1a378-157">Requirement</span></span> | <span data-ttu-id="1a378-158">值</span><span class="sxs-lookup"><span data-stu-id="1a378-158">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1a378-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1a378-159">Minimum supported client</span></span><br/> | <span data-ttu-id="1a378-160">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a378-160">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1a378-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1a378-161">Minimum supported server</span></span><br/> | <span data-ttu-id="1a378-162">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a378-162">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1a378-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a378-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a378-164">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="1a378-164">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




