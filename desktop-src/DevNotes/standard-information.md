---
description: 包含標準資訊屬性。 這個屬性存在於每個基底檔案記錄中，而且必須是常駐的。
ms.assetid: 8e668309-2722-4115-923d-bf0aa78d24f1
title: STANDARD_INFORMATION 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STANDARD_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4927553ac593475f8659932468227362ae19fe59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025809"
---
# <a name="standard_information-structure"></a><span data-ttu-id="29e77-104">標準 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="29e77-104">STANDARD\_INFORMATION structure</span></span>

<span data-ttu-id="29e77-105">\[此結構只對 NTFS 磁片區的第3版有效;未來的版本可能會改變。\]</span><span class="sxs-lookup"><span data-stu-id="29e77-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="29e77-106">包含標準資訊屬性。</span><span class="sxs-lookup"><span data-stu-id="29e77-106">Contains the standard information attribute.</span></span> <span data-ttu-id="29e77-107">這個屬性存在於每個基底檔案記錄中，而且必須是常駐的。</span><span class="sxs-lookup"><span data-stu-id="29e77-107">This attribute is present in every base file record and must be resident.</span></span>

## <a name="syntax"></a><span data-ttu-id="29e77-108">語法</span><span class="sxs-lookup"><span data-stu-id="29e77-108">Syntax</span></span>


```C++
typedef struct _STANDARD_INFORMATION {
  UCHAR Reserved[0x30];
  ULONG OwnerId;
  ULONG SecurityId;
} STANDARD_INFORMATION, *PSTANDARD_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="29e77-109">成員</span><span class="sxs-lookup"><span data-stu-id="29e77-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="29e77-110">**已保留**</span><span class="sxs-lookup"><span data-stu-id="29e77-110">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="29e77-111">保留的。</span><span class="sxs-lookup"><span data-stu-id="29e77-111">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="29e77-112">**OwnerId**</span><span class="sxs-lookup"><span data-stu-id="29e77-112">**OwnerId**</span></span>
</dt> <dd>

<span data-ttu-id="29e77-113">來自安全性索引的檔案擁有者識別碼。</span><span class="sxs-lookup"><span data-stu-id="29e77-113">The identifier of the file owner, from the security index.</span></span>

</dd> <dt>

<span data-ttu-id="29e77-114">**SecurityId**</span><span class="sxs-lookup"><span data-stu-id="29e77-114">**SecurityId**</span></span>
</dt> <dd>

<span data-ttu-id="29e77-115">檔案的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="29e77-115">The security identifier for the file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29e77-116">備註</span><span class="sxs-lookup"><span data-stu-id="29e77-116">Remarks</span></span>

<span data-ttu-id="29e77-117">請注意，此結構沒有相關聯的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="29e77-117">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="29e77-118">此結構定義僅適用于主要版本3和次要版本0或1，如 [**FSCTL \_ 取得 \_ NTFS \_ 磁片區 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)所報告。</span><span class="sxs-lookup"><span data-stu-id="29e77-118">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

## <a name="see-also"></a><span data-ttu-id="29e77-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29e77-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29e77-120">主檔案資料表</span><span class="sxs-lookup"><span data-stu-id="29e77-120">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
