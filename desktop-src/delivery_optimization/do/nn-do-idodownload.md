---
title: IDODownload 介面
description: 用來啟動及管理下載。
keywords:
- IDODownload 介面
topic_type:
- apiref
api_name:
- IDODownload
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: ec2f74ce7daae6f612297d21e15e6993fcd78382
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315262"
---
# <a name="idodownload-interface"></a>IDODownload 介面

**IDODownload** 介面可用來啟動及管理下載。

## <a name="methods"></a>方法

**IDODownload** 介面具有這些方法。

| 方法 | 描述 |
| ---- |:---- |
| [IDODownload：： Abort](./nf-do-idomanager-createdownload.md) | 中止下載。 |
| [IDODownload：： Finalize](./nf-do-idodownload-finalize.md) | 完成下載。 |
| [IDODownload：： GetProperty](./nf-do-idodownload-getproperty.md) | 抓取包含特定下載屬性之 **變數** 的指標。 |
| [IDODownload：： GetStatus](./nf-do-idodownload-getstatus.md) | 抓取 **DO_DOWNLOAD_STATUS** 結構的指標，此結構會反映下載的目前狀態。 |
| [IDODownload：:P ause](./nf-do-idodownload-pause.md) | 暫停下載。 |
| [IDODownload：： SetProperty](./nf-do-idodownload-setproperty.md) | 設定下載屬性。 |
| [IDODownload：： Start](./nf-do-idodownload-start.md) | 啟動或繼續進行下載。 |

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | \[僅限 Windows 10 版本1809的 Win32 應用程式\] |
| **最低支援的伺服器** | Windows Server，僅限1809版的 \[ Win32 應用程式\] |
| **標頭** | Do。h |