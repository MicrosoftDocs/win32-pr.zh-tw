---
description: 傳回目前影片輸出所使用 (SRM) 的系統 renewability 訊息版本號碼。
ms.assetid: 65d4b98b-369f-4863-a28c-f9e3b4c2b55d
title: 'OPM_GET_CURRENT_HDCP_SRM_VERSION (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e05ad53ae58e2141c63179c84a90f90cea86fb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969245"
---
# <a name="opm_get_current_hdcp_srm_version"></a>OPM \_ 取得 \_ 目前的 \_ HDCP \_ SRM \_ 版本

傳回目前影片輸出所使用 (SRM) 的系統 renewability 訊息版本號碼。



| 需求 | 值 |
|--------------|-----------------------------------------------------------------------------|
| 要求 GUID | OPM \_ 取得 \_ 目前的 \_ HDCP \_ SRM \_ 版本                                       |
| 輸入資料   | 無                                                                        |
| 傳回資料  | [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構 |



 

## <a name="remarks"></a>備註

如果此查詢成功， [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構的 **ulInformation** 成員會包含 SRM 版本號碼（以位元組由小到大格式）。

SRMs 可用來更新已撤銷 High-Bandwidth 數位內容保護 (HDCP) 裝置的清單。 SRMs 是以影片內容提供。 若要設定 SRM，請傳送 [**OPM \_ set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) 命令。

此查詢可能會導致 [**IOPMVideoOutput：： GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) 方法傳回下列任何錯誤碼。



| 傳回碼                                            | Description                             |
|--------------------------------------------------------|-----------------------------------------|
| 錯誤 \_ 圖形 \_ OPM \_ \_ \_ 尚未設定 HDCP \_ SRM            | 應用程式未設定 SRM。     |
| 錯誤 \_ 圖形 \_ OPM \_ 輸出 \_ 不 \_ \_ 支援 \_ HDCP | 影片輸出不支援 HDCP。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Opmapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IOPMVideoOutput：： GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[OPM 狀態要求](opm-status-requests.md)
</dt> </dl>

 

 




