---
title: DODownloadPropertyEx 列舉
description: 指定「進行下載」作業的擴充屬性識別碼。
keywords:
- DODownloadPropertyEx 列舉，DODownloadPropertyEx
topic_type:
- apiref
api_name:
- DODownloadPropertyEx
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 5df0f53778d9059ef8767f5b8052940847e36c00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843716"
---
# <a name="dodownloadpropertyex-enumeration"></a>DODownloadPropertyEx 列舉

> [!IMPORTANT]
> **DODownloadPropertyEx** 列舉已被取代。 相反地，請使用 [DODownloadProperty](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) 列舉搭配 [IDODownload：： GetProperty](../do/nf-do-idodownload-getproperty.md) 和 [IDODownload：： SetProperty](../do/nf-do-idodownload-setproperty.md)。

**DODownloadPropertyEx** 列舉會指定 DO 下載作業的擴充屬性識別碼。 這個列舉是由 **IDODownloadInternal** 介面使用，而 **變數** 值則是用來取得和設定屬性值。

## <a name="syntax"></a>Syntax

```cpp
typedef enum _DODownloadPropertyEx
{
  DODownloadPropertyEx_UpdateId = 0,
  DODownloadPropertyEx_CorrelationVector,
  DODownloadPropertyEx_DecryptionInfo,    
  DODownloadPropertyEx_IntegrityCheckInfo,   
  DODownloadPropertyEx_IntegrityCheckMandatory, 
  DODownloadPropertyEx_TotalSizeBytes, 
  DODownloadPropertyEx_TempLocalFileUsage 
} DODownloadPropertyEx;
```
## <a name="constants"></a>常數

| 需求 | 值 |
|-|-|
| DODownloadPropertyEx_UpdateId | 保留的。 請勿使用。 |
| DODownloadPropertyEx_CorrelationVector | 選擇性。 針對遙測用途設定特定的相互關聯向量。 VARIANT 類型為 VT_BSTR。 |
| DODownloadPropertyEx_DecryptionInfo | 保留的。 請勿使用。 |
| DODownloadPropertyEx_IntegrityCheckInfo | 選擇性只寫入。 設定 (PHF) 位置的片段雜湊檔，這會用來執行所下載內容的執行時間完整性檢查。 VARIANT 類型為 VT_BSTR。 |
| DODownloadPropertyEx_IntegrityCheckMandatory | 選擇性。 設定布林值旗標，指出部分雜湊檔 (PHF) 是否為強制性。 如果 VARIANT_TRUE，當完整性檢查失敗時，將會中止下載。 VARIANT 類型為 VT_BOOL。 |
| DODownloadPropertyEx_TotalSizeBytes | 保留的。 請勿使用。 |
| DODownloadPropertyEx_TempLocalFileUsage | 保留的。 請勿使用。 |

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | \[僅限 Windows 10 版本1809的 Win32 應用程式\] |
| **最低支援的伺服器** | Windows Server，僅限1809版的 \[ Win32 應用程式\] |
| **標頭** | DODownloadInternal。h |
