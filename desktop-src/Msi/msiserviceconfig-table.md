---
description: MsiServiceConfig 資料表會設定由目前封裝安裝或安裝的服務。
ms.assetid: 0d9fd005-9326-4a18-8496-35b5d1927f47
title: MsiServiceConfig 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b72e21fdfecd59780b862d3bfe7d68ef829b59b847dbceb0e9c13befae9d4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828588"
---
# <a name="msiserviceconfig-table"></a>MsiServiceConfig 資料表

MsiServiceConfig 資料表會設定由目前封裝安裝或安裝的服務。

**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。 從 Windows Installer 5.0 開始，可以使用此資料表。

MsiServiceConfig 資料表具有下列資料行。



| Column           | 類型                         | 答案 | Nullable |
|------------------|------------------------------|-----|----------|
| MsiServiceConfig | [識別碼](identifier.md) | Y   | N        |
| 名稱             | [格式 化](formatted.md)   | N   | N        |
| 事件            | [整數](integer.md)       | N   | N        |
| ConfigType       | [整數](integer.md)       | N   | N        |
| 引數         | [格式 化](formatted.md)   | N   | Y        |
| 元件\_      | [識別碼](identifier.md) | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="MsiServiceConfig"></span><span id="msiserviceconfig"></span><span id="MSISERVICECONFIG"></span>MsiServiceConfig
</dt> <dd>

這是此資料表的主要索引鍵。

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>名字
</dt> <dd>

此資料行包含屬於此封裝或已安裝之服務的名稱。

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>事件
</dt> <dd>

這個資料行會指定變更服務設定的時機。 下列值可以合併以表示多個作業。 包含的任何值都會被忽略。



| 常數                                         | 描述                                              |
|--------------------------------------------------|----------------------------------------------------------|
| **msidbServiceConfigEventInstall** 1<br/>   | 在元件安裝期間採取動作。   |
| **msidbServiceConfigEventUninstall** 2<br/> | 在元件卸載期間採取動作。 |
| **msidbServiceConfigEventReinstall** 4<br/> | 在元件重新安裝期間採取動作。 |



 

</dd> <dt>

<span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>名稱 configtype
</dt> <dd>

此欄位中的值與 [引數] 欄位中的值結合，可指定要對服務設定進行的變更。 指定的變更會在系統下次啟動時生效。



| Config                                                      | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **服務 \_設定 \_ 延遲 \_ 自動 \_ 啟動** 3<br/>       | 設定 [自動啟動服務](../services/automatically-starting-services.md)的時間延遲。 <br/> 在 [引數] 欄位中輸入1，以在其他自動啟動服務加上時間延遲之後啟動服務。 <br/> 在 [引數] 欄位中輸入0，以關閉自動啟動服務延遲。<br/> 僅適用于已安裝的自動啟動服務，或此封裝所安裝的服務，以及 [ServiceInstall 資料表](serviceinstall-table.md)的 StartType 欄位中的 **服務 \_ 自動 \_ 啟動**。<br/>                                                                         |
| **服務 \_CONFIG \_ REQUIRED \_ 許可權 \_ 資訊** 6<br/> | 變更服務所需的許可權清單。<br/> 在 [引數] 欄位中輸入要求的許可權清單。 [引數] 欄位中的 [格式化](formatted.md) 字串值會列出所要求之許可權的 [**許可權常數**](../secauthz/privilege-constants.md) 。 您可以使用 \[ ~ \] [格式化](formatted.md)字串的語法來插入 null 字元。 分隔清單中的許可權常數 \[ ~ \] 。<br/>                                                                                                                              |
| **服務 \_CONFIG \_ 服務 \_ SID \_ 資訊** 5<br/>         | 將服務 SID 類型新增至包含此服務的進程權杖。<br/> 在 [引數] 欄位中，為 [**服務 \_ sid \_ 資訊**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) 結構輸入有效的服務 sid 類型： **服務 sid 類型 [ \_ \_ \_ 無** ] (0x00) 、 **服務 \_ sid \_ 類型 \_ 限制** (0x03) 或 **服務 \_ sid \_ 類型 \_** [不受限制] (0x01) 。 <br/>                                                                                                                                                                                                                                              |
| **服務 \_CONFIG \_ PRESHUTDOWN \_ INFO** 7<br/>          | 設定 [服務控制管理員](../services/service-control-manager.md) (SCM) 等待的時間長度，再繼續進行其他關機作業。 SCM 會在將 **服務 \_ 控制 \_ PRESHUTDOWN** 通知傳送至服務之後等候這段時間。 <br/> 在 [引數] 欄位中輸入時間延遲長度（以毫秒為單位）。 將 [引數] 欄位保留為空白，以將時間延遲重設為預設值3分鐘。 <br/>                                                                                                                               |
| **服務 \_設定 \_ 失敗 \_ 動作 \_ 旗** 標4<br/>     | 設定何時執行此服務的失敗動作。 如果服務沒有設定的失敗動作，就會忽略此設定。<br/> 輸入0，只在服務終止但未 **\_ 停止 reporting service** 時執行動作。<br/> 輸入1以在服務終止報表 **服務 \_** 且 [**服務 \_ 狀態**](/windows/win32/api/winsvc/ns-winsvc-service_status)結構的 **dwWin32ExitCode** 成員不 **\_ 成功時** 執行動作。 如果服務在沒有報表服務的情況下終止，也 **會 \_** 執行設定的失敗動作。<br/> |



 

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>參數
</dt> <dd>

此欄位中的值與 [名稱 configtype] 欄位中的值結合，可指定要對服務設定進行的變更。 指定的變更會在系統下次啟動時生效。

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

[元件資料表](component-table.md)的元件資料行的外部索引鍵。

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

 

 
