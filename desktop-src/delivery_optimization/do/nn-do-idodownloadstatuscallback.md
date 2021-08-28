---
title: IDODownloadStatusCallback 介面
description: 用來接收有關下載的通知。
keywords:
- IDODownloadStatusCallback 介面
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: d91ff44e3b4f4247983ec81d53257347c8bcfa523f85855dcd0d37074f4b38fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498948"
---
# <a name="idodownloadstatuscallback-interface"></a>IDODownloadStatusCallback 介面

**IDODownloadStatusCallback** 介面可用來接收有關下載的通知。

## <a name="methods"></a>方法

**IDODownloadStatusCallback** 介面具有這些方法。

| 方法 | 描述 |
| ---- |:---- |
| [IDODownloadStatusCallback::OnStatusChanged](./nf-do-idodownloadstatuscallback-onstatuschanged.md) | 只要下載狀態變更，就會呼叫此方法的執行。 |

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | Windows 10 版本 1809 \[僅限 Win32 應用程式\] |
| **最低支援的伺服器** | WindowsServer，僅限1809版的 \[ Win32 應用程式\] |
| **標頭** | Do。h |