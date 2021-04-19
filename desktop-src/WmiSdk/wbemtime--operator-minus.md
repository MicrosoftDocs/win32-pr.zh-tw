---
description: WBEMTime 類別減法運算子 (&\# 8211; ) 已多載至：
audience: developer
ms.assetid: 0fa51aab-7ea2-4af7-bb12-1646388b0405
ms.tgt_platform: multiple
title: 'WBEMTime：： operator-運算子 (WbemTime .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 39256ba9d922ea9d3eef8e442115e840b963ca71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983912"
---
# <a name="wbemtimeoperator--operators"></a>WBEMTime：： operator-運算子

\[[**WBEMTime**](wbemtime.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。 [MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]

[**WBEMTime**](wbemtime.md)類別減法運算子 () 已多載至：

-   從物件的時間減去時間範圍，以產生包含所產生時間的新時間物件。
-   從物件的時間減去時間，以產生新的時間範圍物件，其中包含兩次之間的差異。

### <a name="overload-list"></a>多載清單



| 運算子                                                                         | 描述                                                                      |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**operator- (WBEMTime&)**](/windows/win32/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize)         | 從 **WBEMTime** 減去 **WBEMTime** 。<br/>                         |
| [**operator- (WBEMTimeSpan&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_)) | 從 **WBEMTime** 減去 [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) 。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                                                                      |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                                                                                |
| 標頭<br/>                   | <dl> <dt>WbemTime。h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt> </dl> |



�

�
