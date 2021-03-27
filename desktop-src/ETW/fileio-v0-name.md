---
description: FileIo \_ V0 \_ Name 類別是檔案 i/o 事件之事件種類類別的較舊版本。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: dcbe37f2-6df0-41a5-b85f-dcd06cbd5901
title: FileIo_V0_Name 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V0_Name
- FileIo_V0_Name.FileObject
- FileIo_V0_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6e88d1b9b5b36815b1a833062c30e804e4db744a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694259"
---
# <a name="fileio_v0_name-class"></a><span data-ttu-id="43081-104">FileIo \_ V0 \_ Name 類別</span><span class="sxs-lookup"><span data-stu-id="43081-104">FileIo\_V0\_Name class</span></span>

<span data-ttu-id="43081-105">**FileIo \_ V0 \_ Name** 類別是檔案 i/o 事件之事件種類類別的較舊版本。</span><span class="sxs-lookup"><span data-stu-id="43081-105">The **FileIo\_V0\_Name** class is an older version of the event type class for file I/O events.</span></span>

<span data-ttu-id="43081-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="43081-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="43081-107">語法</span><span class="sxs-lookup"><span data-stu-id="43081-107">Syntax</span></span>

``` syntax
[EventType(0), EventTypeName("Name")]
class FileIo_V0_Name : FileIo_V0
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="43081-108">成員</span><span class="sxs-lookup"><span data-stu-id="43081-108">Members</span></span>

<span data-ttu-id="43081-109">**FileIo \_ V0 \_ Name** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="43081-109">The **FileIo\_V0\_Name** class has these types of members:</span></span>

-   [<span data-ttu-id="43081-110">屬性</span><span class="sxs-lookup"><span data-stu-id="43081-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43081-111">屬性</span><span class="sxs-lookup"><span data-stu-id="43081-111">Properties</span></span>

<span data-ttu-id="43081-112">**FileIo \_ V0 \_ Name** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="43081-112">The **FileIo\_V0\_Name** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="43081-113">FileName</span><span class="sxs-lookup"><span data-stu-id="43081-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43081-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="43081-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43081-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43081-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43081-116">限定詞： WmiDataId (2) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="43081-116">Qualifiers: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="43081-117">檔案的完整路徑，不包括磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="43081-117">Full path to the file, not including the drive letter.</span></span>

</dd> <dt>

<span data-ttu-id="43081-118">FileObject</span><span class="sxs-lookup"><span data-stu-id="43081-118">FileObject</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43081-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="43081-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43081-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43081-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43081-121">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="43081-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="43081-122">將 this 指標的值符合 [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md)事件中的 **FileObject** 指標值，以判斷 i/o 作業的類型。</span><span class="sxs-lookup"><span data-stu-id="43081-122">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43081-123">備註</span><span class="sxs-lookup"><span data-stu-id="43081-123">Remarks</span></span>

<span data-ttu-id="43081-124">**Windows Server 2003：** 若要取得檔案名路徑的磁碟機號，請使用 **FileObject** 屬性值對應至對應的 [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="43081-124">**Windows Server 2003:** To retrieve the drive letter for the file name path, use the **FileObject** property value to map to the corresponding [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event.</span></span> <span data-ttu-id="43081-125">從 **DiskIo \_ TypeGroup1** 事件中，使用 **DiskNumber** 和 **ByteOffset** 屬性值對應至對應的 [**SystemConfig \_ LogDisk**](systemconfig-logdisk.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="43081-125">From the **DiskIo\_TypeGroup1** event, use the **DiskNumber** and **ByteOffset** property values to map to the corresponding [**SystemConfig\_LogDisk**](systemconfig-logdisk.md) event.</span></span> <span data-ttu-id="43081-126">**DriveLetterString** 屬性包含磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="43081-126">The **DriveLetterString** property contains the drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="43081-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="43081-127">Requirements</span></span>



| <span data-ttu-id="43081-128">需求</span><span class="sxs-lookup"><span data-stu-id="43081-128">Requirement</span></span> | <span data-ttu-id="43081-129">值</span><span class="sxs-lookup"><span data-stu-id="43081-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="43081-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="43081-130">Minimum supported client</span></span><br/> | <span data-ttu-id="43081-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="43081-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="43081-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="43081-132">Minimum supported server</span></span><br/> | <span data-ttu-id="43081-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="43081-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="43081-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43081-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43081-135">**FileIo \_ V0**</span><span class="sxs-lookup"><span data-stu-id="43081-135">**FileIo\_V0**</span></span>](fileio-v0.md)
</dt> </dl>

 

 




