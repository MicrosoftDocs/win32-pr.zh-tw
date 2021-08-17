---
title: 'WINBIO_FLAG 常數 (Winbio \_ 類型 .h) '
description: 指定新會話的生物特徵辨識單位設定和存取特性。
ms.assetid: 82b57023-6c27-433d-bf13-f136f501fc60
topic_type:
- apiref
api_name:
- WINBIO_FLAG_DEFAULT
- WINBIO_FLAG_BASIC
- WINBIO_FLAG_ADVANCED
- WINBIO_FLAG_RAW
- WINBIO_FLAG_MAINTENANCE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e018b1d810e3a57b4adea1116aa9bebc7b82dd44888b2d720e018329d31acf4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910308"
---
# <a name="winbio_flag-constants"></a>WINBIO \_ 旗標常數

下列常數可以用在 [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) 函式中，以指定新會話的生物特徵辨識單位設定和存取特性。



| 常數                                                                                                                                                                                     | 描述                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FLAG_DEFAULT"></span><span id="winbio_flag_default"></span><dl> <dt>**WINBIO \_ 旗標 \_ 預設值**</dt> </dl>             | 感應器設定旗標。 生物識別單位的運作方式是在安裝期間指定。<br/>                                                                           |
| <span id="WINBIO_FLAG_BASIC"></span><span id="winbio_flag_basic"></span><dl> <dt>**WINBIO \_ 旗標 \_ 基本**</dt> </dl>                   | 感應器設定旗標。 生物識別單位只會以基本的擷取裝置運作。<br/>                                                                                         |
| <span id="WINBIO_FLAG_ADVANCED"></span><span id="winbio_flag_advanced"></span><dl> <dt>**WINBIO \_ 旗標 \_ ADVANCED**</dt> </dl>          | 感應器設定旗標。 生物識別單位使用內部處理和儲存功能。<br/>                                                                              |
| <span id="WINBIO_FLAG_RAW"></span><span id="winbio_flag_raw"></span><dl> <dt>**WINBIO \_ 旗標 \_ 原始**</dt> </dl>                         | 所需的存取旗標。 用戶端應用程式會使用 [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample)來捕捉原始的生物特徵辨識資料。<br/>                                             |
| <span id="WINBIO_FLAG_MAINTENANCE"></span><span id="winbio_flag_maintenance"></span><dl> <dt>**WINBIO \_ 旗標 \_ 維護**</dt> </dl> | 所需的存取旗標。 用戶端會呼叫 [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged)，以在生物特徵辨識單位上執行廠商定義的控制作業。<br/> |



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

 

 





