---
title: DODownloadProperty 列舉
description: 指定「進行下載」作業的屬性識別碼。
keywords:
- DODownloadProperty 列舉，DODownloadProperty
topic_type:
- apiref
api_name:
- DODownloadProperty
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: bb8ec6ad8cc55239522f953c6a81a8bf7b2b62ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105335"
---
# <a name="dodownloadproperty-enumeration"></a>DODownloadProperty 列舉

**DODownloadProperty** 列舉會指定 DO 下載作業的屬性識別碼。 此列舉是由 **IDODownload** 介面所使用，並由變數值執行，其中包含值的型別。

## <a name="syntax"></a>Syntax

```cpp
typedef enum _DODownloadProperty
{
  DODownloadProperty_Id = 0,
  DODownloadProperty_Uri,
  DODownloadProperty_ContentId,
  DODownloadProperty_DisplayName,
  DODownloadProperty_LocalPath,
  DODownloadProperty_HttpCustomHeaders,
  DODownloadProperty_CostPolicy,
  DODownloadProperty_SecurityFlags,
  DODownloadProperty_CallbackFreqPercent,
  DODownloadProperty_CallbackFreqSeconds,
  DODownloadProperty_NoProgressTimeoutSeconds,
  DODownloadProperty_ForegroundPriority,
  DODownloadProperty_BlockingMode,
  DODownloadProperty_CallbackInterface,
  DODownloadProperty_StreamInterface,
  DODownloadProperty_SecurityContext,
  DODownloadProperty_NetworkToken
  DODownloadProperty_CorrelationVector,
  DODownloadProperty_DecryptionInfo,
  DODownloadProperty_IntegrityCheckInfo,
  DODownloadProperty_IntegrityCheckMandatory,
  DODownloadProperty_TotalSizeBytes
} DODownloadProperty;
```

## <a name="constants"></a>常數

