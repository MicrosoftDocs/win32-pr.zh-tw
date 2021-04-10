---
description: 包含磁片區開機磁區中儲存的磁片上檔案系統辨識資訊 (邏輯磁片磁區零) 。
ms.assetid: d9c19e01-ff82-4bbc-9eb6-aac9dc5c34ac
title: FILE_SYSTEM_RECOGNITION_STRUCTURE 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_SYSTEM_RECOGNITION_STRUCTURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: c542b2b9ee1cd1696c7c95797c7df20aa02180cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026509"
---
# <a name="file_system_recognition_structure-structure"></a><span data-ttu-id="f9f29-103">檔 \_ 系統 \_ 識別 \_ 結構結構</span><span class="sxs-lookup"><span data-stu-id="f9f29-103">FILE\_SYSTEM\_RECOGNITION\_STRUCTURE structure</span></span>

<span data-ttu-id="f9f29-104">包含磁片區開機磁區中儲存的磁片上檔案系統辨識資訊 (邏輯磁片磁區零) 。</span><span class="sxs-lookup"><span data-stu-id="f9f29-104">Contains the on-disk file system recognition information stored in the volume's boot sector (logical disk sector zero).</span></span>

<span data-ttu-id="f9f29-105">這是在公用標頭中無法使用的內部定義資料結構，在此提供給想要利用檔案系統識別的檔案系統開發人員使用。</span><span class="sxs-lookup"><span data-stu-id="f9f29-105">This is an internally-defined data structure not available in a public header and is provided here for file system developers who want to take advantage of file system recognition.</span></span> <span data-ttu-id="f9f29-106">如需詳細資訊，請參閱 [檔案系統識別](file-system-recognition.md)。</span><span class="sxs-lookup"><span data-stu-id="f9f29-106">For more information, see [File System Recognition](file-system-recognition.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f9f29-107">語法</span><span class="sxs-lookup"><span data-stu-id="f9f29-107">Syntax</span></span>


```C++
typedef struct _FILE_SYSTEM_RECOGNITION_STRUCTURE {
  UCHAR  Jmp[3];
  UCHAR  FsName[8];
  UCHAR  MustBeZero[5];
  ULONG  Identifier;
  USHORT Length;
  USHORT Checksum;
} FILE_SYSTEM_RECOGNITION_STRUCTURE;
```



## <a name="members"></a><span data-ttu-id="f9f29-108">成員</span><span class="sxs-lookup"><span data-stu-id="f9f29-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f9f29-109">**Jmp**</span><span class="sxs-lookup"><span data-stu-id="f9f29-109">**Jmp**</span></span>
</dt> <dd>

<span data-ttu-id="f9f29-110">JMP 指令。</span><span class="sxs-lookup"><span data-stu-id="f9f29-110">The JMP instruction.</span></span> <span data-ttu-id="f9f29-111">總和 **檢查** 碼資料成員所包含的值中不會包含此資料成員。</span><span class="sxs-lookup"><span data-stu-id="f9f29-111">This data member is not included in the value contained in the **Checksum** data member.</span></span>

</dd> <dt>

<span data-ttu-id="f9f29-112">**FsName**</span><span class="sxs-lookup"><span data-stu-id="f9f29-112">**FsName**</span></span>
</dt> <dd>

<span data-ttu-id="f9f29-113">檔案系統名稱。</span><span class="sxs-lookup"><span data-stu-id="f9f29-113">The file system name.</span></span> <span data-ttu-id="f9f29-114">這是8個 ASCII 字元的序列，代表磁片區所格式化之檔案系統的 nonlocalizable 人類可讀取名稱。</span><span class="sxs-lookup"><span data-stu-id="f9f29-114">This is a sequence of 8 ASCII characters that represents the nonlocalizable human-readable name of the file system the volume is formatted with.</span></span>

<span data-ttu-id="f9f29-115">此字串與具有一般 BIOS 參數區塊 (BPB) 結構的磁片上的 OEM 檔案系統名稱相同。</span><span class="sxs-lookup"><span data-stu-id="f9f29-115">This string is in the same place as the OEM file system name on a disk with a normal BIOS parameter block (BPB) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f9f29-116">**MustBeZero**</span><span class="sxs-lookup"><span data-stu-id="f9f29-116">**MustBeZero**</span></span>
</dt> <dd>

<span data-ttu-id="f9f29-117">包含所有零的保留空間。</span><span class="sxs-lookup"><span data-stu-id="f9f29-117">Reserved space that contains all zeros.</span></span>

<span data-ttu-id="f9f29-118">此資料成員會與 BPB 中的下列資料成員正常地重迭：</span><span class="sxs-lookup"><span data-stu-id="f9f29-118">This data member overlaps what normally are the following data members in a BPB:</span></span>

-   <span data-ttu-id="f9f29-119">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="f9f29-119">**BytesPerSector**</span></span>
-   <span data-ttu-id="f9f29-120">**SectorsPerCluster**</span><span class="sxs-lookup"><span data-stu-id="f9f29-120">**SectorsPerCluster**</span></span>
-   <span data-ttu-id="f9f29-121">**ReservedSectorCount**</span><span class="sxs-lookup"><span data-stu-id="f9f29-121">**ReservedSectorCount**</span></span>

<span data-ttu-id="f9f29-122">因為這些資料成員會設定為零，所以這應該就足以讓較早的 Os 結束，因為這不是有效的 BPB，因此可辨識磁片區。</span><span class="sxs-lookup"><span data-stu-id="f9f29-122">Because these data members are set to zero, this should be sufficient to cause earlier OSs to conclude that this is not a valid BPB and therefore recognize the volume.</span></span>

</dd> <dt>

<span data-ttu-id="f9f29-123">**識別碼**</span><span class="sxs-lookup"><span data-stu-id="f9f29-123">**Identifier**</span></span>
</dt> <dd>

<span data-ttu-id="f9f29-124">結構識別碼。</span><span class="sxs-lookup"><span data-stu-id="f9f29-124">A structure identifier.</span></span> <span data-ttu-id="f9f29-125">必須包含以位元組由大到小的位元組順序排列的值0x53525346。</span><span class="sxs-lookup"><span data-stu-id="f9f29-125">Must contain the value 0x53525346 arranged in little-endian byte order.</span></span>

<span data-ttu-id="f9f29-126">在結構中的這個位置，資料會對齊16個位元組。</span><span class="sxs-lookup"><span data-stu-id="f9f29-126">At this point in the structure, the data is aligned to 16 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f9f29-127">**長度**</span><span class="sxs-lookup"><span data-stu-id="f9f29-127">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="f9f29-128">此結構中從開頭到結尾的位元組數目，包括 **Jmp** 資料成員。</span><span class="sxs-lookup"><span data-stu-id="f9f29-128">The number of bytes in this structure, from the beginning to the end, including the **Jmp** data member.</span></span>

</dd> <dt>

<span data-ttu-id="f9f29-129">**校驗**</span><span class="sxs-lookup"><span data-stu-id="f9f29-129">**Checksum**</span></span>
</dt> <dd>

<span data-ttu-id="f9f29-130">從 **FsName** 資料成員開始算起的位元組的雙位元組總和檢查碼，並且在此結構的最後一個位元組結尾，但不包括 **Jmp** 和總和 **檢查** 碼的資料成員。</span><span class="sxs-lookup"><span data-stu-id="f9f29-130">A two-byte checksum calculated over the bytes starting at the **FsName** data member and ending at the last byte of this structure, excluding the **Jmp** and **Checksum** data members.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9f29-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9f29-131">Requirements</span></span>



| <span data-ttu-id="f9f29-132">需求</span><span class="sxs-lookup"><span data-stu-id="f9f29-132">Requirement</span></span> | <span data-ttu-id="f9f29-133">值</span><span class="sxs-lookup"><span data-stu-id="f9f29-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f9f29-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9f29-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f9f29-135">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9f29-135">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f9f29-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9f29-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f9f29-137">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9f29-137">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9f29-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9f29-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9f29-139">計算檔案系統識別總和檢查碼</span><span class="sxs-lookup"><span data-stu-id="f9f29-139">Computing a File System Recognition Checksum</span></span>](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[<span data-ttu-id="f9f29-140">檔案系統識別</span><span class="sxs-lookup"><span data-stu-id="f9f29-140">File System Recognition</span></span>](file-system-recognition.md)
</dt> <dt>

[<span data-ttu-id="f9f29-141">**檔 \_ 系統 \_ 識別 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f9f29-141">**FILE\_SYSTEM\_RECOGNITION\_INFORMATION**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-file_system_recognition_information)
</dt> <dt>

[<span data-ttu-id="f9f29-142">**FSCTL \_ 查詢 \_ 檔 \_ 系統 \_ 識別**</span><span class="sxs-lookup"><span data-stu-id="f9f29-142">**FSCTL\_QUERY\_FILE\_SYSTEM\_RECOGNITION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

