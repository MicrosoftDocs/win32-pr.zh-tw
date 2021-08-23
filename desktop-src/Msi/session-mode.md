---
description: 這是會話物件的 Mode 屬性。 這個屬性是一個值，代表目前安裝會話的指定模式旗標。 大部分的模式旗標在外部是唯讀的，但您也可以設定幾個指定的旗標。
ms.assetid: 9aca413d-d653-4ec1-a39b-af956f6c95e7
title: Session. Mode 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Mode
api_type:
- COM
api_location: ''
ms.openlocfilehash: ed0c24280307cf368239ab88b5357924a3ee40d5a62444838e155aca2c0642f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629118"
---
# <a name="sessionmode-property"></a>Session. Mode 屬性

這是 [**會話**](session-object.md)物件的 **Mode** 屬性。 這個屬性是一個值，代表目前安裝會話的指定模式旗標。 大部分的模式旗標在外部是唯讀的，但您也可以設定幾個指定的旗標。

[**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)函式會傳回布林值 TRUE 或 FALSE，指出傳遞至函式的特定屬性目前是否已設定 (TRUE) 或未設定 (FALSE) 。

請注意，從延遲的自訂動作呼叫 **mode** 屬性時，不會提供 *旗* 標的所有執行模式值。 如需詳細資訊，請參閱 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Session.Mode
```



## <a name="property-value"></a>屬性值

旗標的必要整數值。 必須是下列其中之一：



| 旗標名稱                                                                                                                                                                                                                                                                                                | 意義                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiRunModeAdmin"></span><span id="msirunmodeadmin"></span><span id="MSIRUNMODEADMIN"></span><dl> <dt>**msiRunModeAdmin**</dt> <dt>0</dt> </dl>                                              | 系統管理模式安裝，否則為產品安裝。<br/>                                  |
| <span id="msiRunModeAdvertise"></span><span id="msirunmodeadvertise"></span><span id="MSIRUNMODEADVERTISE"></span><dl> <dt>**msiRunModeAdvertise**</dt> <dt>1</dt> </dl>                              | 安裝的公告模式。<br/>                                                          |
| <span id="msiRunModeMaintenance"></span><span id="msirunmodemaintenance"></span><span id="MSIRUNMODEMAINTENANCE"></span><dl> <dt>**msiRunModeMaintenance**</dt> <dt>2</dt> </dl>                      | 已載入維護模式資料庫。<br/>                                                   |
| <span id="msiRunModeRollbackEnabled"></span><span id="msirunmoderollbackenabled"></span><span id="MSIRUNMODEROLLBACKENABLED"></span><dl> <dt>**msiRunModeRollbackEnabled**</dt> <dt>3</dt> </dl>      | 已啟用復原。<br/>                                                                |
| <span id="msiRunModeLogEnabled"></span><span id="msirunmodelogenabled"></span><span id="MSIRUNMODELOGENABLED"></span><dl> <dt>**msiRunModeLogEnabled**</dt> <dt>4</dt> </dl>                          | 記錄檔正在使用中。<br/>                                                                 |
| <span id="msiRunModeOperations"></span><span id="msirunmodeoperations"></span><span id="MSIRUNMODEOPERATIONS"></span><dl> <dt>**msiRunModeOperations**</dt> <dt>5</dt> </dl>                          | 執行或幕後處理作業。<br/>                                                   |
| <span id="msiRunModeRebootAtEnd"></span><span id="msirunmoderebootatend"></span><span id="MSIRUNMODEREBOOTATEND"></span><dl> <dt>**msiRunModeRebootAtEnd**</dt> <dt>6</dt> </dl>                      |  (可設定的) 需要重新開機。<br/>                                                        |
| <span id="msiRunModeRebootNow"></span><span id="msirunmoderebootnow"></span><span id="MSIRUNMODEREBOOTNOW"></span><dl> <dt>**msiRunModeRebootNow**</dt> <dt>7</dt> </dl>                              | 需要重新開機才能繼續安裝 (可設定的) 。<br/>                               |
| <span id="msiRunModeCabinet"></span><span id="msirunmodecabinet"></span><span id="MSIRUNMODECABINET"></span><dl> <dt>**msiRunModeCabinet**</dt> <dt>8</dt> </dl>                                      | 使用媒體資料表從封包和檔案安裝檔案。<br/>                         |
| <span id="msiRunModeSourceShortNames"></span><span id="msirunmodesourceshortnames"></span><span id="MSIRUNMODESOURCESHORTNAMES"></span><dl> <dt>**msiRunModeSourceShortNames**</dt> <dt>9</dt> </dl>  | 來源檔案只使用簡短的檔案名。<br/>                                             |
| <span id="msiRunModeTargetShortNames"></span><span id="msirunmodetargetshortnames"></span><span id="MSIRUNMODETARGETSHORTNAMES"></span><dl> <dt>**msiRunModeTargetShortNames**</dt> <dt>10</dt> </dl> | 目標檔案只會使用簡短的檔案名。<br/>                                      |
| <span id="msiRunModeWindows9x"></span><span id="msirunmodewindows9x"></span><span id="MSIRUNMODEWINDOWS9X"></span><dl> <dt>**msiRunModeWindows9x**</dt> <dt>12</dt> </dl>                             | 作業系統 Windows 98/95。<br/>                                                  |
| <span id="msiRunModeZawEnabled"></span><span id="msirunmodezawenabled"></span><span id="MSIRUNMODEZAWENABLED"></span><dl> <dt>**msiRunModeZawEnabled**</dt> <dt>13</dt> </dl>                         | 作業系統支援產品的廣告。<br/>                                  |
| <span id="msiRunModeScheduled"></span><span id="msirunmodescheduled"></span><span id="MSIRUNMODESCHEDULED"></span><dl> <dt>**msiRunModeScheduled**</dt> <dt>16</dt> </dl>                             | 從安裝腳本執行呼叫的延後 [自訂動作](custom-actions.md) 。<br/>  |
| <span id="msiRunModeRollback"></span><span id="msirunmoderollback"></span><span id="MSIRUNMODEROLLBACK"></span><dl> <dt>**msiRunModeRollback**</dt> <dt>17</dt> </dl>                                 | 從復原執行腳本呼叫的延後 [自訂動作](custom-actions.md) 。<br/> |
| <span id="msiRunModeCommit"></span><span id="msirunmodecommit"></span><span id="MSIRUNMODECOMMIT"></span><dl> <dt>**msiRunModeCommit**</dt> <dt>18</dt> </dl>                                         | 從認可執行腳本呼叫的延後 [自訂動作](custom-actions.md) 。<br/>   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |



 

 




