---
title: 'WINBIO_BIR_QUALITY 常數 (Winbio \_ 類型 .h) '
description: 如果未指定0到100的整數值，請指定 BIR 中生物特徵辨識資料的相對品質。
ms.assetid: A42AA21B-9AA5-4DB6-B58F-0776BEC63E6C
topic_type:
- apiref
api_name:
- WINBIO_DATA_QUALITY_NOT_SET
- WINBIO_DATA_QUALITY_NOT_SUPPORTED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1eb0881672c9e3bf51214cff93cb3f68d802b04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106193"
---
# <a name="winbio_bir_quality-constants"></a>WINBIO \_ BIR \_ 品質常數

[**WINBIO \_ BIR \_ 標頭**](winbio-bir-header.md)結構的 **DataQuality** 成員會使用下列旗標，以指定從0到100的整數值未指定時，BIR 中生物特徵辨識資料的相對品質。



| 常數/值                                                                                                                                                                                                                                                                       | Description                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <dt>**WINBIO \_資料 \_ 品質 \_ 未 \_ 設定**</dt> <dt> 1</dt> </dl>                   | BIR 建立者支援品質度量，但未在 BIR 中設定任何值。<br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <dt>**WINBIO \_\_ \_ 不 \_ 支援資料品質**</dt> <dt>2</dt> </dl> | BIR 建立者不支援品質度量。<br/>                             |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式常數](client-application-constants.md)
</dt> </dl>

 

 





