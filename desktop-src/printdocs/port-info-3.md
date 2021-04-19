---
description: PORT \_ INFO \_ 3 結構會指定印表機埠的狀態值。
ms.assetid: 0939353f-284b-4dbb-89a2-04918c934430
title: 'PORT_INFO_3 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_3
- _PORT_INFO_3A
- _PORT_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 49888ee6410f39745b848bbbf7fd95fa329c6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992042"
---
# <a name="port_info_3-structure"></a>埠 \_ 資訊 \_ 3 結構

**PORT \_ INFO \_ 3** 結構會指定印表機埠的狀態值。

## <a name="syntax"></a>語法


```C++
typedef struct _PORT_INFO_3 {
  DWORD  dwStatus;
  LPTSTR pszStatus;
  DWORD  dwSeverity;
} PORT_INFO_3, *PPORT_INFO_3;
```



## <a name="members"></a>成員

<dl> <dt>

**dwStatus**
</dt> <dd>

新的埠狀態值。 只有當 **pszStatus** 成員是 **Null** 時，才會使用這個值。

這個成員可以是下列其中一個值。



| 值                            | 意義                                             |
|----------------------------------|-----------------------------------------------------|
| 0                                | 清除印表機埠狀態。                     |
| \_離線埠狀態 \_            | 埠的印表機已離線。                      |
| 埠 \_ 狀態 \_ 紙 \_ 紙         | 埠的印表機有紙紙。                 |
| 埠 \_ 狀態 \_ 紙張 \_ 輸出         | 埠的印表機缺紙。                 |
| 埠 \_ 狀態 \_ 輸出 \_ BIN 已 \_ 滿  | 埠的 printer's 輸出 bin 已滿。            |
| 埠 \_ 狀態 \_ 紙張 \_ 問題     | 埠的印表機有紙張問題。             |
| \_ \_ 無 \_ 墨粉的埠狀態          | 埠的印表機已缺墨粉。                 |
| 埠 \_ 狀態 \_ 門 \_ 開啟         | 埠的印表機門已開啟。             |
| 埠 \_ 狀態 \_ 使用者 \_ 介入 | 埠的印表機需要使用者介入。      |
| 埠 \_ 狀態 \_ \_ 記憶體不足 \_    | 埠的印表機記憶體不足。                |
| 埠 \_ 狀態 \_ 墨粉 \_ 低         | 埠的印表機碳粉不足。                 |
| 埠 \_ 狀態 \_ 預熱 \_        | 埠的印表機正在準備。                   |
| 埠 \_ 狀態省 \_ 電 \_        | 埠的印表機會處於電源節省模式。 |



 

</dd> <dt>

**pszStatus**
</dt> <dd>

要設定的新印表機埠狀態值字串指標。 如果針對 **dwStatus** 所列的值沒有適當的狀態值，請使用這個成員。

</dd> <dt>

**dwSeverity**
</dt> <dd>

埠狀態值的嚴重性。

這個成員可以是下列其中一個值。



| 值                       | 意義                                   |
|-----------------------------|-------------------------------------------|
| 埠 \_ 狀態 \_ 類型 \_ 錯誤   | 埠狀態值表示錯誤。 |
| 埠 \_ 狀態 \_ 類型 \_ 警告 | 埠狀態值是警告。       |
| 埠 \_ 狀態 \_ 類型 \_ 資訊    | 埠狀態值為 [資訊]。   |



 

</dd> </dl>

## <a name="remarks"></a>備註

當您設定 [印表機埠狀態值] 的 [嚴重性值埠 \_ 狀態 \_ 類型] \_ 錯誤時，列印多工緩衝處理器會停止將作業傳送至埠。 列印多工緩衝處理器不會繼續將作業傳送到埠，直到進行另一個 [**SetPort**](setport.md) 呼叫以清除狀態為止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 埠 \_ 資訊 \_ 3w 法** (Unicode) 和 **\_ 埠 \_ 資訊 \_ 3a** (ANSI) <br/>                                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**SetPort**](setport.md)
</dt> </dl>

 

 




