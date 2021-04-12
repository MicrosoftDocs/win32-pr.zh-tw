---
description: WBEMTime 類別指派運算子會進行多載，以加速各種 Windows 和 ANSI C 執行時間時間格式之間的轉換。 不同的多載簽章如下所示。
audience: developer
ms.assetid: 47978056-d46f-4f8f-99cb-8463b44da7cf
ms.tgt_platform: multiple
title: 'WBEMTime：： operator = 運算子 (WbemTime .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 637cc76e776060a4c36a12a9b26bd09a6c231a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320820"
---
# <a name="wbemtimeoperator-operators"></a>WBEMTime：： operator = 運算子

\[[**WBEMTime**](wbemtime.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。 [MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]

[**WBEMTime**](wbemtime.md)類別指派運算子會進行多載，以加速各種 WINDOWS 和 ANSI C 執行時間時間格式之間的轉換。 不同的多載簽章如下所示。

### <a name="overload-list"></a>多載清單



| 運算子                                                                     | 描述                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------|
| [**operator = (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))               | 將 **BSTR** 轉換成 **WBEMTime** 格式。<br/>         |
| [**operator = (時間 \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))        | 將 **時間 \_ t** 轉換成 **WBEMTime** 格式。<br/>        |
| [**operator = (FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))     | 將 **FILETIME** 轉換成 **WBEMTime** 格式。<br/>       |
| [**operator = (結構 tm&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))   | 將 **tm** 結構轉換為 **WBEMTime** 格式。<br/> |
| [**operator = (SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_)) | 將 **SYSTEMTIME** 轉換為 **WBEMTime** 格式。<br/>     |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                                                                      |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                                                                                |
| 標頭<br/>                   | <dl> <dt>WbemTime。h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt> </dl> |



�

�
