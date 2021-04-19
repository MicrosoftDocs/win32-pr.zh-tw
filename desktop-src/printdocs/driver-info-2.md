---
description: 驅動程式 \_ 資訊 \_ 2 結構會識別印表機驅動程式、驅動程式版本號碼、寫入驅動程式的環境、儲存驅動程式的檔案名等等。
ms.assetid: cca1227d-69b9-44df-8dac-384c2f8843ae
title: 'DRIVER_INFO_2 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_2
- _DRIVER_INFO_2A
- _DRIVER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: a88caf5aa10828b81dccefbe8118b3a57aebce97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976872"
---
# <a name="driver_info_2-structure"></a>驅動程式 \_ 資訊 \_ 2 結構

**驅動程式 \_ 資訊 \_ 2** 結構會識別印表機驅動程式、驅動程式版本號碼、寫入驅動程式的環境、儲存驅動程式的檔案名等等。

## <a name="syntax"></a>語法


```C++
typedef struct _DRIVER_INFO_2 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
} DRIVER_INFO_2, *PDRIVER_INFO_2;
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

以 null 結束的字串指標，指定寫入驅動程式的環境 (例如，Windows x86、Windows IA64 和 Windows x64) 。

</dd> <dt>

**pDriverPath**
</dt> <dd>

以 null 結束的字串指標，指定包含設備磁碟機之檔案的檔案名或完整路徑和檔案名 (例如 "c： \\ 驅動程式 \\pscript.dll" ) 。

</dd> <dt>

**pDataFile**
</dt> <dd>

以 null 結束的字串指標，指定包含驅動程式資料之檔案的檔案名或完整路徑和檔案名 (例如 "c： \\ 驅動程式 \\ Qms810" ) 。

</dd> <dt>

**pConfigFile**
</dt> <dd>

以 null 結束的字串指標，指定設備磁碟機設定 .dll 的檔案名或完整路徑和檔案名 (例如 "c： driver \\ \\Pscrptui.dll" ) 。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 驅動程式 \_ 資訊 \_ 2w** (Unicode) 和 **\_ 驅動程式 \_ 資訊 \_ 2a** (ANSI) <br/>                             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

 




