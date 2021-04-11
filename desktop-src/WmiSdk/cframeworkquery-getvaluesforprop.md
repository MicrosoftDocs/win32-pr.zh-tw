---
description: GetValuesForProp 方法會傳回該屬性在查詢中所產生之特定屬性的所有值。
audience: developer
ms.assetid: b5ed4b48-f622-4a55-897d-d800ada0270f
ms.tgt_platform: multiple
title: 'CFrameworkQuery：： GetValuesForProp 方法 (FrQuery .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b5fd9dbc22289843141c517203809045abbf05a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193879"
---
# <a name="cframeworkquerygetvaluesforprop-methods"></a>CFrameworkQuery：： GetValuesForProp 方法

\[[**CFrameworkQuery**](/windows/win32/api/frquery/nl-frquery-cframeworkquery)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。 [MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]

**GetValuesForProp** 方法會傳回該屬性在查詢中所產生之特定屬性的所有值。

例如，對 **GetValuesForProp** (L "name"、sa) 的呼叫會傳回陣列 *sa*，其中包含所有需要傳回實例以滿足查詢的 "Name" 值。 如果 *sa* 包含 {"a"，"b"}，則為 "name = b" 加上所有實例的所有實例，其中 "name = b" 必須送回以完全符合查詢。

如果「名稱」的條件約束沒有足夠的限制，則會傳回空的 *sa* 陣列。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                             | 描述                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetValuesForProp (CHStringArray&、LPCWSTR)**](/windows/win32/api/frquery/nf-frquery-cframeworkquery-getvaluesforprop(lpcwstr_chstringarray_))                      | 傳回該屬性在查詢中出現時所產生之特定屬性的所有值。<br/> |
| [**GetValuesForProp (LPCWSTR，std：： vector &lt; \_ bstr \_ t &gt;&)**](/windows/win32/api/frquery/nf-frquery-cframeworkquery-getvaluesforprop(lpcwstr_std-vector__bstr_t__)) | 傳回該屬性在查詢中出現時所產生之特定屬性的所有值。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                                                                      |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                                                                                |
| 標頭<br/>                   | <dl> <dt>FrQuery (包含 FwCommon) </dt> </dl>                                                     |
| 程式庫<br/>                  | <dl> <dt>FrameDyn .lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt> </dl> |



�

�
