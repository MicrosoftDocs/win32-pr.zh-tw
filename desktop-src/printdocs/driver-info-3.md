---
description: 驅動程式 \_ 資訊 \_ 3 結構包含印表機驅動程式資訊。
ms.assetid: ccf87319-0bcf-4f71-8de3-0190459d2b0e
title: 'DRIVER_INFO_3 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_3
- _DRIVER_INFO_3A
- _DRIVER_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 64509977a85bc33cb13dac4e6ba2817502c06cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996930"
---
# <a name="driver_info_3-structure"></a>驅動程式 \_ 資訊 \_ 3 結構

**驅動程式 \_ 資訊 \_ 3** 結構包含印表機驅動程式資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _DRIVER_INFO_3 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
  LPTSTR pHelpFile;
  LPTSTR pDependentFiles;
  LPTSTR pMonitorName;
  LPTSTR pDefaultDataType;
} DRIVER_INFO_3, *PDRIVER_INFO_3;
```



## <a name="members"></a>成員

<dl> <dt>

**cVersion**
</dt> <dd>

寫入驅動程式的作業系統版本。 支援的值為3和4，分別代表 V3 和 V4 驅動程式。

</dd> <dt>

**pName**
</dt> <dd>

以 null 結束的字串指標，指定驅動程式的名稱 (例如 "QMS 810" ) 。

</dd> <dt>

**pEnvironment**
</dt> <dd>

以 null 結束的字串指標，指定寫入驅動程式的環境 (例如，Windows x86、Windows IA64 和 Windows x64) 。

</dd> <dt>

**pDriverPath**
</dt> <dd>

以 null 結束的字串指標，指定包含設備磁碟機之檔案的檔案名或完整路徑和檔案名 (例如 "C： \\ 驅動程式 \\Pscript.dll" ) 。

</dd> <dt>

**pDataFile**
</dt> <dd>

以 null 結束的字串指標，指定包含驅動程式資料之檔案的檔案名或完整路徑和檔案名 (例如 "C： \\ 驅動程式 \\ Qms810" ) 。

</dd> <dt>

**pConfigFile**
</dt> <dd>

以 null 結束的字串指標，指定設備磁碟機設定動態連結程式庫的檔案名或完整路徑和檔案名 (例如 "C： \\ 驅動程式 \\Pscrptui.dll" ) 。

</dd> <dt>

**pHelpFile**
</dt> <dd>

以 null 終止的字串指標，指定設備磁碟機的說明檔的檔案名或完整路徑和檔案名。

</dd> <dt>

**pDependentFiles**
</dt> <dd>

MultiSZ 緩衝區的指標，其中包含以 null 終止之字串的序列。 緩衝區中每個以 null 結束的字串都包含驅動程式相依的檔案名。 字串序列會以空的零長度字串來終止。 如果 **pDependentFiles** 不是 **Null** ，而且不包含任何檔案名，則會指向包含兩個空字串的緩衝區。

</dd> <dt>

**pMonitorName**
</dt> <dd>

指定語言監視器 (之以 null 結束的字串指標，例如「PJL 監視器」 ) 。 這個成員可以是 **Null** ，而且只能針對能夠進行雙向通訊的印表機指定。

</dd> <dt>

**pDefaultDataType**
</dt> <dd>

以 null 結束的字串指標，指定列印工作的預設資料類型 (例如 "EMF" ) 。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 驅動程式 \_ 資訊 \_ 3w 法** (Unicode) 和 **\_ 驅動程式 \_ 資訊 \_ 3a** (ANSI) <br/>                             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

 




