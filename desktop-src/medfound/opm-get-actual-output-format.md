---
description: 傳回透過連接器傳輸之視訊訊號的描述。
ms.assetid: 8464470f-49db-4559-80b2-02cfc473e30e
title: 'OPM_GET_ACTUAL_OUTPUT_FORMAT (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a37f35e9f3d64bd1a72bb6800011978ea1cf2f4c60f523a344594f949beb4f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102072"
---
# <a name="opm_get_actual_output_format"></a>OPM \_ 取得 \_ 實際 \_ 輸出 \_ 格式

傳回透過連接器傳輸之視訊訊號的描述。



| 需求 | 值 |
|--------------|------------------------------------------------------------------------------|
| 要求 GUID | OPM \_ 取得 \_ 實際 \_ 輸出 \_ 格式                                             |
| 輸入資料   | 無                                                                         |
| 傳回資料  | [**OPM \_ 實際 \_ 輸出 \_ 格式**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format)結構 |



 

## <a name="remarks"></a>備註

透過連接器傳送的視訊訊號不一定會與桌面顯示模式具有相同的格式。 例如，桌面顯示模式可能是 1024 x 768 圖元（85 Hz），而連接器可能是以 720 x 480 圖元為單位傳輸視訊訊號的 S-video 連接器，60/1.01 Hz。 在此情況下，驅動程式會傳回 S-video 信號的解析度，而不是電腦解析度。

此查詢相當於 \_ 認證輸出保護通訊協定 (COPP) 中所使用的 DXVA COPPQueryDisplayData 查詢。

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

[**IOPMVideoOutput：： GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[OPM 狀態要求](opm-status-requests.md)
</dt> </dl>

 

 




