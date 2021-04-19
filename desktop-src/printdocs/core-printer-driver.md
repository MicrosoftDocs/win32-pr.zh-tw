---
description: 代表其他印表機驅動程式所依存的印表機驅動程式。
ms.assetid: b03f9ac1-7ad2-4aee-b496-e1ee15ba7d38
title: 'CORE_PRINTER_DRIVER 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CORE_PRINTER_DRIVER
- _CORE_PRINTER_DRIVERA
- _CORE_PRINTER_DRIVERW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 786fa3491919659fca60700cfb086023c3fdef3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997125"
---
# <a name="core_printer_driver-structure"></a>核心 \_ 印表機 \_ 驅動程式結構

代表其他印表機驅動程式所依存的印表機驅動程式。

## <a name="syntax"></a>語法


```C++
typedef struct _CORE_PRINTER_DRIVER {
  GUID      CoreDriverGUID;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  TCHAR     szPackageID[MAX_PATH];
} CORE_PRINTER_DRIVER, *PCORE_PRINTER_DRIVER;
```



## <a name="members"></a>成員

<dl> <dt>

**CoreDriverGUID**
</dt> <dd>

核心印表機驅動程式的 GUID。

</dd> <dt>

**ftDriverDate**
</dt> <dd>

最新版本的核心印表機驅動程式的日期和時間。

</dd> <dt>

**dwlDriverVersion**
</dt> <dd>

最新版本的核心印表機驅動程式的版本識別碼。

</dd> <dt>

**szPackageID \[ 最大 \_ 路徑\]**
</dt> <dd>

包含核心印表機驅動程式之驅動程式套件的路徑。

</dd> </dl>

## <a name="remarks"></a>備註

此結構可代表製造商的基礎驅動程式，而該驅動程式的驅動程式與各種印表機型號相依。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 核心 \_ 印表機 \_ DRIVERW** (Unicode) 和 **\_ 核心 \_ 印表機 \_ DRIVERA** (ANSI) <br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




