---
title: 'WINBIO_STORAGE_SCHEMA 結構 (Winbio \_ 類型 .h) '
description: 描述生物特徵辨識存儲裝置配接器的功能。
ms.assetid: e4924803-5a1b-4e0a-b2cb-01d018d27ba1
keywords:
- WINBIO_STORAGE_SCHEMA 結構 Windows 生物特徵辨識架構 API
- PWINBIO_STORAGE_SCHEMA 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_STORAGE_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc0bd0d61814b4133c3789b0c8119edcaf79945452cc26aa313504c055ac2f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909255"
---
# <a name="winbio_storage_schema-structure"></a>WINBIO \_ 儲存體 \_ 架構結構

**WINBIO \_ 儲存體 \_ 架構** 結構描述生物特徵辨識儲存體介面卡的功能。 [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)函數會使用這個結構。

## <a name="syntax"></a>語法


```C++
typedef struct _WINBIO_STORAGE_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           DatabaseId;
  WINBIO_UUID           DataFormat;
  ULONG                 Attributes;
  WINBIO_STRING         FilePath;
  WINBIO_STRING         ConnectionString;
} WINBIO_STORAGE_SCHEMA, *PWINBIO_STORAGE_SCHEMA;
```



## <a name="members"></a>成員

<dl> <dt>

**BiometricFactor**
</dt> <dd>

儲存在資料庫中的生物特徵辨識測量型別。

</dd> <dt>

**DatabaseId**
</dt> <dd>

識別資料庫的 GUID。

</dd> <dt>

**DataFormat**
</dt> <dd>

識別資料庫中範本格式的 GUID。

</dd> <dt>

**屬性**
</dt> <dd>

資料庫特性的相關資訊。 這可以是下列常數的位 **or** 。



| 值                                                                                                                                                                                                                                                                              | 意義                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <dt>**WINBIO \_資料庫 \_ 旗標 \_ 遮罩**</dt> <dt>0xFFFF0000</dt> </dl>                | 代表旗標位的遮罩。<br/>                     |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <dt>**WINBIO \_資料庫 \_ 旗標 \_ 遠端**</dt> <dt>0x00020000</dt> </dl>          | 資料庫位於遠端電腦上。<br/>               |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <dt>**WINBIO \_資料庫 \_ 旗標 \_ 可移動**</dt> <dt>0x00010000</dt> </dl> | 資料庫位於抽取式磁碟機上。<br/>               |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <dt>**WINBIO \_資料庫 \_ 類型 \_ DBMS**</dt> <dt>0x00000002</dt> </dl>                | 資料庫是由資料庫管理系統所管理。<br/> |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <dt>**WINBIO \_資料庫 \_ 類型 \_**</dt>檔 <dt>0x00000001</dt> </dl>                | 資料庫包含在檔案中。<br/>                     |
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <dt>**WINBIO \_資料庫 \_ 類型 \_ 遮罩**</dt> <dt>0x0000FFFF</dt> </dl>                | 表示類型位的遮罩。<br/>                     |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <dt>**WINBIO \_資料庫 \_ 類型 \_ ONCHIP**</dt> <dt>0x00000003</dt> </dl>          | 資料庫位於生物特徵辨識感應器上。<br/>            |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <dt>**WINBIO \_資料庫 \_ 類型 \_ 智慧卡**</dt> <dt>0x00000004</dt> </dl> | 資料庫位於智慧卡上。<br/>                    |



 

</dd> <dt>

**FilePath**
</dt> <dd>

如果資料庫位於電腦磁片上，則為資料庫的路徑和檔案名。

</dd> <dt>

**ConnectionString**
</dt> <dd>

可傳送至資料庫伺服器以識別資料庫的字串值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                                    |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式結構](client-application-structures.md)
</dt> <dt>

[**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)
</dt> </dl>

 

 





