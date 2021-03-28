---
description: 這個類別是檔案 i/o 事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: a4ee38df-af75-4aec-89ec-5a1c39302c82
title: FileIo_V1_Name 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V1_Name
- FileIo_V1_Name.FileObject
- FileIo_V1_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 617e0abeed095099996079211107d0720017514a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027041"
---
# <a name="fileio_v1_name-class"></a><span data-ttu-id="85abd-104">FileIo \_ V1 \_ 名稱類別</span><span class="sxs-lookup"><span data-stu-id="85abd-104">FileIo\_V1\_Name class</span></span>

<span data-ttu-id="85abd-105">這個類別是檔案 i/o 事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="85abd-105">This class is the event type class for file I/O events.</span></span>

<span data-ttu-id="85abd-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="85abd-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="85abd-107">語法</span><span class="sxs-lookup"><span data-stu-id="85abd-107">Syntax</span></span>

``` syntax
[EventType{0, 32}, EventTypeName{"Name", "FileCreate"}]
class FileIo_V1_Name : FileIo
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="85abd-108">成員</span><span class="sxs-lookup"><span data-stu-id="85abd-108">Members</span></span>

<span data-ttu-id="85abd-109">**FileIo \_ V1 \_ 名稱** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="85abd-109">The **FileIo\_V1\_Name** class has these types of members:</span></span>

-   [<span data-ttu-id="85abd-110">屬性</span><span class="sxs-lookup"><span data-stu-id="85abd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="85abd-111">屬性</span><span class="sxs-lookup"><span data-stu-id="85abd-111">Properties</span></span>

<span data-ttu-id="85abd-112">**FileIo \_ V1 \_ 名稱** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="85abd-112">The **FileIo\_V1\_Name** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="85abd-113">FileName</span><span class="sxs-lookup"><span data-stu-id="85abd-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85abd-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="85abd-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85abd-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85abd-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85abd-116">限定詞： WmiDataId (2) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="85abd-116">Qualifiers: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="85abd-117">檔案的完整路徑，不包括磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="85abd-117">Full path to the file, not including the drive letter.</span></span>

</dd> <dt>

<span data-ttu-id="85abd-118">FileObject</span><span class="sxs-lookup"><span data-stu-id="85abd-118">FileObject</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85abd-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="85abd-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85abd-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85abd-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85abd-121">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="85abd-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="85abd-122">將 this 指標的值符合 [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md)事件中的 **FileObject** 指標值，以判斷 i/o 作業的類型。</span><span class="sxs-lookup"><span data-stu-id="85abd-122">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85abd-123">備註</span><span class="sxs-lookup"><span data-stu-id="85abd-123">Remarks</span></span>

<span data-ttu-id="85abd-124">**Windows Server 2003：** 若要取得檔案名路徑的磁碟機號，請使用 **FileObject** 屬性值對應至對應的 [DiskIo \_ TypeGroup1](diskio-typegroup1.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="85abd-124">**Windows Server 2003:** To retrieve the drive letter for the file name path, use the **FileObject** property value to map to the corresponding [DiskIo\_TypeGroup1](diskio-typegroup1.md) event.</span></span> <span data-ttu-id="85abd-125">從 DiskIo \_ TypeGroup1 事件中，使用 **DiskNumber** 和 **ByteOffset** 屬性值對應至對應的 [SystemConfig \_ LogDisk](systemconfig-logdisk.md) 事件 (**ByteOffset** 對應至 **startoffset 位置**) 。</span><span class="sxs-lookup"><span data-stu-id="85abd-125">From the DiskIo\_TypeGroup1 event, use the **DiskNumber** and **ByteOffset** property values to map to the corresponding [SystemConfig\_LogDisk](systemconfig-logdisk.md) event (**ByteOffset** maps to **StartOffset**).</span></span> <span data-ttu-id="85abd-126">**DriveLetterString** 屬性包含磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="85abd-126">The **DriveLetterString** property contains the drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="85abd-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="85abd-127">Requirements</span></span>



| <span data-ttu-id="85abd-128">需求</span><span class="sxs-lookup"><span data-stu-id="85abd-128">Requirement</span></span> | <span data-ttu-id="85abd-129">值</span><span class="sxs-lookup"><span data-stu-id="85abd-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="85abd-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85abd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="85abd-131">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85abd-131">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="85abd-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85abd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="85abd-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85abd-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="85abd-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85abd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85abd-135">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="85abd-135">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




