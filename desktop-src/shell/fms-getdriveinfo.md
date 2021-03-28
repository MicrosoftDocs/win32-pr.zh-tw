---
description: 包含 [active File Manager] 視窗中所選磁片磁碟機的相關資訊 ([目錄] 視窗或 [搜尋結果] 視窗) 。
title: 'FMS_GETDRIVEINFO 結構 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 14f8a90b-d0ed-4818-a719-8fc4ea617bef
ms.openlocfilehash: b19b54d89f74fa122effa5853beb2961e0ddf1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973221"
---
# <a name="fms_getdriveinfo-structure"></a><span data-ttu-id="85945-103">FMS \_ GETDRIVEINFO 結構</span><span class="sxs-lookup"><span data-stu-id="85945-103">FMS\_GETDRIVEINFO structure</span></span>

<span data-ttu-id="85945-104">包含 [active File Manager] 視窗中所選磁片磁碟機的相關資訊 ([目錄] 視窗或 [搜尋結果] 視窗) 。</span><span class="sxs-lookup"><span data-stu-id="85945-104">Contains information about the drive selected in the active File Manager window (the directory window or the Search Results window).</span></span>

## <a name="syntax"></a><span data-ttu-id="85945-105">語法</span><span class="sxs-lookup"><span data-stu-id="85945-105">Syntax</span></span>


```C++
typedef struct _FMS_GETDRIVEINFO {
  DWORD dwTotalSpace;
  DWORD dwFreeSpace;
  TCHAR szPath[260];
  TCHAR szVolume[14];
  TCHAR szShare[128];
} FMS_GETDRIVEINFO;
```



## <a name="members"></a><span data-ttu-id="85945-106">成員</span><span class="sxs-lookup"><span data-stu-id="85945-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="85945-107">**dwTotalSpace**</span><span class="sxs-lookup"><span data-stu-id="85945-107">**dwTotalSpace**</span></span>
</dt> <dd>

<span data-ttu-id="85945-108">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="85945-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="85945-109">磁片磁碟機相關磁片的總儲存空間量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="85945-109">The total amount of storage space, in bytes, on the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="85945-110">**dwFreeSpace**</span><span class="sxs-lookup"><span data-stu-id="85945-110">**dwFreeSpace**</span></span>
</dt> <dd>

<span data-ttu-id="85945-111">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="85945-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="85945-112">磁片磁碟機相關磁片的可用儲存空間量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="85945-112">The amount of free storage space, in bytes, on the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="85945-113">**szPath**</span><span class="sxs-lookup"><span data-stu-id="85945-113">**szPath**</span></span>
</dt> <dd>

<span data-ttu-id="85945-114">類型： **TCHAR \[ 260 \]**</span><span class="sxs-lookup"><span data-stu-id="85945-114">Type: **TCHAR\[260\]**</span></span>

</dd> <dd>

<span data-ttu-id="85945-115">目前的目錄的以 null 結束路徑。</span><span class="sxs-lookup"><span data-stu-id="85945-115">the null-terminated path of the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="85945-116">**szVolume**</span><span class="sxs-lookup"><span data-stu-id="85945-116">**szVolume**</span></span>
</dt> <dd>

<span data-ttu-id="85945-117">類型： **TCHAR \[ 14 \]**</span><span class="sxs-lookup"><span data-stu-id="85945-117">Type: **TCHAR\[14\]**</span></span>

</dd> <dd>

<span data-ttu-id="85945-118">與磁片磁碟機相關聯之磁片的以 null 終止的磁片區標籤。</span><span class="sxs-lookup"><span data-stu-id="85945-118">The null-terminated volume label of the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="85945-119">**szShare**</span><span class="sxs-lookup"><span data-stu-id="85945-119">**szShare**</span></span>
</dt> <dd>

<span data-ttu-id="85945-120">類型： **TCHAR \[ 128 \]**</span><span class="sxs-lookup"><span data-stu-id="85945-120">Type: **TCHAR\[128\]**</span></span>

</dd> <dd>

<span data-ttu-id="85945-121">如果透過網路) 存取磁片磁碟機，則為網路資源 (以 null 終止的名稱。</span><span class="sxs-lookup"><span data-stu-id="85945-121">The null-terminated name of the network resource (if the drive is being accessed through a network).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="85945-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="85945-122">Requirements</span></span>



| <span data-ttu-id="85945-123">需求</span><span class="sxs-lookup"><span data-stu-id="85945-123">Requirement</span></span> | <span data-ttu-id="85945-124">值</span><span class="sxs-lookup"><span data-stu-id="85945-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="85945-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85945-125">Minimum supported client</span></span><br/> | <span data-ttu-id="85945-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85945-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="85945-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85945-127">Minimum supported server</span></span><br/> | <span data-ttu-id="85945-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85945-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="85945-129">標頭</span><span class="sxs-lookup"><span data-stu-id="85945-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="85945-130"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="85945-130"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85945-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85945-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85945-132">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="85945-132">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="85945-133">**FM \_ GETDRIVEINFO**</span><span class="sxs-lookup"><span data-stu-id="85945-133">**FM\_GETDRIVEINFO**</span></span>](fm-getdriveinfo.md)
</dt> </dl>

 

 




