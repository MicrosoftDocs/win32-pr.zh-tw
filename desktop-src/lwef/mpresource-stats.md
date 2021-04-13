---
title: 'MPRESOURCE_STATS 結構 (MpClient .h) '
description: 與資源相關的統計資料。
ms.assetid: D1DC4BC9-911D-448C-A421-11D2F51F0A61
keywords:
- MPRESOURCE_STATS 結構舊版 Windows 環境功能
- PMPRESOURCE_STATS 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPRESOURCE_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afbe1ce6734aabd1093f7acd886af757c51ed83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465936"
---
# <a name="mpresource_stats-structure"></a><span data-ttu-id="2c6a3-105">MPRESOURCE \_ 統計結構</span><span class="sxs-lookup"><span data-stu-id="2c6a3-105">MPRESOURCE\_STATS structure</span></span>

<span data-ttu-id="2c6a3-106">與資源相關的統計資料。</span><span class="sxs-lookup"><span data-stu-id="2c6a3-106">Resource-related statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c6a3-107">語法</span><span class="sxs-lookup"><span data-stu-id="2c6a3-107">Syntax</span></span>


```C++
typedef struct tagMPRESOURCE_STATS {
  DWORD  PPMProgress;
  UINT64 ProcessCount;
  UINT64 FileCount;
  UINT64 FileBytesCount;
  UINT64 RegKeyCount;
  UINT64 Reserved[4];
} MPRESOURCE_STATS, *PMPRESOURCE_STATS;
```



## <a name="members"></a><span data-ttu-id="2c6a3-108">成員</span><span class="sxs-lookup"><span data-stu-id="2c6a3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2c6a3-109">**PPMProgress**</span><span class="sxs-lookup"><span data-stu-id="2c6a3-109">**PPMProgress**</span></span>
</dt> <dd>

<span data-ttu-id="2c6a3-110">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2c6a3-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="2c6a3-111">每百萬個)  (部分掃描的大約進度。</span><span class="sxs-lookup"><span data-stu-id="2c6a3-111">Approximate progress for scan in ppm (parts per million).</span></span> <span data-ttu-id="2c6a3-112">如果無法使用進度資訊，請將設定為 **MPPROGRESS \_ 無效** 。</span><span class="sxs-lookup"><span data-stu-id="2c6a3-112">Set to **MPPROGRESS\_INVALID** if progress information is not available.</span></span>

</dd> <dt>

<span data-ttu-id="2c6a3-113">**ProcessCount**</span><span class="sxs-lookup"><span data-stu-id="2c6a3-113">**ProcessCount**</span></span>
</dt> <dd>

<span data-ttu-id="2c6a3-114">類型： **UINT64**</span><span class="sxs-lookup"><span data-stu-id="2c6a3-114">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="2c6a3-115">掃描的進程數目。</span><span class="sxs-lookup"><span data-stu-id="2c6a3-115">Number of processes scanned.</span></span>

</dd> <dt>

<span data-ttu-id="2c6a3-116">**FileCount**</span><span class="sxs-lookup"><span data-stu-id="2c6a3-116">**FileCount**</span></span>
</dt> <dd>

<span data-ttu-id="2c6a3-117">類型： **UINT64**</span><span class="sxs-lookup"><span data-stu-id="2c6a3-117">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="2c6a3-118">掃描的檔案數目。</span><span class="sxs-lookup"><span data-stu-id="2c6a3-118">Number of files scanned.</span></span>

</dd> <dt>

<span data-ttu-id="2c6a3-119">**FileBytesCount**</span><span class="sxs-lookup"><span data-stu-id="2c6a3-119">**FileBytesCount**</span></span>
</dt> <dd>

<span data-ttu-id="2c6a3-120">類型： **UINT64**</span><span class="sxs-lookup"><span data-stu-id="2c6a3-120">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="2c6a3-121">掃描檔案的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="2c6a3-121">Number of bytes scanned for files.</span></span>

</dd> <dt>

<span data-ttu-id="2c6a3-122">**RegKeyCount**</span><span class="sxs-lookup"><span data-stu-id="2c6a3-122">**RegKeyCount**</span></span>
</dt> <dd>

<span data-ttu-id="2c6a3-123">類型： **UINT64**</span><span class="sxs-lookup"><span data-stu-id="2c6a3-123">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="2c6a3-124">掃描的 RegKeys 數目。</span><span class="sxs-lookup"><span data-stu-id="2c6a3-124">Number of RegKeys scanned.</span></span>

</dd> <dt>

<span data-ttu-id="2c6a3-125">**已保留**</span><span class="sxs-lookup"><span data-stu-id="2c6a3-125">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="2c6a3-126">類型： **UINT64 \[ 4 \]**</span><span class="sxs-lookup"><span data-stu-id="2c6a3-126">Type: **UINT64\[4\]**</span></span>

</dd> <dd>

<span data-ttu-id="2c6a3-127">保留供日後使用的欄位。</span><span class="sxs-lookup"><span data-stu-id="2c6a3-127">Fields reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c6a3-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c6a3-128">Requirements</span></span>



| <span data-ttu-id="2c6a3-129">需求</span><span class="sxs-lookup"><span data-stu-id="2c6a3-129">Requirement</span></span> | <span data-ttu-id="2c6a3-130">值</span><span class="sxs-lookup"><span data-stu-id="2c6a3-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c6a3-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c6a3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2c6a3-132">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c6a3-132">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2c6a3-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c6a3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2c6a3-134">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c6a3-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2c6a3-135">標頭</span><span class="sxs-lookup"><span data-stu-id="2c6a3-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c6a3-136"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="2c6a3-136"><dt>MpClient.h</dt></span></span> </dl> |



 

 





