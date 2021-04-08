---
description: GetLocalOffsetForDate 方法會傳回以分鐘為單位的位移 (+ 或 &\# 8211; 在引數中提供的時間內，) GMT 和本地時間之間的位移。
audience: developer
ms.assetid: 15cc5f45-604c-4335-bcd3-92d62dc15420
ms.tgt_platform: multiple
title: 'WBEMTime：： GetLocalOffsetForDate 方法 (WbemTime .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e2c10cd076e18a803f0cb22b2798c09091cc70b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850744"
---
# <a name="wbemtimegetlocaloffsetfordate-methods"></a>WBEMTime：： GetLocalOffsetForDate 方法

\[[**WBEMTime**](wbemtime.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。 [MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]

**GetLocalOffsetForDate** 方法會傳回引數中所提供時間的時差（以分鐘為單位） (+ 或) 之間的時差和本地時間。

### <a name="overload-list"></a>多載清單



| 方法                                                                                           | 描述                                           |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| [**GetLocalOffsetForDate (time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(consttime_t_))         | 引數是 **時間 \_ t** 的參考。<br/>  |
| [**GetLocalOffsetForDate (FILETIME \*)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constfiletime))     | 引數是 **FILETIME** 的指標。<br/>   |
| [**GetLocalOffsetForDate (結構 tm \*)**](/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getstructtm)   | 引數是 **tm** 結構的指標。<br/> |
| [**GetLocalOffsetForDate (SYSTEMTIME \*)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constsystemtime)) | 引數是指向 **SYSTEMTIME** 的指標。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                                                                      |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                                                                                |
| 標頭<br/>                   | <dl> <dt>WbemTime。h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt> </dl> |



�

�
