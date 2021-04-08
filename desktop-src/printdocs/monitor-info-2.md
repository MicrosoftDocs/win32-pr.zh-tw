---
description: 監視器 \_ 資訊 \_ 2 結構會識別監視。
ms.assetid: 4dd1ca15-6983-403e-8159-1a6d35a88162
title: 'MONITOR_INFO_2 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_2
- _MONITOR_INFO_2A
- _MONITOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 9d3ad70a0728ca6e73c4dbefb248df58e858a996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695079"
---
# <a name="monitor_info_2-structure"></a>監視 \_ INFO \_ 2 結構

**監視器 \_ 資訊 \_ 2** 結構會識別監視。

## <a name="syntax"></a>語法


```C++
typedef struct _MONITOR_INFO_2 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} MONITOR_INFO_2, *PMONITOR_INFO_2;
```



## <a name="members"></a>成員

<dl> <dt>

**pName**
</dt> <dd>

以 null 結束的字串指標，也就是監視的名稱。

</dd> <dt>

**pEnvironment**
</dt> <dd>

以 null 結束的字串指標，可指定用來寫入監視器的環境 (例如 Windows NT x86、Windows IA64、Windows x64) 。

</dd> <dt>

**pDLLName**
</dt> <dd>

以 null 結束的字串指標，該字串為監視器 DLL 的名稱。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 監視器 \_ 資訊 \_ 2w** (Unicode) 和 **\_ 監視 \_ 資訊 \_ 2a** (ANSI) <br/>                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddMonitor**](addmonitor.md)
</dt> <dt>

[**EnumMonitors**](enummonitors.md)
</dt> <dt>

[**監視 \_ 資訊 \_ 1**](monitor-info-1.md)
</dt> </dl>

 

 




