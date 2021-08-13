---
title: DO_DOWNLOAD_STATUS 結構
description: 用來取得特定下載的狀態。
keywords:
- DO_DOWNLOAD_STATUS 結構
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_STATUS
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 8775b7daf55d58698d00bcaa2820b909e302933c9f407d1cb6416d6b095a872b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543732"
---
# <a name="do_download_status-structure"></a>DO_DOWNLOAD_STATUS 結構

**DO_DOWNLOAD_STATUS** 結構是用來取得特定下載的狀態。 它是透過呼叫 **IDODownload：： GetStatus** 函數來取得。

## <a name="syntax"></a>語法
```cpp
typedef struct _DO_DOWNLOAD_STATUS
{
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  DODownloadState State;
  HRESULT Error;
  HRESULT ExtendedError;
} DO_DOWNLOAD_STATUS;
```

## <a name="members"></a>成員

`BytesTotal`

要下載的總位元組數。

`BytesTransferred`

已下載的位元組數目。

`State`

**DODownloadState** 列舉所定義的目前下載狀態。

`Error`

如果 () 存在與目前下載相關聯的錯誤資訊，則為錯誤資訊。

`ExtendedError`

擴充的錯誤資訊 (如果存在於與目前下載相關聯的) 。

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | Windows 10 版本 1809 \[僅限 Win32 應用程式\] |
| **最低支援的伺服器** | WindowsServer，僅限1809版的 \[ Win32 應用程式\] |
| **標頭** | Do。h |
