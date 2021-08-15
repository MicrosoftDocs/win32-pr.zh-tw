---
title: 'MpThreatOpen 函式 (MpClient) '
description: 針對取得威脅的目的，傳回列舉控制碼。
ms.assetid: E1178F0C-E9C0-4532-AE9B-452770600DF2
keywords:
- MpThreatOpen 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpThreatOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 949fd1c8291ecb183cf51cf5385fe356a33cb1288978fda42f37d748f1a162a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746887"
---
# <a name="mpthreatopen-function"></a>MpThreatOpen 函式

針對取得威脅的目的，傳回列舉控制碼。 這項功能可用來開啟特定掃描偵測到的威脅、系統中的所有作用中威脅、威脅消毒的歷程記錄，或簽章資料庫中出現的所有威脅。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI MpThreatOpen(
  _In_  MPHANDLE        hScanHandle,
  _In_  MPTHREAT_SOURCE ThreatSource,
  _In_  MPTHREAT_TYPE   ThreatType,
  _Out_ PMPHANDLE       phThreatEnumHandle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hScanHandle* \[在\]
</dt> <dd>

類型： **MPHANDLE**

可以是 [**MpScanStart**](mpscanstart.md) 函式所傳回之已完成掃描工作的控制碼。 或者，您可以將此參數設定為 [**MpManagerOpen**](mpmanageropen.md) 所傳回的 malware protection manager 介面控制碼，以列舉系統中的所有作用中威脅、威脅消毒的歷程記錄，或簽章資料庫中的威脅。

</dd> <dt>

*ThreatSource* \[在\]
</dt> <dd>

類型： **MPTHREAT \_ 來源**

用來控制威脅列舉的來源。 此參數的可能值為：



| 值                                                                                                                                                                                                 | 意義                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_SOURCE_SCAN"></span><span id="mpthreat_source_scan"></span><dl> <dt>**MPTHREAT \_ 來源 \_ 掃描**</dt> </dl>                   | 與特定掃描控制碼相關聯的威脅。<br/>                                              |
| <span id="MPTHREAT_SOURCE_ACTIVE"></span><span id="mpthreat_source_active"></span><dl> <dt>**MPTHREAT \_ 來源 \_ 有效**</dt> </dl>             | 系統中目前作用中的威脅。<br/>                                                        |
| <span id="MPTHREAT_SOURCE_HISTORY"></span><span id="mpthreat_source_history"></span><dl> <dt>**MPTHREAT \_ 來源歷程 \_ 記錄**</dt> </dl>          | 以歷程記錄方式處理和保留的威脅。<br/>                                                 |
| <span id="MPTHREAT_SOURCE_QUARANTINE"></span><span id="mpthreat_source_quarantine"></span><dl> <dt>**MPTHREAT \_ 來源 \_ 隔離**</dt> </dl> | 已隔離的威脅。<br/>                                                                           |
| <span id="MPTHREAT_SOURCE_SIGNATURE"></span><span id="mpthreat_source_signature"></span><dl> <dt>**MPTHREAT \_ 來源簽章 \_**</dt> </dl>    | 可以使用目前的簽章資料庫偵測到的威脅。<br/>                                |
| <span id="MPTHREAT_SOURCE_STATE"></span><span id="mpthreat_source_state"></span><dl> <dt>**MPTHREAT \_ 來源 \_ 狀態**</dt> </dl>                | 最近所採取的威脅。  ( 「最近」是由可設定的內部設定所定義。 ) <br/> |



 

</dd> <dt>

*ThreatType* \[在\]
</dt> <dd>

類型： **MPTHREAT \_ 類型**

用來根據偵測類型篩選列舉的威脅。 此參數的可能值為：



| 值                                                                                                                                                                                           | 意義                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span><dl> <dt>**MPTHREAT \_ 類型 \_ KNOWNBAD**</dt> </dl>       | 偵測是根據特定的簽章、模擬或其他威脅偵測方法來執行。<br/> |
| <span id="MPTHREAT_TYPE_SUSPICIOUS"></span><span id="mpthreat_type_suspicious"></span><dl> <dt>**MPTHREAT \_ 類型 \_ 可疑**</dt> </dl> | 偵測是根據行為監視來執行。<br/>                                               |
| <span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span><dl> <dt>**未知的 MPTHREAT \_ 類型 \_**</dt> </dl>          | 偵測是根據 (非分類) 的未知威脅來執行。<br/>                                    |
| <span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span><dl> <dt>**MPTHREAT \_ 類型 \_ KNOWNGOOD**</dt> </dl>    | 偵測是根據已知的安全威脅來執行。<br/>                                                |
| <span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span><dl> <dt>**MPTHREAT \_ 類型 \_ NIS**</dt> </dl>                      | 偵測是根據 NIS 威脅執行。<br/>                                                       |



 

</dd> <dt>

*phThreatEnumHandle* \[擴展\]
</dt> <dd>

類型： **PMPHANDLE**

傳回識別列舉內容的威脅列舉控制碼。 您可以使用此控制碼來列舉使用 [**MpThreatEnumerate**](mpthreatenumerate.md)的威脅資訊。 控制碼必須使用 [**MpHandleClose**](mphandleclose.md) 函式來關閉。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果函式成功，則傳回值為 **S \_ OK**。

如果函式失敗，則傳回值會是失敗的 **HRESULT** 程式碼。 呼叫端可以使用 [**MpErrorMessageFormat**](mperrormessageformat.md) 函數來取得錯誤訊息的一般描述。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpHandleClose**](mphandleclose.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**MpScanStart**](mpscanstart.md)
</dt> <dt>

[**MpThreatEnumerate**](mpthreatenumerate.md)
</dt> </dl>

 

 





