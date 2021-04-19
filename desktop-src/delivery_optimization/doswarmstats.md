---
title: 'DOSwarmStats 結構 (>deliveryoptimization .h) '
description: 包含用來下載和上傳檔案之統計資料的欄位。
ms.assetid: 66B2498A-38E0-44E4-96C1-F778BD9AA593
keywords:
- DOSwarmStats 結構
topic_type:
- apiref
api_name:
- DOSwarmStats
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53d1702c25716ffe90c35727a258134311d5f427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106976978"
---
# <a name="doswarmstats-structure"></a><span data-ttu-id="b0430-104">DOSwarmStats 結構</span><span class="sxs-lookup"><span data-stu-id="b0430-104">DOSwarmStats structure</span></span>

<span data-ttu-id="b0430-105">包含用來下載和上傳檔案之統計資料的欄位。</span><span class="sxs-lookup"><span data-stu-id="b0430-105">Contains fields for download and upload statistics for a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0430-106">語法</span><span class="sxs-lookup"><span data-stu-id="b0430-106">Syntax</span></span>


```C++
typedef struct _DOSwarmStats {
  LPWSTR       fileId;
  LPWSTR       sourceURL;
  UINT64       fileSize;
  UINT64       totalBytesDownloaded;
  UINT64       bytesFromLanPeers;
  UINT64       bytesFromGroupPeers;
  UINT64       bytesFromInternetPeers;
  UINT64       bytesFromHttp;
  UINT64       bytesFromDoinc;
  UINT64       bytesToLanPeers;
  UINT64       bytesToGroupPeers;
  UINT64       bytesToInternetPeers;
  UINT         httpConnectionCount;
  UINT         doincConnectionCount;
  UINT         lanConnectionCount;
  UINT         groupConnectionCount;
  UINT         internetConnectionCount;
  UINT         downloadDuration;
  DownloadMode downloadMode;
  SwarmStatus  status;
  BOOL         isBackground;
} DOSwarmStats;
```



## <a name="members"></a><span data-ttu-id="b0430-107">成員</span><span class="sxs-lookup"><span data-stu-id="b0430-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b0430-108">**fileId**</span><span class="sxs-lookup"><span data-stu-id="b0430-108">**fileId**</span></span>
</dt> <dd>

<span data-ttu-id="b0430-109">以 **AddFileWithRanges** 呼叫所指定之以 Null 結束的字串。</span><span class="sxs-lookup"><span data-stu-id="b0430-109">Null-terminated string that was specified with the **AddFileWithRanges** call.</span></span>

</dd> <dt>

<span data-ttu-id="b0430-110">**sourceURL**</span><span class="sxs-lookup"><span data-stu-id="b0430-110">**sourceURL**</span></span>
</dt> <dd>

<span data-ttu-id="b0430-111">以 Null 終止的字串，其中包含伺服器上的檔案名 (例如，HTTPs:// &lt; server &gt; / &lt; path &gt; /file.ext) 。</span><span class="sxs-lookup"><span data-stu-id="b0430-111">Null-terminated string that contains the name of the file on the server (for example, https://&lt;server&gt;/&lt;path&gt;/file.ext).</span></span>

</dd> <dt>

<span data-ttu-id="b0430-112">**fileSize**</span><span class="sxs-lookup"><span data-stu-id="b0430-112">**fileSize**</span></span>
</dt> <dd>

<span data-ttu-id="b0430-113">檔案大小，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="b0430-113">Size of the file in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b0430-114">**totalBytesDownloaded**</span><span class="sxs-lookup"><span data-stu-id="b0430-114">**totalBytesDownloaded**</span></span>
</dt> <dd>

<span data-ttu-id="b0430-115">傳送的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="b0430-115">Total number of bytes transferred.</span></span>

</dd> <dt>

<span data-ttu-id="b0430-116">**bytesFromLanPeers**</span><span class="sxs-lookup"><span data-stu-id="b0430-116">**bytesFromLanPeers**</span></span>
</dt> <dd>

<span data-ttu-id="b0430-117">從 LAN 對等傳送的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="b0430-117">Number of bytes transferred from LAN peers.</span></span>

</dd> <dt>

<span data-ttu-id="b0430-118">**bytesFromGroupPeers**</span><span class="sxs-lookup"><span data-stu-id="b0430-118">**bytesFromGroupPeers**</span></span>
</dt> <dd>

<span data-ttu-id="b0430-119">從群組對等傳輸的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="b0430-119">Number of bytes transferred from group peers.</span></span>

</dd> <dt>

<span data-ttu-id="b0430-120">**bytesFromInternetPeers**</span><span class="sxs-lookup"><span data-stu-id="b0430-120">**bytesFromInternetPeers**</span></span>
</dt> <dd>

<span data-ttu-id="b0430-121">從網際網路對等傳送的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="b0430-121">Number of bytes transferred from Internet peers.</span></span>

</dd> <dt>

<span data-ttu-id="b0430-122">**bytesFromHttp**</span><span class="sxs-lookup"><span data-stu-id="b0430-122">**bytesFromHttp**</span></span>
</dt> <dd>

<span data-ttu-id="b0430-123">從 HTTP 傳輸的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="b0430-123">Number of bytes transferred from http.</span></span>

</dd> <dt>

<span data-ttu-id="b0430-124">**bytesFromDoinc**</span><span class="sxs-lookup"><span data-stu-id="b0430-124">**bytesFromDoinc**</span></span>
</dt> <dd>

<span data-ttu-id="b0430-125">僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="b0430-125">For internal use only.</span></span>

</dd> <dt>

<span data-ttu-id="b0430-126">**bytesToLanPeers**</span><span class="sxs-lookup"><span data-stu-id="b0430-126">**bytesToLanPeers**</span></span>
</dt> <dd>

<span data-ttu-id="b0430-127">傳送至 LAN 對等的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="b0430-127">Number of bytes transferred to LAN peers.</span></span>

</dd> <dt>

<span data-ttu-id="b0430-128">**bytesToGroupPeers**</span><span class="sxs-lookup"><span data-stu-id="b0430-128">**bytesToGroupPeers**</span></span>
</dt> <dd>

<span data-ttu-id="b0430-129">傳送給群組對等的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="b0430-129">Number of bytes transferred to group peers.</span></span>

</dd> <dt>

<span data-ttu-id="b0430-130">**bytesToInternetPeers**</span><span class="sxs-lookup"><span data-stu-id="b0430-130">**bytesToInternetPeers**</span></span>
</dt> <dd>

<span data-ttu-id="b0430-131">傳送至網際網路對等的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="b0430-131">Number of bytes transferred to Internet peers.</span></span>

</dd> <dt>

<span data-ttu-id="b0430-132">**HTTPConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="b0430-132">**httpConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="b0430-133">Http 連接的計數。</span><span class="sxs-lookup"><span data-stu-id="b0430-133">Count of http connections.</span></span>

</dd> <dt>

<span data-ttu-id="b0430-134">**doincConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="b0430-134">**doincConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="b0430-135">僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="b0430-135">For internal use only.</span></span>

</dd> <dt>

<span data-ttu-id="b0430-136">**lanConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="b0430-136">**lanConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="b0430-137">LAN 連接的計數。</span><span class="sxs-lookup"><span data-stu-id="b0430-137">Count of LAN connections.</span></span>

</dd> <dt>

<span data-ttu-id="b0430-138">**groupConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="b0430-138">**groupConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="b0430-139">群組連接的計數。</span><span class="sxs-lookup"><span data-stu-id="b0430-139">Count of group connections.</span></span>

</dd> <dt>

<span data-ttu-id="b0430-140">**internetConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="b0430-140">**internetConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="b0430-141">網際網路連接的計數。</span><span class="sxs-lookup"><span data-stu-id="b0430-141">Count of Internet connections.</span></span>

</dd> <dt>

<span data-ttu-id="b0430-142">**downloadDuration**</span><span class="sxs-lookup"><span data-stu-id="b0430-142">**downloadDuration**</span></span>
</dt> <dd>

<span data-ttu-id="b0430-143">檔案傳輸的持續時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b0430-143">Duration of the file transfer in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="b0430-144">**downloadMode**</span><span class="sxs-lookup"><span data-stu-id="b0430-144">**downloadMode**</span></span>
</dt> <dd>

<span data-ttu-id="b0430-145">使用的下載模式，請參閱 [**DownloadMode**](downloadmode.md)。</span><span class="sxs-lookup"><span data-stu-id="b0430-145">The download mode used, see [**DownloadMode**](downloadmode.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0430-146">**status**</span><span class="sxs-lookup"><span data-stu-id="b0430-146">**status**</span></span>
</dt> <dd>

<span data-ttu-id="b0430-147">檔案傳輸的狀態，請參閱 [**SwarmStatus**](swarmstatus.md)。</span><span class="sxs-lookup"><span data-stu-id="b0430-147">The status of a file transfer, see [**SwarmStatus**](swarmstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0430-148">**isBackground**</span><span class="sxs-lookup"><span data-stu-id="b0430-148">**isBackground**</span></span>
</dt> <dd>

<span data-ttu-id="b0430-149">如果這是背景傳送，則為 True。</span><span class="sxs-lookup"><span data-stu-id="b0430-149">True, if this is a background transfer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b0430-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0430-150">Requirements</span></span>



| <span data-ttu-id="b0430-151">需求</span><span class="sxs-lookup"><span data-stu-id="b0430-151">Requirement</span></span> | <span data-ttu-id="b0430-152">值</span><span class="sxs-lookup"><span data-stu-id="b0430-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0430-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0430-153">Minimum supported client</span></span><br/> | <span data-ttu-id="b0430-154">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0430-154">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b0430-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0430-155">Minimum supported server</span></span><br/> | <span data-ttu-id="b0430-156">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0430-156">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b0430-157">標頭</span><span class="sxs-lookup"><span data-stu-id="b0430-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0430-158"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="b0430-158"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 





