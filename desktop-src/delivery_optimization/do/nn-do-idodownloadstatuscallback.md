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
ms.openlocfilehash: 0917b73939535854469a1fe02ea89acc904cf055
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375421"
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
| **最低支援的用戶端** | \[僅限 Windows 10 版本1809的 Win32 應用程式\] |
| **最低支援的伺服器** | Windows Server，僅限1809版的 \[ Win32 應用程式\] |
| **標頭** | Do。h |