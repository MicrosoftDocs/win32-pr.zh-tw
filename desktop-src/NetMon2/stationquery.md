---
description: STATIONQUERY 結構會使用網路監視器來提供特定電腦的相關資訊。
ms.assetid: b7202c6b-e2b9-4a6f-8b87-3d11879f1d69
title: 'STATIONQUERY 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONQUERY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: de76c4da7bc27d76c04aeeaa7a46d69134e411ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997516"
---
# <a name="stationquery-structure"></a>STATIONQUERY 結構

**STATIONQUERY** 結構會使用網路監視器來提供特定電腦的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _STATIONQUERY {
  DWORD Flags;
  BYTE  BCDVerMinor;
  BYTE  BCDVerMajor;
  DWORD LicenseNumber;
  BYTE  MachineName[MACHINE_NAME_LENGTH];
  BYTE  UserName[USER_NAME_LENGTH];
  BYTE  Reserved[32];
  BYTE  AdapterAddress[6];
  WCHAR WMachineName[MACHINE_NAME_LENGTH];
  WCHAR WUserName[USER_NAME_LENGTH];
} STATIONQUERY, *LPSTATIONQUERY;
```



## <a name="members"></a>成員

<dl> <dt>

**旗標**
</dt> <dd>

識別網路監視器目前狀態的旗標。



| 值                                                                                                                                                                                                                | 意義                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="STATIONQUERY_FLAGS_LOADED"></span><span id="stationquery_flags_loaded"></span><dl> <dt>**已 \_ 載入 STATIONQUERY 旗標 \_**</dt> </dl>                   | 驅動程式已載入，但核心不是。<br/> |
| <span id="STATIONQUERY_FLAGS_RUNNING"></span><span id="stationquery_flags_running"></span><dl> <dt>**STATIONQUERY \_ 旗標 \_ 正在執行**</dt> </dl>                | 驅動程式已載入，但未捕獲資料。<br/> |
| <span id="STATIONQUERY_FLAGS_CAPTURING"></span><span id="stationquery_flags_capturing"></span><dl> <dt>**STATIONQUERY \_ 旗標 \_ 捕獲**</dt> </dl>          | 驅動程式積極參與捕捉。<br/> |
| <span id="STATIONQUERY_FLAGS_TRANSMITTING"></span><span id="stationquery_flags_transmitting"></span><dl> <dt>**STATIONQUERY \_ 旗標 \_ 傳輸**</dt> </dl> | 這個旗標已過時。<br/>                       |



 

</dd> <dt>

**BCDVerMinor**
</dt> <dd>

電腦上安裝網路監視器的次要版本號碼。

</dd> <dt>

**BCDVerMajor**
</dt> <dd>

電腦上安裝網路監視器的主要版本號碼。

</dd> <dt>

**LicenseNumber**
</dt> <dd>

軟體授權號碼。

</dd> <dt>

**MachineName**
</dt> <dd>

電腦製造商名稱（如果有的話）。

</dd> <dt>

**使用者名稱**
</dt> <dd>

使用者名稱或系統識別碼。

</dd> <dt>

**已保留**
</dt> <dd>

保留供未來使用。

</dd> <dt>

**AdapterAddress**
</dt> <dd>

NIC 位址。

</dd> <dt>

**WMachineName**
</dt> <dd>

Unicode 電腦名稱稱。 此成員適用于網路監視器2.0 或更新版本。

</dd> <dt>

**WUserName**
</dt> <dd>

Unicode 使用者名稱。 此成員適用于網路監視器2.0 或更新版本。

</dd> </dl>

## <a name="remarks"></a>備註

資料表資料表會使用 [這些結構的](querytable.md) 陣列來提供目前使用網路監視器來捕捉資料的電腦清單。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[透視](querytable.md)
</dt> </dl>

 

 




