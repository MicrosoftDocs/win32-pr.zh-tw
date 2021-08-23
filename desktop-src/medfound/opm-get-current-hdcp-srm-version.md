---
description: 傳回目前影片輸出所使用 (SRM) 的系統 renewability 訊息版本號碼。
ms.assetid: 65d4b98b-369f-4863-a28c-f9e3b4c2b55d
title: 'OPM_GET_CURRENT_HDCP_SRM_VERSION (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee36516510d04fec067bbc692387e2e36b9da083db1a6daae0f51948a992cc83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887488"
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



| 傳回碼                                            | 描述                             |
|--------------------------------------------------------|-----------------------------------------|
| 錯誤 \_ 圖形 \_ OPM \_ \_ \_ 尚未設定 HDCP \_ SRM            | 應用程式未設定 SRM。     |
| 錯誤 \_ 圖形 \_ OPM \_ 輸出 \_ 不 \_ \_ 支援 \_ HDCP | 影片輸出不支援 HDCP。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Opmapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IOPMVideoOutput：： GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[OPM 狀態要求](opm-status-requests.md)
</dt> </dl>

 

 




