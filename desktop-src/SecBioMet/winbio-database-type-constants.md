---
title: 'WINBIO_DATABASE_TYPE 常數 (Winbio \_ 類型 .h) '
description: 可以用於 WINBIO \_ 儲存架構結構之屬性成員的旗標 \_ 。
ms.assetid: 07e7e91c-3ca6-41cd-a2c7-ac43bb5156a6
topic_type:
- apiref
api_name:
- WINBIO_DATABASE_TYPE_MASK
- WINBIO_DATABASE_TYPE_FILE
- WINBIO_DATABASE_TYPE_DBMS
- WINBIO_DATABASE_TYPE_ONCHIP
- WINBIO_DATABASE_TYPE_SMARTCARD
- WINBIO_DATABASE_FLAG_MASK
- WINBIO_DATABASE_FLAG_REMOVABLE
- WINBIO_DATABASE_FLAG_REMOTE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acd67f49c5fa689fb4418789aae7c4d6c9a305a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685914"
---
# <a name="winbio_database_type-constants"></a>WINBIO \_ 資料庫 \_ 類型常數

下列旗標可用於 [**WINBIO \_ 儲存 \_ 架構**](winbio-storage-schema.md)結構的 **屬性** 成員。



| 常數/值                                                                                                                                                                                                                                                                     | Description                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <dt>**WINBIO \_資料庫 \_ 類型 \_ 遮罩**</dt> <dt>0x0000FFFF</dt> </dl>                | 表示所有 \_ 類型位的遮罩 \_ 。<br/>                                                                   |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <dt>**WINBIO \_資料庫 \_ 類型 \_**</dt>檔 <dt>0x00000001</dt> </dl>                | 資料庫包含在檔案中。<br/>                                                                              |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <dt>**WINBIO \_資料庫 \_ 類型 \_ DBMS**</dt> <dt>0x00000002</dt> </dl>                | 資料庫是由外部資料庫管理系統所管理 (DBMS) 元件，例如 Microsoft SQL Server。<br/> |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <dt>**WINBIO \_資料庫 \_ 類型 \_ ONCHIP**</dt> <dt>0x00000003</dt> </dl>          | 資料庫位於生物特徵辨識感應器上。<br/>                                                                     |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <dt>**WINBIO \_資料庫 \_ 類型 \_ 智慧卡**</dt> <dt>0x00000004</dt> </dl> | 資料庫位於智慧卡上。<br/>                                                                             |
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <dt>**WINBIO \_資料庫 \_ 旗標 \_ 遮罩**</dt> <dt>0xFFFF0000</dt> </dl>                | 表示所有旗標位的遮罩 \_ \_ 。<br/>                                                                   |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <dt>**WINBIO \_資料庫 \_ 旗標 \_ 可移動**</dt> <dt>0x00010000</dt> </dl> | 包含資料庫的儲存媒體可以從電腦中實際移除。<br/>                           |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <dt>**WINBIO \_資料庫 \_ 旗標 \_ 遠端**</dt> <dt>0x00020000</dt> </dl>          | 資料庫位於遠端電腦上。<br/>                                                                        |



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

 

 





