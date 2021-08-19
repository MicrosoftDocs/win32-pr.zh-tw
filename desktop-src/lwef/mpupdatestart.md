---
title: 'MpUpdateStart 函式 (MpClient) '
description: 開始簽名更新作業。
ms.assetid: BB056356-17E5-42F0-9636-9E1C254361E4
keywords:
- MpUpdateStart 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpUpdateStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a61cda213ecfbb23c9ef366fcce7b5c91e806f26f0f4ebe8b45dc596b63d1b5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975888"
---
# <a name="mpupdatestart-function"></a>MpUpdateStart 函式

開始簽名更新作業。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI MpUpdateStart(
  _In_     MPHANDLE         hMpHandle,
  _In_     DWORD            dwUpdateOptions,
  _In_opt_ PMPCALLBACK_INFO pCallbackInfo,
  _Out_    PMPHANDLE        phUpdateHandle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hMpHandle* \[在\]
</dt> <dd>

類型： **MPHANDLE**

惡意程式碼防護管理員介面的控制碼。 [**MpManagerOpen**](mpmanageropen.md)函數會傳回這個控制碼。

</dd> <dt>

*dwUpdateOptions* \[在\]
</dt> <dd>

類型： **DWORD**

指定簽章更新作業的選項。 它可能是下列其中一個值：



| 值                                                                                                                                                                                              | 意義                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPUPDATE_OPTION_NONE"></span><span id="mpupdate_option_none"></span><dl> <dt>**MPUPDATE \_ 選項 \_ NONE**</dt> </dl>                | 未要求特定的選項。<br/>                                                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_ASYNC"></span><span id="mpupdate_option_async"></span><dl> <dt>**MPUPDATE \_ 選項 \_ ASYNC**</dt> </dl>             | 更新作業是非同步，在此情況下， **MpUpdateStart** 會在成功初始化簽章更新之後立即傳回。  (根據預設，更新作業是同步的，這表示只有在簽章更新完成後才會傳回 **MpUpdateStart** 。 ) <br/> |
| <span id="MPUPDATE_OPTION_PROGRESS"></span><span id="mpupdate_option_progress"></span><dl> <dt>**MPUPDATE \_ 選項 \_ 進度**</dt> </dl>    | 呼叫端想要透過回呼接收簽章更新進度資訊。<br/>                                                                                                                                                                                           |
| <span id="MPUPDATE_OPTION_HTTP"></span><span id="mpupdate_option_http"></span><dl> <dt>**MPUPDATE \_ 選項 \_ HTTP**</dt> </dl>                | 您可以從 Microsoft security 入口網站下載完整的簽章套件來執行簽章更新。 如果用戶端透過 Microsoft Update 遇到簽章下載問題，則可以使用此選項做為回復選項。<br/>                                           |
| <span id="MPUPDATE_OPTION_UNC"></span><span id="mpupdate_option_unc"></span><dl> <dt>**MPUPDATE \_ 選項 \_ UNC**</dt> </dl>                   | 使用 UNC 共用的直接下載來執行簽章更新。<br/>                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_MANAGED"></span><span id="mpupdate_option_managed"></span><dl> <dt>**MPUPDATE \_ 選項 \_ 管理**</dt> </dl>       | 使用受管理的服務 WSUS 執行簽章更新。<br/>                                                                                                                                                                                                                             |
| <span id="MPUPDATE_OPTION_UNMANAGED"></span><span id="mpupdate_option_unmanaged"></span><dl> <dt>**\_ \_ 未受管理的 MPUPDATE 選項**</dt> </dl> | 使用非受控服務 MU/WU 執行簽章更新。<br/>                                                                                                                                                                                                                          |



 

</dd> <dt>

*pCallbackInfo* \[在中，選擇性\]
</dt> <dd>

類型： **PMPCALLBACK \_ 資訊**

用來以簽章更新狀態變更饋送用戶端的回呼資訊指標 (例如開始和完成) 和進度資訊。 回呼函數中傳回的 [**MPCALLBACK \_ 資料**](mpcallback-data.md) 會報告實際的更新狀態和進度相關資訊。 以下是可能的回呼清單：



| 值                                                                                                                                                                                                                                | 意義                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ 開始**</dt> </dl>                                      | 更新作業已啟動。<br/>                                                                                                                                  |
| <span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ 完成**</dt> </dl>                             | 更新作業已完成。<br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ 搜尋 \_ 開始**</dt> </dl>                | 開始搜尋更新。<br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ 搜尋 \_ 完成**</dt> </dl>       | 搜尋已完成的更新。 您可以透過 [**MPSIGUPDATE \_ 資料**](mpsigupdate-data.md) 結構取得其他資訊。<br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ 下載 \_ 開始**</dt> </dl>          | 已開始更新下載。<br/>                                                                                                                               |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ 下載 \_ 進度**</dt> </dl> | 下載進度資訊。 您可以透過 [**MPSIGUPDATE \_ 資料**](mpsigupdate-data.md) 結構取得其他資訊。<br/>                            |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ 下載 \_ 完成**</dt> </dl> | 下載更新完成。 您可以透過 [**MPSIGUPDATE \_ 資料**](mpsigupdate-data.md) 結構取得其他資訊。<br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ 安裝 \_ 開始**</dt> </dl>             | 已開始安裝更新。<br/>                                                                                                                            |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ 安裝 \_ 進度**</dt> </dl>    | 安裝進度資訊。 您可以透過 [**MPSIGUPDATE \_ 資料**](mpsigupdate-data.md) 結構取得其他資訊。<br/>                        |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ 安裝 \_ 完成**</dt> </dl>    | 已完成安裝更新。 您可以透過 [**MPSIGUPDATE \_ 資料**](mpsigupdate-data.md) 結構取得其他資訊。<br/>                         |
| <span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span><dl> <dt>**已 \_ 處理 MPNOTIFY SIGUPDATE \_ 要求 \_**</dt> </dl> | 反惡意程式碼服務已處理簽名更新要求。 [**MPCALLBACK \_ 資料**](mpcallback-data.md)中的 *hResult* 會指出失敗或成功。<br/> |
| <span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span><dl> <dt>**\_ \_ 需要重新開機 MPNOTIFY SIGUPDATE \_**</dt> </dl>       | 需要重新開機才能完成更新作業。 [**MPCALLBACK \_ 資料**](mpcallback-data.md)中的 *hResult* 會指出失敗或成功。<br/>             |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <dt>**MPNOTIFY \_ 內部 \_ 失敗**</dt> </dl>                                   | 簽章更新作業遇到一般失敗。 [**MPCALLBACK \_ 資料**](mpcallback-data.md)中的 *hResult* 具有特定的錯誤碼。<br/>    |



 

</dd> <dt>

*phUpdateHandle* \[擴展\]
</dt> <dd>

類型： **PMPHANDLE**

傳回的更新控制碼，識別目前起始的簽章更新作業。 這個控制碼可用於後續的函式呼叫，例如控制簽章更新作業。 控制碼必須使用 [**MpHandleClose**](mphandleclose.md) 函式來關閉。

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

[**MPCALLBACK \_ 資料**](mpcallback-data.md)
</dt> <dt>

[**MPSIGUPDATE \_ 資料**](mpsigupdate-data.md)
</dt> </dl>

 

 





