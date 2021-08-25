---
title: 'WINBIO_DB 常數 (Winbio \_ 類型 .h) '
description: 指定要用於系統集區的資料庫。
ms.assetid: 2cffa455-5834-4a35-b8d8-f9d1feddcaa1
topic_type:
- apiref
api_name:
- WINBIO_DB_DEFAULT
- WINBIO_DB_BOOTSTRAP
- WINBIO_DB_ONCHIP
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a9d8392fd38e9d53588002c8aeab688ffc8b76efced83819318d9c6b6c2b721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867978"
---
# <a name="winbio_db-constants"></a>WINBIO \_ DB 常數

呼叫 [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) 來指定要用於系統集區的資料庫時，可以使用下列常數。



| 常數                                                                                                                                                                         | 描述                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DB_DEFAULT"></span><span id="winbio_db_default"></span><dl> <dt>**WINBIO \_ DB \_ 預設值**</dt> </dl>       | 感應器集區中的每個生物特徵辨識單位都會使用預設生物識別單位設定中指定的預設資料庫。<br/>                                                                   |
| <span id="WINBIO_DB_BOOTSTRAP"></span><span id="winbio_db_bootstrap"></span><dl> <dt>**WINBIO \_ DB \_ 啟動程式**</dt> </dl> | 可以用於啟動 Windows 之前的案例。 一般而言，資料庫是感應器晶片的一部分或屬於 BIOS 的一部分，而且只能用於範本註冊與刪除。<br/> |
| <span id="WINBIO_DB_ONCHIP"></span><span id="winbio_db_onchip"></span><dl> <dt>**WINBIO \_ DB \_ ONCHIP**</dt> </dl>          | 資料庫位於感應器晶片上。<br/>                                                                                                                                                  |



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

 

 





