---
description: 傳回影片輸出的實體接點類型。
ms.assetid: c5862758-0125-4dbe-af72-5ed4a85bd702
title: 'OPM_GET_CONNECTOR_TYPE (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a95ca88b079aa93b4c2665fe7aa954eb58cfc1a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191771"
---
# <a name="opm_get_connector_type"></a>OPM \_ 取得 \_ 連接器 \_ 類型

傳回影片輸出的實體接點類型。



| 需求 | 值 |
|--------------|-----------------------------------------------------------------------------|
| 要求 GUID | OPM \_ 取得 \_ 連接器 \_ 類型                                                   |
| 輸入資料   | 無                                                                        |
| 傳回資料  | [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構 |



 

## <a name="remarks"></a>備註

連接器類型會以 [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構的 **ulInformation** 成員傳回。 **UlInformation** 的值等於 [**OPM 連接器類型旗標**](opm-connector-type-flags.md)中列出的其中一個連接器類型。

在 COPP 模擬模式中，連接器類型可能會與 **OPM \_ COPP 相容的 \_ \_ 連接器 \_ 類型 \_ 內部** 旗標合併。 使用位 **and** 來將連接器型別解壓縮：

`ulInformation & ~OPM_COPP_COMPATIBLE_CONNECTOR_TYPE_INTERNAL`

應用程式應該忽略 **OPM \_ COPP \_ 相容的 \_ 連接器 \_ 類型 \_ 內部** 旗標。 如需詳細資訊，請參閱 [**OPM 連接器類型旗標**](opm-connector-type-flags.md)的備註一節。

此查詢相當於 \_ 認證輸出保護通訊協定 (COPP) 中所使用的 DXVA COPPQueryConnectorType 查詢。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Opmapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IOPMVideoOutput：： COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput：： GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[OPM 狀態要求](opm-status-requests.md)
</dt> </dl>

 

 




