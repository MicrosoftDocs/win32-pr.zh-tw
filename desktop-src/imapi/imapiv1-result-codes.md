---
title: 'IMAPIv1 結果碼 (Imapierror .h) '
description: 如果方法成功，IMAPI.EXE 介面的方法會傳回 S \_ OK。 否則，它們會傳回下列其中一個結果碼。
ms.assetid: 0143ad10-9b65-4621-9bed-71dadd38c3fc
topic_type:
- apiref
api_name:
- IMAPI_S_PROPERTIESIGNORED
- IMAPI_S_BUFFER_TO_SMALL
- IMAPI_E_NOTOPENED
- IMAPI_E_NOTINITIALIZED
- IMAPI_E_USERABORT
- IMAPI_E_GENERIC
- IMAPI_E_MEDIUM_NOTPRESENT
- IMAPI_E_MEDIUM_INVALIDTYPE
- IMAPI_E_DEVICE_NOPROPERTIES
- IMAPI_E_DEVICE_NOTACCESSIBLE
- IMAPI_E_DEVICE_NOTPRESENT
- IMAPI_E_DEVICE_INVALIDTYPE
- IMAPI_E_INITIALIZE_WRITE
- IMAPI_E_INITIALIZE_ENDWRITE
- IMAPI_E_FILESYSTEM
- IMAPI_E_FILEACCESS
- IMAPI_E_DISCINFO
- IMAPI_E_TRACKNOTOPEN
- IMAPI_E_TRACKOPEN
- IMAPI_E_DISCFULL
- IMAPI_E_BADJOLIETNAME
- IMAPI_E_INVALIDIMAGE
- IMAPI_E_NOACTIVEFORMAT
- IMAPI_E_NOACTIVERECORDER
- IMAPI_E_WRONGFORMAT
- IMAPI_E_ALREADYOPEN
- IMAPI_E_WRONGDISC
- IMAPI_E_FILEEXISTS
- IMAPI_E_STASHINUSE
- IMAPI_E_DEVICE_STILL_IN_USE
- IMAPI_E_LOSS_OF_STREAMING
- IMAPI_E_COMPRESSEDSTASH
- IMAPI_E_ENCRYPTEDSTASH
- IMAPI_E_NOTENOUGHDISKFORSTASH
- IMAPI_E_REMOVABLESTASH
- IMAPI_E_CANNOT_WRITE_TO_MEDIA
- IMAPI_E_TRACK_NOT_BIG_ENOUGH
api_location:
- Imapierror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80e8aba2a2d3d12628a45c6716c6f94a405d752f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685528"
---
# <a name="imapiv1-result-codes"></a>IMAPIv1 結果碼

如果方法成功，IMAPI.EXE 介面的方法會傳回 S \_ OK。 否則，它們會傳回下列其中一個結果碼。



| 常數/值                                                                                                                                                                                                                                                                    | Description                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMAPI_S_PROPERTIESIGNORED"></span><span id="imapi_s_propertiesignored"></span><dl> <dt>**Imapi.exe \_S \_ PROPERTIESIGNORED**</dt> <dt>0x40200</dt> </dl>                   | 在屬性集內傳遞了不明的屬性，但它已被忽略。<br/>                                                                                                                                                                              |
| <span id="IMAPI_S_BUFFER_TO_SMALL"></span><span id="imapi_s_buffer_to_small"></span><dl> <dt>**Imapi.exe \_S \_ 緩衝區 \_ 至 \_ 小型**</dt> <dt>0x40201</dt> </dl>                       | 輸出緩衝區太小。<br/>                                                                                                                                                                                                                   |
| <span id="IMAPI_E_NOTOPENED"></span><span id="imapi_e_notopened"></span><dl> <dt>**Imapi.exe \_E \_ NOTOPENED**</dt> <dt>0x8004020b</dt> </dl>                                        | 尚未對 [**IDiscMaster：： Open**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open) 進行呼叫。<br/>                                                                                                                                                                        |
| <span id="IMAPI_E_NOTINITIALIZED"></span><span id="imapi_e_notinitialized"></span><dl> <dt>**Imapi.exe \_E \_ NOTINITIALIZED**</dt> <dt>0x8004020c</dt> </dl>                         | 錄製器物件尚未初始化。<br/>                                                                                                                                                                                                       |
| <span id="IMAPI_E_USERABORT"></span><span id="imapi_e_userabort"></span><dl> <dt>**Imapi.exe \_E \_ USERABORT**</dt> <dt>0x8004020d</dt> </dl>                                        | 使用者已取消操作。<br/>                                                                                                                                                                                                                  |
| <span id="IMAPI_E_GENERIC"></span><span id="imapi_e_generic"></span><dl> <dt>**Imapi.exe \_E \_ 泛型**</dt> <dt>0x8004020e</dt> </dl>                                              | 發生一般錯誤。<br/>                                                                                                                                                                                                                         |
| <span id="IMAPI_E_MEDIUM_NOTPRESENT"></span><span id="imapi_e_medium_notpresent"></span><dl> <dt>**Imapi.exe \_E \_ 中型 \_ NOTPRESENT**</dt> <dt>0x8004020f</dt> </dl>               | 裝置中沒有任何光碟。<br/>                                                                                                                                                                                                                   |
| <span id="IMAPI_E_MEDIUM_INVALIDTYPE"></span><span id="imapi_e_medium_invalidtype"></span><dl> <dt>**Imapi.exe \_E \_ 中型 \_ INVALIDTYPE**</dt> <dt>0x80040210</dt> </dl>            | 媒體不是可使用的類型。<br/>                                                                                                                                                                                                         |
| <span id="IMAPI_E_DEVICE_NOPROPERTIES"></span><span id="imapi_e_device_noproperties"></span><dl> <dt>**Imapi.exe \_E \_ 裝置 \_ NOPROPERTIES**</dt> <dt>0x80040211</dt> </dl>         | 錄製器不支援任何屬性。<br/>                                                                                                                                                                                                     |
| <span id="IMAPI_E_DEVICE_NOTACCESSIBLE"></span><span id="imapi_e_device_notaccessible"></span><dl> <dt>**Imapi.exe \_E \_ 裝置 \_ NOTACCESSIBLE**</dt> <dt>0x80040212</dt> </dl>      | 裝置無法使用或已在使用中。<br/>                                                                                                                                                                                                   |
| <span id="IMAPI_E_DEVICE_NOTPRESENT"></span><span id="imapi_e_device_notpresent"></span><dl> <dt>**Imapi.exe \_E \_ 裝置 \_ NOTPRESENT**</dt> <dt>0x80040213</dt> </dl>               | 裝置不存在或已移除。<br/>                                                                                                                                                                                                    |
| <span id="IMAPI_E_DEVICE_INVALIDTYPE"></span><span id="imapi_e_device_invalidtype"></span><dl> <dt>**Imapi.exe \_E \_ 裝置 \_ INVALIDTYPE**</dt> <dt>0x80040214</dt> </dl>            | 錄製器不支援操作。<br/>                                                                                                                                                                                                       |
| <span id="IMAPI_E_INITIALIZE_WRITE"></span><span id="imapi_e_initialize_write"></span><dl> <dt>**Imapi.exe \_E \_ INITIALIZE \_ WRITE**</dt> <dt>0x80040215</dt> </dl>                  | 無法初始化磁片磁碟機介面進行寫入。<br/>                                                                                                                                                                                         |
| <span id="IMAPI_E_INITIALIZE_ENDWRITE"></span><span id="imapi_e_initialize_endwrite"></span><dl> <dt>**Imapi.exe \_E \_ INITIALIZE \_ ENDWRITE**</dt> <dt>0x80040216</dt> </dl>         | 無法初始化磁片磁碟機介面以進行關閉。<br/>                                                                                                                                                                                         |
| <span id="IMAPI_E_FILESYSTEM"></span><span id="imapi_e_filesystem"></span><dl> <dt>**Imapi.exe \_E \_ FILESYSTEM**</dt> <dt>0x80040217</dt> </dl>                                     | 啟用/停用檔案系統存取或自動插入偵測期間發生錯誤。<br/>                                                                                                                                                 |
| <span id="IMAPI_E_FILEACCESS"></span><span id="imapi_e_fileaccess"></span><dl> <dt>**Imapi.exe \_E \_ FILEACCESS**</dt> <dt>0x80040218</dt> </dl>                                     | 寫入影像檔案時發生錯誤。<br/>                                                                                                                                                                                                   |
| <span id="IMAPI_E_DISCINFO"></span><span id="imapi_e_discinfo"></span><dl> <dt>**Imapi.exe \_E \_ DISCINFO**</dt> <dt>0x80040219</dt> </dl>                                           | 嘗試從裝置讀取光碟資料時發生錯誤。<br/>                                                                                                                                                                                 |
| <span id="IMAPI_E_TRACKNOTOPEN"></span><span id="imapi_e_tracknotopen"></span><dl> <dt>**Imapi.exe \_E \_ TRACKNOTOPEN**</dt> <dt>0x8004021a</dt> </dl>                               | 音訊播放軌未開啟以供寫入。<br/>                                                                                                                                                                                                           |
| <span id="IMAPI_E_TRACKOPEN"></span><span id="imapi_e_trackopen"></span><dl> <dt>**Imapi.exe \_E \_ TRACKOPEN**</dt> <dt>0x8004021b</dt> </dl>                                        | 已暫存開啟的音訊播放軌。<br/>                                                                                                                                                                                                      |
| <span id="IMAPI_E_DISCFULL"></span><span id="imapi_e_discfull"></span><dl> <dt>**Imapi.exe \_E \_ DISCFULL**</dt> <dt>0x8004021c</dt> </dl>                                           | 光碟無法保存任何其他資料。<br/>                                                                                                                                                                                                               |
| <span id="IMAPI_E_BADJOLIETNAME"></span><span id="imapi_e_badjolietname"></span><dl> <dt>**Imapi.exe \_E \_ BADJOLIETNAME**</dt> <dt>0x8004021d</dt> </dl>                            | 應用程式嘗試將不正確的名稱專案新增至光碟。<br/>                                                                                                                                                                                     |
| <span id="IMAPI_E_INVALIDIMAGE"></span><span id="imapi_e_invalidimage"></span><dl> <dt>**Imapi.exe \_E \_ INVALIDIMAGE**</dt> <dt>0x8004021e</dt> </dl>                               | 暫存的映射不適合燒錄。 它已損毀或清除，而且沒有任何可用的內容。<br/>                                                                                                                                          |
| <span id="IMAPI_E_NOACTIVEFORMAT"></span><span id="imapi_e_noactiveformat"></span><dl> <dt>**Imapi.exe \_E \_ NOACTIVEFORMAT**</dt> <dt>0x8004021f</dt> </dl>                         | 未使用 [**IDiscMaster：： SetActiveDiscMasterFormat**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscmasterformat)選取現用格式主機。<br/>                                                                                                      |
| <span id="IMAPI_E_NOACTIVERECORDER"></span><span id="imapi_e_noactiverecorder"></span><dl> <dt>**Imapi.exe \_E \_ NOACTIVERECORDER**</dt> <dt>0x80040220</dt> </dl>                   | 尚未使用 [**IDiscMaster：： SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder)選取使用中的光碟錄製器。<br/>                                                                                                              |
| <span id="IMAPI_E_WRONGFORMAT"></span><span id="imapi_e_wrongformat"></span><dl> <dt>**Imapi.exe \_E \_ WRONGFORMAT**</dt> <dt>0x80040221</dt> </dl>                                  | 當 [**IRedbookDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster)是使用中格式時，就會呼叫 [**IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) ，反之亦然。 若要使用不同的格式，請變更格式並清除影像檔案內容。<br/> |
| <span id="IMAPI_E_ALREADYOPEN"></span><span id="imapi_e_alreadyopen"></span><dl> <dt>**Imapi.exe \_E \_ ALREADYOPEN**</dt> <dt>0x80040222</dt> </dl>                                  | 您的應用程式已經對此物件呼叫 [**IDiscMaster：： Open**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open) 。<br/>                                                                                                                            |
| <span id="IMAPI_E_WRONGDISC"></span><span id="imapi_e_wrongdisc"></span><dl> <dt>**Imapi.exe \_E \_ WRONGDISC**</dt> <dt>0x80040223</dt> </dl>                                        | IMAPI.EXE 多會話光碟已從使用中的錄製器中移除。<br/>                                                                                                                                                                           |
| <span id="IMAPI_E_FILEEXISTS"></span><span id="imapi_e_fileexists"></span><dl> <dt>**Imapi.exe \_E \_ FILEEXISTS**</dt> <dt>0x80040224</dt> </dl>                                     | 要加入的檔案已在影像檔中，且未設定覆寫旗標。<br/>                                                                                                                                                                  |
| <span id="IMAPI_E_STASHINUSE"></span><span id="imapi_e_stashinuse"></span><dl> <dt>**Imapi.exe \_E \_ STASHINUSE**</dt> <dt>0x80040225</dt> </dl>                                     | 另一個應用程式已經使用暫存光碟映射所需的 IMAPI.EXE 隱藏檔。 請稍後再試一次。<br/>                                                                                                                                        |
| <span id="IMAPI_E_DEVICE_STILL_IN_USE"></span><span id="imapi_e_device_still_in_use"></span><dl> <dt>**Imapi.exe \_E \_ 裝置 \_ 仍 \_ 在 \_ 使用中**</dt> <dt>0x80040226</dt> </dl>       | 另一個應用程式已在使用此裝置，因此 IMAPI.EXE 無法存取裝置。<br/>                                                                                                                                                              |
| <span id="IMAPI_E_LOSS_OF_STREAMING"></span><span id="imapi_e_loss_of_streaming"></span><dl> <dt>**Imapi.exe \_E \_ 0x80040227 \_ 遺失 \_ 串流**</dt> <dt></dt> </dl>              | 內容串流遺失;可能發生了執行中的緩衝區。<br/>                                                                                                                                                                                 |
| <span id="IMAPI_E_COMPRESSEDSTASH"></span><span id="imapi_e_compressedstash"></span><dl> <dt>**Imapi.exe \_E \_ COMPRESSEDSTASH**</dt> <dt>0x80040228</dt> </dl>                      | 隱藏專案位於壓縮的磁片區上，無法讀取。<br/>                                                                                                                                                                                   |
| <span id="IMAPI_E_ENCRYPTEDSTASH"></span><span id="imapi_e_encryptedstash"></span><dl> <dt>**Imapi.exe \_E \_ ENCRYPTEDSTASH**</dt> <dt>0x80040229</dt> </dl>                         | 隱藏專案位於加密的磁片區上，無法讀取。<br/>                                                                                                                                                                                   |
| <span id="IMAPI_E_NOTENOUGHDISKFORSTASH"></span><span id="imapi_e_notenoughdiskforstash"></span><dl> <dt>**Imapi.exe \_E \_ NOTENOUGHDISKFORSTASH**</dt> <dt>0x8004022a</dt> </dl>    | 沒有足夠的可用空間可在指定的磁片區上建立隱藏的檔案。<br/>                                                                                                                                                                  |
| <span id="IMAPI_E_REMOVABLESTASH"></span><span id="imapi_e_removablestash"></span><dl> <dt>**Imapi.exe \_E \_ REMOVABLESTASH**</dt> <dt>0x8004022b</dt> </dl>                         | 選取的隱藏位置位於卸載式媒體上。<br/>                                                                                                                                                                                              |
| <span id="IMAPI_E_CANNOT_WRITE_TO_MEDIA"></span><span id="imapi_e_cannot_write_to_media"></span><dl> <dt>**Imapi.exe \_E \_ 無法 \_ 寫入 \_ \_ 媒體**</dt> <dt>0x8004022c</dt> </dl> | 媒體無法寫入。<br/>                                                                                                                                                                                                                   |
| <span id="IMAPI_E_TRACK_NOT_BIG_ENOUGH"></span><span id="imapi_e_track_not_big_enough"></span><dl> <dt>**Imapi.exe \_E \_ 曲目的 0x8004022d \_ \_ \_ 不夠大**</dt> <dt></dt> </dl>    | 此曲目不夠大。<br/>                                                                                                                                                                                                                      |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Imapierror。h</dt> </dl> |



 

 





