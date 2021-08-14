---
description: MsiServiceConfigFailureActions 資料表會列出服務失敗之後要執行的作業。 下表中指定的作業會在系統下次啟動時執行。
ms.assetid: 7c450b74-1f91-4a1c-beee-646a407eb8a8
title: MsiServiceConfigFailureActions 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907c0feb2e331c1e19ff4292d11cc58b65340a7543d9af5d0a1ccf23d2e80a48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944415"
---
# <a name="msiserviceconfigfailureactions-table"></a>MsiServiceConfigFailureActions 資料表

MsiServiceConfigFailureActions 資料表會列出服務失敗之後要執行的作業。 下表中指定的作業會在系統下次啟動時執行。

**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。 從 Windows Installer 5.0 開始，可以使用此資料表。

MsiServiceConfigFailureActions 資料表具有下列資料行。



| Column                         | 類型                         | 答案 | Nullable |
|--------------------------------|------------------------------|-----|----------|
| MsiServiceConfigFailureActions | [識別碼](identifier.md) | Y   | N        |
| Name                           | [格式 化](formatted.md)   | N   | N        |
| 事件                          | [整數](integer.md)       | N   | N        |
| ResetPeriod                    | [整數](integer.md)       | N   | Y        |
| RebootMessage                  | [格式 化](formatted.md)   | N   | Y        |
| Command                        | [格式 化](formatted.md)   | N   | Y        |
| 動作                        | [Text](text.md)             | N   | Y        |
| DelayActions                   | [Text](text.md)             | N   | Y        |
| 元件\_                    | [識別碼](identifier.md) | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>MsiServiceConfigFailureActions
</dt> <dd>

這是識別失敗動作之資料表的主要索引鍵。

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>名字
</dt> <dd>

此資料行包含屬於此封裝或已安裝之服務的名稱。

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>事件
</dt> <dd>

這個資料行會指定何時變更服務的設定。 下列值是可以結合以代表多個作業的位欄位。 任何其他位域值都會被忽略。



| 常數                                         | 描述                                     |
|--------------------------------------------------|-------------------------------------------------|
| **msidbServiceConfigEventInstall** 1<br/>   | 在元件安裝期間變更。    |
| **msidbServiceConfigEventUninstall** 2<br/> | 在元件卸載期間變更。  |
| **msidbServiceConfigEventReinstall** 4<br/> | 重新安裝元件期間的變更。 |



 

</dd> <dt>

<span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>ResetPeriod
</dt> <dd>

服務失敗計數的重設期間（以秒為單位）。 [服務控制管理員](../services/service-control-manager.md) (SCM) 計算自上次重新開機系統之後每個服務失敗的次數。 如果重設期間的服務不會失敗，則會將計數重設為零。 當服務在第 n 次失敗時，系統會在 [ \[ \] 動作] 欄位中指定之陣列的元素 N-1 執行指定的動作。

將 [ResetPeriod] 欄位保留為空白，表示永遠不會重設失敗計數。

</dd> <dt>

<span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>RebootMessage
</dt> <dd>

在重新開機電腦之前傳送給使用者的訊息，以回應 [動作] 資料行中指定的 **SC \_ 動作 \_ 重新開機** 動作。 您可以使用空字串 ""，以不變更的情況傳送目前的訊息。 您可以使用 \[ ~ \] [格式化](formatted.md)資料類型的語法來刪除目前的訊息，而不傳送任何訊息。

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>命令
</dt> <dd>

由 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數所建立的進程所執行的命令列，以回應 [動作] 資料行中指定的 **SC \_ action \_ run \_ 命令** 動作。 新的進程會在與服務相同的帳戶下執行，而且只有在 [動作] 欄位是 **SC \_ Action \_ RUN \_ 命令** 的情況下才會執行。 您可以使用空字串 ""，以不變更的情況使用目前的命令列。 您可以使用 \[ ~ \] [格式化](formatted.md)資料類型的語法來刪除目前的命令列，並在服務失敗時不執行任何操作。

</dd> <dt>

<span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>行動
</dt> <dd>

此欄位包含整數值的陣列，這些值會指定當服務失敗時，SCM 所採取的動作。 分隔陣列中的值 \[ ~ \] 。 陣列的第 n 個專案中的整數值會指定服務在第 n 次失敗時所執行的動作。 陣列的每個成員都是下列其中一個整數值。



| 常數                                 | 描述           |
|------------------------------------------|-----------------------|
| **SC \_動作 \_ 無** 0<br/>         | 不進行動作。            |
| **SC \_動作 \_ 重新開機** 2<br/>       | 重新啟動電腦。 |
| **SC \_動作 \_ 重新開機** 1<br/>      | 重新啟動服務。  |
| **SC \_動作 \_ 執行 \_ 命令** 3<br/> | 執行命令。        |



 

</dd> <dt>

<span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>DelayActions
</dt> <dd>

此欄位包含整數值的陣列，這些值會指定在執行動作資料行中指定的動作之前，要等候的時間（以毫秒為單位）。 分隔陣列中的值 \[ ~ \] 。 DelayActions 陣列中的元素數目必須等於動作陣列中的元素數目。 DelayActions 陣列的第 n 個元素會指定動作陣列第 n 個元素的時間延遲。

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

[元件資料表](component-table.md)中第一個資料行的外部索引鍵。

</dd> </dl>

## <a name="validation"></a>驗證

<dl>

[ICE102](ice-102.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 
