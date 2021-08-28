---
description: 取得硬體編解碼器的業績值。
ms.assetid: 51987a79-78bf-41b2-8349-8c2725dd89d6
title: 'OPM_GET_CODEC_INFO (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988ffa9a962d9ed04b6a978da1534a6da4fa506e873d89d238bcbb2aa00fd865
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847978"
---
# <a name="opm_get_codec_info"></a>OPM \_ 取得 \_ 編解碼器 \_ 資訊

取得硬體編解碼器的業績值。



| 需求 | 值 |
|--------------|-------------------------------------------------------------------------------------------|
| 要求 GUID | **OPM \_ 取得 \_ 編解碼器 \_ 資訊**                                                                 |
| 輸入資料   | [**OPM \_ 取得 \_ 編解碼器 \_ 資訊 \_ 參數**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)結構   |
| 傳回資料  | [**OPM \_ 取得 \_ 編解碼器 \_ 資訊 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information)結構 |



 

## <a name="remarks"></a>備註

雖然此命令會使用 [輸出保護管理員](output-protection-manager.md) (OPM) 介面，但它只適用于硬體編碼器和解碼器。 不適用於影片輸出裝置。

一般而言，您不應該直接使用此命令。 若要取得硬體編解碼器的業績值，請呼叫 [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) 函式。 此函數會執行傳送 **OPM \_ 取得 \_ 編解碼器 \_ 資訊** 命令所需的所有 OPM 呼叫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Opmapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[OPM 狀態要求](opm-status-requests.md)
</dt> <dt>

[輸出保護管理員](output-protection-manager.md)
</dt> <dt>

[**IOPMVideoOutput：： GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> </dl>

 

 




