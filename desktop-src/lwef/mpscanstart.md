---
title: 'MpScanStart 函式 (MpClient) '
description: 啟動掃描工作。
ms.assetid: 3AF147C8-A41F-4193-AE28-72C1FBD18BA2
keywords:
- MpScanStart 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpScanStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d343787edc85a18dc7471d19165999a7252d18a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934643"
---
# <a name="mpscanstart-function"></a>MpScanStart 函式

啟動掃描工作。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI MpScanStart(
  _In_     MPHANDLE          hMpHandle,
  _In_     MPSCAN_TYPE       ScanType,
  _In_     DWORD             dwScanOptions,
  _In_opt_ PMPSCAN_RESOURCES pScanResources,
  _In_opt_ PMPCALLBACK_INFO  pCallbackInfo,
  _Out_    PMPHANDLE         phScanHandle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hMpHandle* \[在\]
</dt> <dd>

類型： **MPHANDLE**

惡意程式碼防護管理員介面的控制碼。 [**MpManagerOpen**](mpmanageropen.md)函數會傳回這個控制碼。

</dd> <dt>

*ScanType* \[在\]
</dt> <dd>

類型： **[ **MPSCAN \_ 類型**](mpscan-type.md)**

指定掃描的類型。 此參數必須是 [**MPSCAN \_ 類型**](mpscan-type.md) enueration 的其中一個成員。

</dd> <dt>

*dwScanOptions* \[在\]
</dt> <dd>

類型： **DWORD**

指定掃描操作的各種選項。



| 值                                                                                                                                                                                                       | 意義                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPSCAN_OPTION_NONE"></span><span id="mpscan_option_none"></span><dl> <dt>**MPSCAN \_ 選項 \_ NONE**</dt> </dl>                               | 未要求特定的選項。<br/>                                                                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_ASYNC"></span><span id="mpscan_option_async"></span><dl> <dt>**MPSCAN \_ 選項 \_ ASYNC**</dt> </dl>                            | 掃描工作是非同步，其中 **MpScanStart** 會在成功啟動掃描後立即傳回。  (預設掃描工作是同步的，這表示只有在掃描完成後才會傳回 **MpScanStart** 。 ) <br/>      |
| <span id="MPSCAN_OPTION_PROGRESS"></span><span id="mpscan_option_progress"></span><dl> <dt>**MPSCAN \_ 選項 \_ 進度**</dt> </dl>                   | 呼叫端想要透過回呼接收掃描進度資訊。<br/>                                                                                                                                                                            |
| <span id="MPSCAN_OPTION_LOWPRIORITY"></span><span id="mpscan_option_lowpriority"></span><dl> <dt>**MPSCAN \_ 選項 \_ LOWPRIORITY**</dt> </dl>          | 以低優先順序執行掃描。  (預設會以一般優先順序執行掃描工作。 ) <br/>                                                                                                                                                     |
| <span id="MPSCAN_OPTION_PACKEDEXES"></span><span id="mpscan_option_packedexes"></span><dl> <dt>**MPSCAN \_ 選項 \_ PACKEDEXES**</dt> </dl>             | 掃描封裝的可執行檔是否有可能的威脅。<br/>                                                                                                                                                                                                              |
| <span id="MPSCAN_OPTION_ARCHIVES"></span><span id="mpscan_option_archives"></span><dl> <dt>**MPSCAN \_ 選項 \_ 封存**</dt> </dl>                   | 掃描封存內容是否有可能的威脅。 封存是副檔名為 .zip、.cab 或 tar 的檔案。<br/>                                                                                                                                                |
| <span id="MPSCAN_OPTION_HEURISTICS"></span><span id="mpscan_option_heuristics"></span><dl> <dt>**MPSCAN \_ 選項 \_ 啟發學習法**</dt> </dl>             | 啟用以啟發學習法為基礎的掃描。 這會掃描偵測類型設定為啟發學習法的威脅。<br/>                                                                                                                                                        |
| <span id="MPSCAN_OPTION_REPORTFRIENDLY"></span><span id="mpscan_option_reportfriendly"></span><dl> <dt>**MPSCAN \_ 選項 \_ REPORTFRIENDLY**</dt> </dl> | 在資源掃描中報告易記專案。 這僅供內部使用。<br/>                                                                                                                                                                          |
| <span id="MPSCAN_OPTION_REPORTUNKNOWN"></span><span id="mpscan_option_reportunknown"></span><dl> <dt>**MPSCAN \_ 選項 \_ REPORTUNKNOWN**</dt> </dl>    | 在資源掃描中報告未知的專案。 這僅供內部使用。<br/>                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_NOCONSOLIDATE"></span><span id="mpscan_option_noconsolidate"></span><dl> <dt>**MPSCAN \_ 選項 \_ NOCONSOLIDATE**</dt> </dl>    | 請勿將掃描結果與全域威脅視圖合併。 這適用于用戶端 (例如，電子郵件客戶程式) 想要自行控制清理 UX，而不允許預設反惡意程式碼清理 UX。 這僅供內部使用。<br/> |



 

</dd> <dt>

*pScanResources* \[在中，選擇性\]
</dt> <dd>

類型： **PMPSCAN \_ 資源**

掃描資源資訊的指標。 此參數必須是 **Null** ，才能進行快速掃描。 這是完整掃描的選擇性參數。 若為資源掃描，必須至少使用一個資源資訊結構來指定此參數。 若要掃描特定資源，呼叫端必須具有該資源的 **一般 \_ 讀取** 許可權。 請參閱 [**MPSCAN \_ 資源**](mpscan-resources.md)。

</dd> <dt>

*pCallbackInfo* \[在中，選擇性\]
</dt> <dd>

類型： **PMPCALLBACK \_ 資訊**

用來將掃描狀態變更饋送至用戶端的回呼資訊指標 (例如開始和完成) 和進度資訊。 回呼函式中傳回的 [**MPCALLBACK \_ 資料**](mpcallback-data.md) 會報告實際的掃描狀態和進度相關資訊。 以下是可能的回呼清單：



| 值                                                                                                                                                                                                       | 意義                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span><dl> <dt>**MPNOTIFY \_ 掃描 \_ 開始**</dt> </dl>                            | 掃描工作已啟動。<br/>                                                                                                                                                                                                                                                                                       |
| <span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span><dl> <dt>**MPNOTIFY \_ 掃描 \_ 完成**</dt> </dl>                   | 掃描工作已完成。 您可以透過 [**MPSCAN \_ 資料**](mpscan-data.md) 結構取得其他資訊。<br/>                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span><dl> <dt>**MPNOTIFY \_ 掃描 \_ 暫停**</dt> </dl>                         | 掃描操作已暫停。<br/>                                                                                                                                                                                                                                                                                     |
| <span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span><dl> <dt>**MPNOTIFY \_ 掃描已 \_ 繼續**</dt> </dl>                      | 掃描工作已從暫停繼續。<br/>                                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span><dl> <dt>**MPNOTIFY \_ 掃描 \_ 取消**</dt> </dl>                         | 掃描操作已取消。<br/>                                                                                                                                                                                                                                                                                 |
| <span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span><dl> <dt>**MPNOTIFY \_ 掃描 \_ 進度**</dt> </dl>                   | 掃描進度資訊。 您可以透過 [**MPSCAN \_ 資料**](mpscan-data.md) 結構取得額外的資訊 (例如資源統計資料) 。<br/>                                                                                                                                                               |
| <span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span><dl> <dt>**MPNOTIFY \_ 掃描 \_ 錯誤**</dt> </dl>                            | 掃描特定資源的錯誤資訊。 您可以透過 [**MPSCAN \_ 資料**](mpscan-data.md) 結構取得特定的資源資訊。<br/>                                                                                                                                                             |
| <span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span><dl> <dt>**\_ \_ 受感染的 MPNOTIFY 掃描**</dt> </dl>                   | 掃描找到受感染的資源。 請注意，在大部分情況下，這會導致掃描結束時回報某些威脅。 有時候，由於排除專案的原因，可能無法具體化為威脅。 您可以透過 [**MPSCAN \_ 資料**](mpscan-data.md) 結構取得其他受感染的資源資訊。<br/> |
| <span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span><dl> <dt>**MPNOTIFY \_ 掃描 \_ MEMORYSTART**</dt> </dl>          | 完整掃描的快速掃描部分已開始。<br/>                                                                                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span><dl> <dt>**MPNOTIFY \_ 掃描 \_ MEMORYCOMPLETE**</dt> </dl> | 完整掃描的快速掃描部分已完成。<br/>                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <dt>**MPNOTIFY \_ 內部 \_ 失敗**</dt> </dl>          | 掃描工作遇到一般失敗。 [**MPCALLBACK \_ 資料**](mpcallback-data.md)中的 *hResult* 具有特定的錯誤碼。<br/>                                                                                                                                                                   |



 

</dd> <dt>

*phScanHandle* \[擴展\]
</dt> <dd>

類型： **PMPHANDLE**

傳回的掃描控制碼，識別目前起始的掃描。 這個控制碼可用於後續的函式呼叫，例如取出掃描結果。 控制碼必須使用 [**MpHandleClose**](mphandleclose.md) 函式來關閉。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果函式成功，則傳回值為 **S \_ OK**。

如果函式失敗，則傳回值會是失敗的 **HRESULT** 程式碼。 呼叫端可以使用 [**MpErrorMessageFormat**](mperrormessageformat.md) 函數來取得錯誤訊息的一般描述。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                    |
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

[**MPCALLBACK \_ 資料**](mpcallback-data.md)
</dt> <dt>

[**MPSCAN \_ 資料**](mpscan-data.md)
</dt> <dt>

[**MPSCAN \_ 資源**](mpscan-resources.md)
</dt> <dt>

[**MPSCAN \_ 類型**](mpscan-type.md)
</dt> </dl>

 

 





