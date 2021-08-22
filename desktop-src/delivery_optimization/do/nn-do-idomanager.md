---
title: IDOManager 介面
description: 用來建立新的下載，以及列舉現有的下載。
keywords:
- IDOManager 介面
topic_type:
- apiref
api_name:
- IDOManager
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 5fff72067c69345a9852718c377b179d16f398c0eb3b84c73ca82c3af1b08a71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047086"
---
# <a name="idomanager-interface"></a>IDOManager 介面

**IDOManager** 介面可用來建立新的下載，以及列舉現有的下載。

## <a name="methods"></a>方法

**IDOManager** 介面具有這些方法。

| 方法 | 描述 |
| ---- |:---- |
| [IDOManager::CreateDownload](./nf-do-idomanager-createdownload.md) | 建立新的下載。 |
| [IDOManager::EnumDownloads](./nf-do-idomanager-enumdownloads.md) | 抓取列舉值物件的介面指標，此列舉值物件是用來列舉現有的下載。 |

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | Windows 10 版本 1809 \[僅限 Win32 應用程式\] |
| **最低支援的伺服器** | WindowsServer，僅限1809版的 \[ Win32 應用程式\] |
| **標頭** | Do。h |