---
title: IDODownloadInternal 介面
description: 用來取得或設定擴充的下載屬性。
keywords:
- IDODownloadInternal 介面
topic_type:
- apiref
api_name:
- IDODownloadInternal
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 89dcf0e397e9761c1b156a4ad4b245209cf50020
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092975"
---
# <a name="idodownloadinternal-interface"></a>IDODownloadInternal 介面

> [!IMPORTANT]
> **IDODownloadInternal** 介面已被取代。 請改用 [IDODownload](../do/nn-do-idodownload.md) 介面。

**IDODownloadInternal** 介面可用來取得或設定擴充的下載屬性。

## <a name="methods"></a>方法

**IDODownloadInternal** 介面具有這些方法。

| 方法 | 描述 |
| ---- |:---- |
| [IDODownloadInternal::GetPropertyEx](./nf-dodownloadinternal-idodownloadinternal-getpropertyex.md) | 抓取包含特定延伸下載屬性值之 **變數** 的指標。 |
| [IDODownloadInternal::SetPropertyEx](./nf-dodownloadinternal-idodownloadinternal-setpropertyex.md) | 設定延伸的下載屬性。 方法會接受 **VARIANT** 的指標，其中包含要套用至下載的特定屬性值。 |

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | \[僅限 Windows 10 版本1809的 Win32 應用程式\] |
| **最低支援的伺服器** | Windows Server，僅限1809版的 \[ Win32 應用程式\] |
| **標頭** | DODownloadInternal。h |