| 需求 | 值 |
|-|-|
| DODownloadProperty_Id | 唯讀。 您可以使用這個屬性來取得可唯一識別下載的識別碼。 VARIANT 類型為 VT_BSTR。 |
| DODownloadProperty_Uri | 您可以使用這個屬性來設定或取得要下載之資源的遠端 URI 路徑。 只有在未提供 *DODownloadProperty_ContentId* 時，才需要此屬性。 VARIANT 類型為 VT_BSTR。 |
| DODownloadProperty_ContentId | 您可以使用這個屬性來設定或取得下載唯一的內容識別碼。 只有在未提供 *DODownloadProperty_Uri* 時，才需要此屬性。 VARIANT 類型為 VT_BSTR。 |
| DODownloadProperty_DisplayName | 選擇性。 您可以使用這個屬性來設定或取得下載顯示名稱。 VARIANT 類型為 VT_BSTR。 |
| DODownloadProperty_LocalPath | 您可以使用這個屬性來設定或取得本機路徑名稱，以儲存下載檔案。 如果路徑不存在，則會嘗試在呼叫端的許可權下建立它。 只有在未提供 *DODownloadProperty_StreamInterface* 時，才需要這個屬性。 VARIANT 類型為 VT_BSTR。 |
| DODownloadProperty_HttpCustomHeaders | 選擇性。 您可以使用這個屬性來設定或取得自訂 HTTP 要求標頭。 在 HTTP 檔案要求作業期間，將會包含這些標頭。 標頭必須已經格式化為標準 HTTP 標頭。 VARIANT 類型為 VT_BSTR。 |
| DODownloadProperty_CostPolicy | 選擇性。 您可以使用這個屬性來設定或取得其中一個 **DODownloadCostPolicy** 列舉值。 VARIANT 類型為 VT_UI4。 |
| DODownloadProperty_SecurityFlags | 選擇性只寫入。 您可以使用這個屬性來設定或取得標準的 WinHTTP 安全性旗標 (**WINHTTP_OPTION_SECURITY_FLAGS**) 。 VARIANT 類型為 VT_UI4。</br></br>以下是支援的旗標：</br>SECURITY_FLAG_IGNORE_CERT_CN_INVALID。 允許憑證中有不正確一般名稱。</br>SECURITY_FLAG_IGNORE_CERT_DATE_INVALID。 允許不正確憑證日期。</br>SECURITY_FLAG_IGNORE_UNKNOWN_CA。 允許不正確憑證授權單位單位。</br>SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE。 允許以非伺服器憑證建立伺服器的身分識別。</br>WINHTTP_ENABLE_SSL_REVOCATION。 允許 SSL 撤銷。 如果設定此旗標，則會忽略上述旗標。 |
| DODownloadProperty_CallbackFreqPercent | 選擇性。 您可以使用這個屬性來設定或取得以下載百分比為基礎的回呼頻率。 VARIANT 類型為 VT_UI4。 |
| DODownloadProperty_CallbackFreqSeconds | 選擇性。 您可以使用這個屬性來設定或取得以下載時間為基礎的回呼頻率。 預設值為每秒一次。 VARIANT 類型為 VT_UI4。 |
| DODownloadProperty_NoProgressTimeoutSeconds | 選擇性。 您可以使用這個屬性來設定或取得沒有進度的下載超時時間長度。 接受的最小值為60秒（沒有下載活動）。 VARIANT 類型為 VT_UI4。 |
| DODownloadProperty_ForegroundPriority | 選擇性。 您可以使用這個屬性來設定或取得目前的下載優先順序。 VARIANT_TRUE 值會將下載帶到較高優先順序的前景。 預設為背景優先權。 VARIANT 類型為 VT_BOOL。 |
| DODownloadProperty_BlockingMode | 選擇性。 您可以使用這個屬性來設定或取得目前的下載封鎖模式。 VARIANT_TRUE 值會導致 **IDODownload：： Start** 封鎖直到下載完成或發生錯誤。 預設值為非封鎖模式。 VARIANT 類型為 VT_BOOL。 |
| DODownloadProperty_CallbackInterface | 選擇性。 您可以使用這個屬性來設定或取得用於下載回呼的 **IDODownloadStatusCallback** 介面指標。 VARIANT 類型為 VT_UNKNOWN。 |
| DODownloadProperty_StreamInterface | 選擇性。 您可以使用這個屬性來設定或取得用於資料流程下載類型的 IStream 介面指標。 VARIANT 類型為 VT_UNKNOWN。 |
| DODownloadProperty_SecurityCoNtext | 選擇性只寫入。 您可以使用這個屬性來設定要在 HTTP 要求作業期間使用的憑證內容。 值必須由 CERT_CONTEXT 的序列化位元組組成。 VARIANT 類型是 (VT_ARRAY \| VT_UI1) 。 |
| DODownloadProperty_NetworkToken | 選擇性只寫入。 您可以使用這個屬性來設定要在 HTTP 作業期間使用的網路權杖。 VARIANT_TRUE 值會導致捕捉呼叫端的身分識別權杖，VARIANT_FALSE 將會清除現有的權杖。 預設值是已登入使用者的標記。 VARIANT 類型為 VT_BOOL。 |
| DODownloadProperty_CorrelationVector | 選擇性。 針對遙測用途設定特定的相互關聯向量。 VARIANT 類型為 VT_BSTR。 |
| DODownloadProperty_DecryptionInfo | 選擇性只寫入。 以 JSON 字串的形式設定解密資訊。 VARIANT 類型為 VT_BSTR。 |
| DODownloadProperty_IntegrityCheckInfo | 選擇性只寫入。 設定 (PHF) 位置的片段雜湊檔，這會用來執行所下載內容的執行時間完整性檢查。 VARIANT 類型為 VT_BSTR。 |
| DODownloadProperty_IntegrityCheckMandatory | 選擇性。 設定布林值旗標，指出部分雜湊檔 (PHF) 是否為強制性。 如果 VARIANT_TRUE，則會在完整性檢查失敗時中止下載。 VARIANT 類型為 VT_BOOL。 |
| DODownloadProperty_TotalSizeBytes | 選擇性。 指定下載大小總計（以位元組為單位）。 VARIANT 類型為 VT_UI8。 |

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | \[僅限 Windows 10 版本1809的 Win32 應用程式\] |
| **最低支援的伺服器** | Windows Server，僅限1809版的 \[ Win32 應用程式\] |
| **標頭** | DeliveryOptimizationDownloadTypes。h |
