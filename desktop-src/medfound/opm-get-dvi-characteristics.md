---
description: 查詢數位視訊介面 (DVI) 連接器是否支援 DVI 1.1 版或更新版本。
ms.assetid: b6c450c0-e97f-472d-ae09-fa1e062aeb9e
title: 'OPM_GET_DVI_CHARACTERISTICS (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a6f996b0397db509a45af6e243359c581df333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026389"
---
# <a name="opm_get_dvi_characteristics"></a>OPM \_ 取得 \_ DVI \_ 特性

查詢數位視訊介面 (DVI) 連接器是否支援 DVI 1.1 版或更新版本。



| 需求 | 值 |
|--------------|-----------------------------------------------------------------------------|
| 要求 GUID | OPM \_ 取得 \_ DVI \_ 特性                                              |
| 輸入資料   | 無                                                                        |
| 傳回資料  | [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構 |



 

## <a name="remarks"></a>備註

如果此查詢成功， [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構的 **ulInformation** 成員就會包含下列其中一個值。



| 值                                     | 描述               |
|-------------------------------------------|---------------------------|
| OPM \_ DVI \_ 特性 \_ 1 \_ 0            | DVI 1.0 版。          |
| OPM \_ DVI \_ 特性 \_ 1 \_ 1 \_ 或 \_ 更新版本 | DVI 1.1 版或更新版本。 |



 

只有當實體連接器類型是 OPM 連接器類型的 DVI 時，才支援此查詢 \_ \_ \_ 。 若要取得連接器類型，請傳送 [**OPM \_ get \_ connector \_ 型**](opm-get-connector-type.md) 別查詢。

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

 

 




