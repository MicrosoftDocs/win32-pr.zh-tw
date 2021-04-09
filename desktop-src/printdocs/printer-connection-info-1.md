---
description: 代表印表機連接的相關資訊。
ms.assetid: afac3f91-74eb-46f7-94b4-d37b2b8a32a4
title: 'PRINTER_CONNECTION_INFO_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_CONNECTION_INFO_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 04bfb5411a5602248bcd188d07dec8478462fd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693563"
---
# <a name="printer_connection_info_1-structure"></a>印表機 \_ 連接 \_ 資訊 \_ 1 結構

代表印表機連接的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _PRINTER_CONNECTION_INFO_1 {
  DWORD  dwFlags;
  LPTSTR pszDriverName;
} PRINTER_CONNECTION_INFO_1, *PPRINTER_CONNECTION_INFO_1;
```



## <a name="members"></a>成員

<dl> <dt>

**dwFlags**
</dt> <dd>

系統會定義下列值：



| 值                                      | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ (0x00000020) 的印表機連接不相符 | 如果設定此位旗標，則印表機連接不相符。 使用者可以提供本機列印驅動程式做為 *pszDriverName* ，並使用它來進行轉譯，而不是使用安裝在使用者所連接之伺服器印表機上的驅動程式。<br/>                                                                                                                                                                                                                                    |
| 印表機 \_ 連線 \_ 沒有 \_ UI (0x00000040)    | 如果設定此位旗標，則此呼叫無法顯示對話方塊。 如果必須顯示對話方塊以從伺服器安裝印表機驅動程式，且已設定此位旗標，則不會安裝印表機驅動程式，也不會新增印表機連線，而且呼叫會失敗。<br/> **Windows 7：** 在 Windows 7 和更新版本的 Windows 中，如果已設定這個旗標，而且使用者是在提高許可權的模式下執行，就不會顯示 [ **您信任此印表機嗎？** ] 對話方塊。<br/> |



 

</dd> <dt>

**pszDriverName**
</dt> <dd>

驅動程式名稱的指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




