---
description: 驅動程式 \_ 資訊 \_ 4 結構包含印表機驅動程式資訊。
ms.assetid: 63000de6-74e7-4427-98d7-7bbd2dd61080
title: 'DRIVER_INFO_4 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_4
- _DRIVER_INFO_4A
- _DRIVER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d42f74ce58c126130bd28820283c0b4262d3e3ce6b05106ae9ff74bc280ae234
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119353928"
---
# <a name="driver_info_4-structure"></a>驅動程式 \_ 資訊 \_ 4 結構

**驅動程式 \_ 資訊 \_ 4** 結構包含印表機驅動程式資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _DRIVER_INFO_4 {
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
  LPTSTR pszzPreviousNames;
} DRIVER_INFO_4, *PDRIVER_INFO_4;
```



## <a name="members"></a>成員

<dl> <dt>

**cVersion**
</dt> <dd>

寫入驅動程式的作業系統版本。 支援的值為3。

</dd> <dt>

**pName**
</dt> <dd>

以 null 結束的字串指標，指定驅動程式的名稱 (例如 "QMS 810" ) 。

</dd> <dt>

**pEnvironment**
</dt> <dd>

以 null 結束的字串指標，指定寫入驅動程式的環境 (例如 Windows x86、Windows IA64 和 Windows x64) 。

</dd> <dt>

**pDriverPath**
</dt> <dd>

以 null 結束的字串指標，指定包含設備磁碟機之檔案的檔案名或完整路徑和檔案名 (例如，C： \\ 驅動程式 \\Pscript.dll) 。

</dd> <dt>

**pDataFile**
</dt> <dd>

以 null 結束的字串指標，指定包含驅動程式資料之檔案的檔案名或完整路徑和檔案名 (例如，C： \\ 驅動程式 \\ Qms810) 。

</dd> <dt>

**pConfigFile**
</dt> <dd>

以 null 結束的字串指標，指定設備磁碟機設定動態連結程式庫的檔案名或完整路徑和檔案名 (例如 C： \\ 驅動程式 \\Pscrptui.dll) 。

</dd> <dt>

**pHelpFile**
</dt> <dd>

以 null 結束的字串指標，指定設備磁碟機的說明檔的檔案名或完整路徑和檔案名。

</dd> <dt>

**pDependentFiles**
</dt> <dd>

MultiSZ 緩衝區的指標，其中包含以 null 終止之字串的序列。 緩衝區中每個以 null 結束的字串都包含驅動程式相依的檔案名。 字串序列會以空的零長度字串來終止。 如果 **pDependentFiles** 不是 **Null** ，而且不包含任何檔案名，則會指向包含兩個空字串的緩衝區。

</dd> <dt>

**pMonitorName**
</dt> <dd>

指定語言監視器 (之以 null 結束的字串指標，例如 PJL 監視器) 。 這個成員可以是 **Null** ，而且只能針對能夠進行雙向通訊的印表機指定。

</dd> <dt>

**pDefaultDataType**
</dt> <dd>

以 null 結束的字串指標，指定列印工作的預設資料類型 (例如，EMF) 。

</dd> <dt>

**pszzPreviousNames**
</dt> <dd>

以 null 結束的字串指標，這個字串會指定與此驅動程式相容的先前印表機驅動程式名稱。 例如，OldName1 \\ 0OldName2 \\ 0 \\ 0。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 驅動程式 \_ 資訊 \_ 4W** (Unicode) 和 **\_ 驅動程式 \_ 資訊 \_ 4a** (ANSI) <br/>                             |



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

 

 




