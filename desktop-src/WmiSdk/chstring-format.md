---
description: Format 方法會格式化並將一連串的字元和值儲存在 CHString 字串中。
audience: developer
ms.assetid: 95d24b0e-3580-4a5d-8dad-50d44ef1ca39
ms.tgt_platform: multiple
title: 'CHString：： Format 方法 (ChString .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5432ac16b3e59b3f5e56d862a5bf66f5b23f732f74d586066584b6b937327830
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319937"
---
# <a name="chstringformat-methods"></a>CHString：： Format 方法

\[[**CHString**](chstring.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。 [MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]

**Format** 方法會格式化並將一連串的字元和值儲存在 [**CHString**](chstring.md)字串中。

### <a name="overload-list"></a>多載清單



| 方法                                              | 描述                                                                                      |
|:----------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**格式 (UINT)**](/previous-versions/windows/desktop/legacy/aa385532(v=vs.85))       | 根據 **UINT** 所指定的資源識別碼，將此 CHString 格式化。<br/> |
| [**(LPCWSTR 格式的格式)**](/windows/win32/api/chstring/nf-chstring-chstring-format(lpcwstr_---)) | 根據 **LPCWSTR** 所指定的格式，將這個 CHString 格式化。<br/>           |



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
