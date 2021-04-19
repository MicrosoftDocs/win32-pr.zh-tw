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
# <a name="doswarmstats-structure"></a>DOSwarmStats 結構

包含用來下載和上傳檔案之統計資料的欄位。

## <a name="syntax"></a>語法


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



## <a name="members"></a>成員

<dl> <dt>

**fileId**
</dt> <dd>

以 **AddFileWithRanges** 呼叫所指定之以 Null 結束的字串。

</dd> <dt>

**sourceURL**
</dt> <dd>

以 Null 終止的字串，其中包含伺服器上的檔案名 (例如，HTTPs:// &lt; server &gt; / &lt; path &gt; /file.ext) 。

</dd> <dt>

**fileSize**
</dt> <dd>

檔案大小，以位元組為單位。

</dd> <dt>

**totalBytesDownloaded**
</dt> <dd>

傳送的位元組總數。

</dd> <dt>

**bytesFromLanPeers**
</dt> <dd>

從 LAN 對等傳送的位元組數目。

</dd> <dt>

**bytesFromGroupPeers**
</dt> <dd>

從群組對等傳輸的位元組數目。

</dd> <dt>

**bytesFromInternetPeers**
</dt> <dd>

從網際網路對等傳送的位元組數目。

</dd> <dt>

**bytesFromHttp**
</dt> <dd>

從 HTTP 傳輸的位元組數目。

</dd> <dt>

**bytesFromDoinc**
</dt> <dd>

僅供內部使用。

</dd> <dt>

**bytesToLanPeers**
</dt> <dd>

傳送至 LAN 對等的位元組數目。

</dd> <dt>

**bytesToGroupPeers**
</dt> <dd>

傳送給群組對等的位元組數目。

</dd> <dt>

**bytesToInternetPeers**
</dt> <dd>

傳送至網際網路對等的位元組數目。

</dd> <dt>

**HTTPConnectionCount**
</dt> <dd>

Http 連接的計數。

</dd> <dt>

**doincConnectionCount**
</dt> <dd>

僅供內部使用。

</dd> <dt>

**lanConnectionCount**
</dt> <dd>

LAN 連接的計數。

</dd> <dt>

**groupConnectionCount**
</dt> <dd>

群組連接的計數。

</dd> <dt>

**internetConnectionCount**
</dt> <dd>

網際網路連接的計數。

</dd> <dt>

**downloadDuration**
</dt> <dd>

檔案傳輸的持續時間（以毫秒為單位）。

</dd> <dt>

**downloadMode**
</dt> <dd>

使用的下載模式，請參閱 [**DownloadMode**](downloadmode.md)。

</dd> <dt>

**status**
</dt> <dd>

檔案傳輸的狀態，請參閱 [**SwarmStatus**](swarmstatus.md)。

</dd> <dt>

**isBackground**
</dt> <dd>

如果這是背景傳送，則為 True。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl> |



 

 





