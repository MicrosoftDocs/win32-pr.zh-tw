---
description: 下列每個函式都會使用指定的資料來初始化新的 CHString 物件。
audience: developer
ms.assetid: d49e1600-d5d4-4c44-81c5-1b8c53b768de
ms.tgt_platform: multiple
title: 'CHString：： CHString (ChString .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 80ce10988fc335c5a16eff8507346dbcdffd6fa70f75d74fb48d3f84b0e2332b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320046"
---
# <a name="chstringchstring-constructors"></a>CHString：： CHString 的函式

\[[**CHString**](chstring.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。 [MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]

下列每個函式都會使用指定的資料來初始化新的 [**CHString**](chstring.md) 物件。

### <a name="overload-list"></a>多載清單



| 建構函式                                                                        | 描述                                                  |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------|
| [**CHString ()**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                          | 建立空的 CHString 物件。<br/>                 |
| [**CHString (LPCSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcstr))                              | 使用 LPCSTR 值初始化。<br/>                |
| [**CHString (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr))                            | 使用 LPCWSTR 值初始化。<br/>               |
| [**CHString (WCHAR，int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(wchar_int))                        | 使用 WCHAR 值的 int 複本進行初始化。<br/>   |
| [**CHString (LPCWSTR，int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr_int))                    | 使用 LPCWSTR 值的 int 複本進行初始化。<br/> |
| [**CHString (const CHString&)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constchstring_))            | 複寫 CHString 參數。<br/>                |
| [**CHString (const 不帶正負號的 char \*)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constunsignedchar)) | 使用 char 所指向的值進行初始化 \* 。<br/>  |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                                                                      |
| 最低支援的伺服器<br/> | Windows伺服器2008<br/>                                                                                                                                |
| 標頭<br/>                   | <dl> <dt>ChString (包含 FwCommon) </dt> </dl>                                                    |
| 程式庫<br/>                  | <dl> <dt>FrameDyn .lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt> </dl> |



�

�
