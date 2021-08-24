---
description: WBEMTime 類別的函式可加速各種 Windows 和 ANSI C 執行時間時間格式之間的轉換。
audience: developer
ms.assetid: 8b0ce221-2186-4aed-a474-00f88cef6350
ms.tgt_platform: multiple
title: 'WBEMTime：： WBEMTime (WbemTime .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: ac02e3ee2a7a77ed1cc2cc9157b0d6c191563f234bf594cb53029a76e76f0137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757618"
---
# <a name="wbemtimewbemtime-constructors"></a>WBEMTime：： WBEMTime 的函式

\[[**WBEMTime**](wbemtime.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。 [MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]

**WBEMTime** 類別的函式可加速各種 Windows 和 ANSI C 執行時間時間格式之間的轉換。

### <a name="overload-list"></a>多載清單



| 建構函式                                                                 | 描述                                                               |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**WBEMTime ()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))                                   | 建立未初始化的時間物件。<br/>                          |
| [**WBEMTime (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))                           | 將新的時間物件初始化為參數中的值。<br/> |
| [**WBEMTime (const time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_))        | 將新的時間物件初始化為參數中的值。<br/> |
| [**WBEMTime (const 結構 tm)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_))    | 將新的時間物件初始化為參數中的值。<br/> |
| [**WBEMTime (const FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_))     | 將新的時間物件初始化為參數中的值。<br/> |
| [**WBEMTime (const SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_)) | 將新的時間物件初始化為參數中的值。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                                                                      |
| 最低支援的伺服器<br/> | Windows伺服器2008<br/>                                                                                                                                |
| 標頭<br/>                   | <dl> <dt>WbemTime。h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt> </dl> |



�

�
