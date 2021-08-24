---
description: 多載的 FormatMessageW 方法會將訊息字串格式化。
audience: developer
ms.assetid: 45780467-d3aa-4927-aa53-60e5ee277c27
ms.tgt_platform: multiple
title: 'CHString：： FormatMessageW 方法 (ChString .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 53f8a9663994ffbc6b50aebddc7d9877c17c1067a074bcdddbe2fc79bc525e99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050936"
---
# <a name="chstringformatmessagew-methods"></a>CHString：： FormatMessageW 方法

\[[**CHString**](chstring.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。 [MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]

多載的 **FormatMessageW** 方法會將訊息字串格式化。

### <a name="overload-list"></a>多載清單



| 方法                                                              | 描述                                                                                     |
|:--------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**FormatMessageW (UINT)**](/previous-versions/windows/desktop/legacy/aa385519(v=vs.85))       | 根據 **UINT** 指定的資源識別碼來格式化此訊息。<br/> |
| [**FormatMessageW (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-formatmessagew(lpcwstr_---)) | 根據 **LPCWSTR** 所指定的格式來格式化此訊息字串。<br/>    |



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
