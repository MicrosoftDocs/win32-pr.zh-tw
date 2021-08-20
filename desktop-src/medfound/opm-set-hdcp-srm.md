---
description: 更新 (SRM) 的系統 renewability 訊息，以 High-Bandwidth 數位內容保護 (HDCP) 。
ms.assetid: ea18baba-0e03-4471-af0e-a588773c98d2
title: 'OPM_SET_HDCP_SRM (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23601386353e0a18ed95238cee7a11ba9c39a84fbf1855b839bde0fd841ccd17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118058724"
---
# <a name="opm_set_hdcp_srm"></a>OPM \_ 設定 \_ HDCP \_ SRM

更新 (SRM) 的系統 renewability 訊息，以 High-Bandwidth 數位內容保護 (HDCP) 。



| 需求 | 值 |
|--------------|-------------------------------------------------------------------------------------|
| 命令 GUID | OPM \_ 設定 \_ HDCP \_ SRM                                                                 |
| 輸入資料   | [**OPM \_ 設定 \_ HDCP \_ SRM \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters)結構 |



 

[**IOPMVideoOutput：： Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)的 *pbAdditionalParameters* 參數必須指向包含 SRM 的緩衝區。 HDCP SRM 的格式記載于 HDCP 規格中。 將 *ulAdditionalParametersSize* 參數設定為等於緩衝區的大小（以位元組為單位）。

## <a name="remarks"></a>備註

SRMs 可用來更新已撤銷的 HDCP 裝置清單。 SRMs 是以影片內容提供。

此命令會更新影片輸出的目前「SRM」。 如果在命令時啟用了 HDCP，則影片輸出會使用新的 SRM 來檢查是否已撤銷任何已連線的 HDCP 裝置。 如果影片輸出偵測到已撤銷的裝置，則會停止顯示影片。 如果您在 HDCP 停用時傳送此命令，則影片輸出會驗證 SRM 並加以儲存。 之後，如果應用程式啟用 HDCP，則影片輸出會使用新的 SRM 來檢查裝置的撤銷狀態。

此命令可能會導致 **Configure** 方法傳回下列任何錯誤碼。



| 傳回碼                                            | 描述                             |
|--------------------------------------------------------|-----------------------------------------|
| 錯誤 \_ 圖形 \_ OPM \_ 不正確 \_ SRM                     | SRM 無效。                   |
| 錯誤 \_ 圖形 \_ OPM \_ 輸出 \_ 不 \_ \_ 支援 \_ HDCP | 影片輸出不支援 HDCP。 |



 

當 **IOPMVideoOutput** 介面 (COPP) 模擬經認證的輸出保護通訊協定時，不支援這個命令。 使用 COPP 的語法時，應用程式會負責剖析 SRMs 和檢查 HDCP 裝置的撤銷狀態。 使用 [OPM \_ 取得連線 \_ 的 \_ HDCP \_ 裝置 \_ 資訊](opm-get-connected-hdcp-device-information.md) 狀態要求，取得裝置的金鑰選取向量 (KSV) ，這是檢查撤銷狀態所需的專案。 如需 SRMs 的詳細資訊，請參閱 HDCP 規格。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Opmapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IOPMVideoOutput：： Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[OPM 命令](opm-commands.md)
</dt> </dl>

 

 




