---
title: 'DeliveryOptimizationFileProperty 列舉 (>deliveryoptimization) '
description: DeliveryOptimizationFileProperty 列舉會指定 DO 檔案的選擇性屬性識別碼。
keywords:
- DeliveryOptimizationFileProperty 列舉
topic_type:
- apiref
api_name:
- DeliveryOptimizationFileProperty
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 238ad815149f7d40dd1902b991608e0a3005eb35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969777"
---
# <a name="deliveryoptimizationfileproperty-enumeration"></a>DeliveryOptimizationFileProperty 列舉

DeliveryOptimizationFileProperty 列舉會指定 DO 檔案的選擇性屬性識別碼。 此列舉會在 IDeliveryOptimizationFile2 介面中使用，其中類型為 VARIANT 的屬性值已傳遞

## <a name="syntax"></a>Syntax

```C++
typedef enum _DeliveryOptimizationFileProperty {  
  DOFilePropertyId_DecryptionInfo,
  DOFilePropertyId_IntegrityCheckInfo,
  DOFilePropertyId_IntegrityCheckMandatory,
  DOFilePropertyId_DownloadSinkInterface,
  DOFilePropertyId_DownloadSinkFilePath,
  DOFilePropertyId_DownloadSinkMemoryStream,
  DOFilePropertyId_TotalSizeBytes
} DOFilePropertyId;
```

## <a name="constants"></a>常數

<dl> <dt>

DOFilePropertyId_DecryptionInfo
</dt> <dd>

DOFilePropertyId_DecryptionInfo 屬性識別碼會以 JSON 字串的形式來設定解密資訊。 DOFilePropertyId_DecryptionInfo 是 VT_BSTR 類型的僅限寫入屬性。

</dd> <dt>

DOFilePropertyId_IntegrityCheckInfo
</dt> <dd>

DOFilePropertyId_IntegrityCheckInfo 屬性識別碼會將片段雜湊檔設定 (PHF) 位置，以供執行以針對下載的內容執行執行時間完整性檢查。 DOFilePropertyId_IntegrityCheckInfo 是 VT_BSTR 類型的僅限寫入屬性。

</dd> <dt>

DOFilePropertyId_IntegrityCheckMandatory
</dt> <dd>

DOFilePropertyId_IntegrityCheckMandatory 屬性識別碼會設定布林值旗標，指出 PHF 的使用是否為強制性。 若為 TRUE，當完整性檢查失敗時，將會中止下載。 DOFilePropertyId_IntegrityCheckMandatory 是 VT_BOOL 類型的讀取/寫入屬性。

</dd> <dt>

DOFilePropertyId_DownloadSinkFilePath
</dt> <dd>

DOFilePropertyId_DownloadSinkFilePath 屬性識別碼會設定要在其中儲存所下載元件的完整檔案系統位置。 DOFilePropertyId_DownloadSinkFilePath 的類型 VT_BSTR。

</dd> <dt>

DOFilePropertyId_DownloadSinkMemoryStream
</dt> <dd>

DOFilePropertyId_DownloadSinkMemoryStream 屬性識別碼已被取代。 請勿使用。

</dd> <dt>

DOFilePropertyId_TotalSizeBytes
</dt> <dd>

DOFilePropertyId_TotalSizeBytes 屬性識別碼會指定下載大小總計。 DOFilePropertyId_TotalSizeBytes 的類型 VT_UI8。
</dd> </dl>

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------|----------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1803版桌面應用程式\]<br/>      |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>  |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl>               |
