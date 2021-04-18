---
description: Mid 方法會從 CHString 字串解壓縮長度 nCount 字元的子字串，從位置 nFirst 開始， (以零為基礎的) 。 方法會傳回已解壓縮之子字串的複本。
audience: developer
ms.assetid: 2036813b-f991-4ca3-95d3-8bbe858aae09
ms.tgt_platform: multiple
title: 'CHString：： Mid 方法 (ChString .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5d05259128f80bcb21d00144d19002ca58ce39c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989466"
---
# <a name="chstringmid-methods"></a>CHString：： Mid 方法

\[[**CHString**](chstring.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。 [MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]

**Mid** 方法會從 [**CHString**](chstring.md)字串解壓縮長度 *nCount* 字元的子字串，從位置 *nFirst* 開始， (以零為基礎的) 。 方法會傳回已解壓縮之子字串的複本。

### <a name="overload-list"></a>多載清單



| 方法                                        | 描述                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [**Mid (int，int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int_int)) | 解壓縮指定長度和起點的子字串。<br/> |
| [**Mid (int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))         | 從 int 開始解壓縮子字串。<br/>                        |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                                                                      |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                                                                                |
| 標頭<br/>                   | <dl> <dt>ChString (包含 FwCommon) </dt> </dl>                                                    |
| 程式庫<br/>                  | <dl> <dt>FrameDyn .lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt> </dl> |



�

�
