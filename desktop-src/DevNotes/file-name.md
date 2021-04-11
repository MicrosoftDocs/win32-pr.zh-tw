---
description: 表示檔案名屬性。 針對輸入的每個目錄，檔案都有一個檔案名屬性。
ms.assetid: 54458eee-b786-446c-80bd-213c13bdeb4a
title: FILE_NAME 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_NAME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 609725c21f0c0811a4222cd9dfd662b3e25673f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025817"
---
# <a name="file_name-structure"></a><span data-ttu-id="e636a-104">檔案名 \_ 結構</span><span class="sxs-lookup"><span data-stu-id="e636a-104">FILE\_NAME structure</span></span>

<span data-ttu-id="e636a-105">\[此結構只對 NTFS 磁片區的第3版有效;未來的版本可能會改變。\]</span><span class="sxs-lookup"><span data-stu-id="e636a-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="e636a-106">表示檔案名屬性。</span><span class="sxs-lookup"><span data-stu-id="e636a-106">Represents a file name attribute.</span></span> <span data-ttu-id="e636a-107">針對輸入的每個目錄，檔案都有一個檔案名屬性。</span><span class="sxs-lookup"><span data-stu-id="e636a-107">A file has one file name attribute for every directory it is entered into.</span></span>

## <a name="syntax"></a><span data-ttu-id="e636a-108">語法</span><span class="sxs-lookup"><span data-stu-id="e636a-108">Syntax</span></span>


```C++
typedef struct _FILE_NAME {
  FILE_REFERENCE ParentDirectory;
  UCHAR          Reserved[0x38];
  UCHAR          FileNameLength;
  UCHAR          Flags;
  WCHAR          FileName[1];
} FILE_NAME, *PFILE_NAME;
```



## <a name="members"></a><span data-ttu-id="e636a-109">成員</span><span class="sxs-lookup"><span data-stu-id="e636a-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="e636a-110">**ParentDirectory**</span><span class="sxs-lookup"><span data-stu-id="e636a-110">**ParentDirectory**</span></span>
</dt> <dd>

<span data-ttu-id="e636a-111">針對此名稱編制索引之目錄的檔案參考。</span><span class="sxs-lookup"><span data-stu-id="e636a-111">A file reference to the directory that indexes to this name.</span></span> <span data-ttu-id="e636a-112">請參閱 [**MFT \_ 區段 \_ 參考**](mft-segment-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="e636a-112">See [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="e636a-113">**已保留**</span><span class="sxs-lookup"><span data-stu-id="e636a-113">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="e636a-114">保留的。</span><span class="sxs-lookup"><span data-stu-id="e636a-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e636a-115">**FileNameLength**</span><span class="sxs-lookup"><span data-stu-id="e636a-115">**FileNameLength**</span></span>
</dt> <dd>

<span data-ttu-id="e636a-116">檔案名的長度（以 Unicode 字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="e636a-116">The length of the file name, in Unicode characters.</span></span>

</dd> <dt>

<span data-ttu-id="e636a-117">**旗標**</span><span class="sxs-lookup"><span data-stu-id="e636a-117">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="e636a-118">檔案名旗標。</span><span class="sxs-lookup"><span data-stu-id="e636a-118">The file name flags.</span></span>

<dl> <dt>

<span data-ttu-id="e636a-119"><span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**檔案 \_名稱 \_ NTFS** (0x01) </span><span class="sxs-lookup"><span data-stu-id="e636a-119"><span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**FILE\_NAME\_NTFS** (0x01)</span></span>
</dt> <dt>

<span data-ttu-id="e636a-120"><span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**檔案 \_名稱 \_ DOS** (0x02) </span><span class="sxs-lookup"><span data-stu-id="e636a-120"><span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**FILE\_NAME\_DOS** (0x02)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="e636a-121">**FileName**</span><span class="sxs-lookup"><span data-stu-id="e636a-121">**FileName**</span></span>
</dt> <dd>

<span data-ttu-id="e636a-122">檔案名的第一個字元。</span><span class="sxs-lookup"><span data-stu-id="e636a-122">The first character of the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e636a-123">備註</span><span class="sxs-lookup"><span data-stu-id="e636a-123">Remarks</span></span>

<span data-ttu-id="e636a-124">請注意，此結構沒有相關聯的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="e636a-124">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="e636a-125">此結構定義僅適用于主要版本3和次要版本0或1，如 [**FSCTL \_ 取得 \_ NTFS \_ 磁片區 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)所報告。</span><span class="sxs-lookup"><span data-stu-id="e636a-125">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

## <a name="see-also"></a><span data-ttu-id="e636a-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e636a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e636a-127">主檔案資料表</span><span class="sxs-lookup"><span data-stu-id="e636a-127">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
