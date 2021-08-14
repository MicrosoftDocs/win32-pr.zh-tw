---
title: 'WINBIO_SENSOR_MODE 常數 (Winbio \_ 類型 .h) '
description: 設定感應器介面卡模式。
ms.assetid: fceaed5c-de59-4da7-9d7a-adeef353292f
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_UNKNOWN_MODE
- WINBIO_SENSOR_BASIC_MODE
- WINBIO_SENSOR_ADVANCED_MODE
- WINBIO_SENSOR_NAVIGATION_MODE
- WINBIO_SENSOR_SLEEP_MODE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e8f0cb4592931629e6feec4fff4a6ac3e5986d3b199afee719dd8dae67a9580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909326"
---
# <a name="winbio_sensor_mode-constants"></a>WINBIO \_ 感應器 \_ 模式常數

[**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn)函式中使用下列值來設定感應器介面卡模式。



| 常數                                                                                                                                                                                                        | 描述                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_SENSOR_UNKNOWN_MODE"></span><span id="winbio_sensor_unknown_mode"></span><dl> <dt>**WINBIO \_ 感應器 \_ 不明 \_ 模式**</dt> </dl>          | 作業模式未知。<br/>                                                                                                                    |
| <span id="WINBIO_SENSOR_BASIC_MODE"></span><span id="winbio_sensor_basic_mode"></span><dl> <dt>**WINBIO \_ 感應器 \_ 基本 \_ 模式**</dt> </dl>                | 在基本模式下操作感應器。 感應器只能做為捕獲裝置。 不會使用任何存在的上架處理或儲存功能。<br/> |
| <span id="WINBIO_SENSOR_ADVANCED_MODE"></span><span id="winbio_sensor_advanced_mode"></span><dl> <dt>**WINBIO \_ 感應器 \_ ADVANCED \_ 模式**</dt> </dl>       | 以 advanced 模式操作感應器。 感應器可以捕獲範例，並執行相符和儲存功能。<br/>                                     |
| <span id="WINBIO_SENSOR_NAVIGATION_MODE"></span><span id="winbio_sensor_navigation_mode"></span><dl> <dt>**WINBIO \_ 感應器 \_ 流覽 \_ 模式**</dt> </dl> | 以滑鼠墊的形式操作感應器。 目前不受支援。<br/>                                                                                 |
| <span id="WINBIO_SENSOR_SLEEP_MODE"></span><span id="winbio_sensor_sleep_mode"></span><dl> <dt>**WINBIO \_ 感應器 \_ 睡眠 \_ 模式**</dt> </dl>                | 以睡眠模式操作感應器。<br/>                                                                                                                   |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                                    |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式常數](client-application-constants.md)
</dt> </dl>

 

 





