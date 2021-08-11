---
description: 深入瞭解： OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION
ms.assetid: 71fa9a99-83e4-4b27-9fd1-5a9dc3070820
title: 'OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d692680e6492a3dc5d92073baf069eefffde68841925ced9afd69dde4d5fcd97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239891"
---
# <a name="opm_get_connected_hdcp_device_information"></a>OPM \_ 取得 \_ 已連線的 \_ HDCP \_ 裝置 \_ 資訊

取得連接至影片輸出 High-Bandwidth 數位內容保護 (HDCP) 裝置的相關資訊。 會傳回下列資訊：

-   裝置的 HDCP 金鑰選取向量 (KSV) 。
-   裝置是否為 HDCP 中繼器。



| 需求 | 值 |
|--------------|---------------------------------------------------------------------------------------------------------|
| 要求 GUID | OPM \_ 取得 \_ 已連線的 \_ HDCP \_ 裝置 \_ 資訊                                                          |
| 輸入資料   | 無                                                                                                    |
| 傳回資料  | [**OPM \_ 連線的 \_ HDCP \_ 裝置 \_ 資訊**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information)結構 |



 

## <a name="remarks"></a>備註

此查詢只能與 *COPP 模擬模式* 搭配使用。 如果 [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) 介面使用輸出保護管理員 (OPM) 語義，則不支援此狀態要求。

KSV 是提供給裝置製造商的識別碼，用於 HDCP 驗證和設定程式。 在 COPP 模擬模式中，應用程式會使用 KSV 來判斷是否已撤銷 HDCP 裝置。 如果是，應用程式不應該播放受保護的內容。 此外，如果裝置為 HDCP 中繼器，應用程式不應該播放受保護的內容，因為 COPP 不支援 HDCP 中繼器。

使用 OPM 語義時不需要此查詢，因為 OPM 支援裝置撤銷和 HDCP 中繼器。

此查詢相當於 \_ 認證輸出保護通訊協定 (COPP) 中所使用的 DXVA COPPQueryHDCPKeyData 查詢。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Opmapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IOPMVideoOutput：： COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[OPM 狀態要求](opm-status-requests.md)
</dt> </dl>

 

 




