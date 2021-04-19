---
description: ServiceInstall 資料表是用來安裝服務，並具有下列資料行。
ms.assetid: 81688d31-e560-4dd0-8d84-efb50206c76e
title: ServiceInstall 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502583802a26c10bfd9572375149720c7c597f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992480"
---
# <a name="serviceinstall-table"></a>ServiceInstall 資料表

ServiceInstall 資料表是用來安裝服務，並具有下列資料行。



| Column         | 類型                               | 答案 | Nullable |
|----------------|------------------------------------|-----|----------|
| ServiceInstall | [識別碼](identifier.md)       | Y   | N        |
| Name           | [格式 化](formatted.md)         | N   | N        |
| DisplayName    | [格式 化](formatted.md)         | N   | Y        |
| ServiceType    | [DoubleInteger](doubleinteger.md) | N   | N        |
| StartType      | [DoubleInteger](doubleinteger.md) | N   | N        |
| ErrorControl   | [DoubleInteger](doubleinteger.md) | N   | N        |
| LoadOrderGroup | [格式 化](formatted.md)         | N   | Y        |
| 相依性   | [格式 化](formatted.md)         | N   | Y        |
| StartName      | [格式 化](formatted.md)         | N   | Y        |
| 密碼       | [格式 化](formatted.md)         | N   | Y        |
| 引數      | [格式 化](formatted.md)         | N   | Y        |
| 元件\_    | [識別碼](identifier.md)       | N   | N        |
| Description    | [格式 化](formatted.md)         | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="ServiceInstall"></span><span id="serviceinstall"></span><span id="SERVICEINSTALL"></span>ServiceInstall
</dt> <dd>

這是資料表的主要索引鍵。

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>名字
</dt> <dd>

此資料行是提供要安裝之服務名稱的字串。 字串的長度上限為256個字元。 服務控制管理員資料庫會保留服務名稱中字元的大小寫，但服務名稱的比較不區分大小寫。 正斜線 (/) 和反斜線 (\\) 是不正確服務名稱字元。

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>DisplayName
</dt> <dd>

此資料行是使用者介面程式用來識別服務的可當地語系化字串。 字串的長度上限為256個字元。 服務控制管理員會保留顯示名稱的大小寫，但顯示名稱比較不區分大小寫。

</dd> <dt>

<span id="ServiceType"></span><span id="servicetype"></span><span id="SERVICETYPE"></span>ServiceType
</dt> <dd>

此資料行是一組指定服務類型的位旗標。 必須在此資料行中指定下列其中一種服務類型。



| 服務類型                | 值      | 描述                                                                                                                                                                                                                  |
|--------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 服務 \_ WIN32 \_ 專屬 \_ 進程   | 0x00000010 | 執行自己的進程的 Microsoft Win32 服務。                                                                                                                                                                         |
| 服務 \_ WIN32 \_ 共用 \_ 進程 | 0x00000020 | 共用進程的 Win32 服務。                                                                                                                                                                                       |
| 服務 \_ 互動式 \_ 進程  | 0x00000100 | 與桌面互動的 Win32 服務。 這個值無法單獨使用，必須加入至上述兩個類型的其中一個。使用這個旗標時，StartName 資料行必須設定為 LocalSystem 或 null。<br/> |



 

不支援下列類型的服務。



| 服務類型               | 值      | 描述                   |
|-------------------------------|------------|-------------------------------|
| 服務 \_ 核心 \_ 驅動程式       | 0x00000001 | 驅動程式服務。             |
| 服務 \_ 檔 \_ 系統 \_ 驅動程式 | 0x00000002 | 檔案系統驅動程式服務。 |



 

</dd> <dt>

<span id="StartType"></span><span id="starttype"></span><span id="STARTTYPE"></span>StartType
</dt> <dd>

此資料行是一組位旗標，指定啟動服務的時機。 必須在此資料行中指定下列其中一種類型的服務啟動。



| 服務啟動類型  | 值      | 描述                                                                                                |
|------------------------|------------|------------------------------------------------------------------------------------------------------------|
| 服務 \_ 自動 \_ 啟動   | 0x00000002 | 服務會在系統啟動時啟動。                                                              |
| 服務 \_ 需求 \_ 開始 | 0x00000003 | 服務會在服務控制管理員呼叫 [**StartService**](/windows/win32/api/winsvc/nf-winsvc-startservicea) 函數時啟動。 |
| 服務 \_ 已停用      | 0x00000004 | 指定無法再啟動的服務。                                                         |



 

Windows Installer 無法使用服務 \_ 啟動 \_ 啟動和服務 \_ 系統 \_ 啟動選項。

</dd> <dt>

<span id="ErrorControl"></span><span id="errorcontrol"></span><span id="ERRORCONTROL"></span>ErrorControl
</dt> <dd>

如果服務在啟動期間無法啟動，則此資料行會指定啟動程式所採取的動作。 這些值會影響已安裝服務的 ServiceControl StartService 事件。 此資料行必須指定下列其中一個錯誤控制旗標。

將常數 **msidbServiceInstallErrorControlVital** (value = 0x08000) 新增至下表中的旗標，指定如果無法將服務安裝到系統，整體安裝應該會失敗。



| 錯誤控制旗標       | 值      | 啟動程式的動作                                                                                                                                                                       |
|--------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 服務 \_ 錯誤 \_ 忽略   | 0x00000000 | 記錄錯誤，並繼續執行啟動作業。                                                                                                                                       |
| 服務 \_ 錯誤 \_ 正常   | 0x00000001 | 記錄錯誤、顯示訊息方塊，然後繼續執行啟動作業。                                                                                                                    |
| 服務 \_ 錯誤 \_ 嚴重 | 0x00000003 | 記錄錯誤（如果可能的話），而且系統會在最後一項已知狀況良好的情況下重新開機。 如果正在啟動最後一個已知良好的設定，則啟動作業會失敗。 |



 

</dd> <dt>

<span id="LoadOrderGroup"></span><span id="loadordergroup"></span><span id="LOADORDERGROUP"></span>LoadOrderGroup
</dt> <dd>

此資料行包含的字串會為此服務所屬的載入順序群組命名。 如果服務不屬於群組，請指定 null 或空字串。

</dd> <dt>

<span id="Dependencies"></span><span id="dependencies"></span><span id="DEPENDENCIES"></span>依賴
</dt> <dd>

此資料行是服務名稱清單或系統必須在此服務之前啟動的載入順序群組。 依 Null 分隔清單中的名稱。 如果服務沒有相依性，請指定 Null 或空字串。 使用語法 \[ ~ \] 插入 Null。 群組的相依性表示，如果在嘗試啟動群組的所有成員之後，此服務至少有一個成員在執行中，就可以執行此服務。

例如，若要要求系統啟動 service1 和 service2，在啟動 ServiceInstall 資料行中所列的服務之前，請在 [相依性] 資料行中輸入 service1 \[ ~ \] service2 \[ ~ \] \[ ~ \] 。 Service1 和 service2 識別碼必須出現在資料表的主鍵中，或者是已安裝之服務的名稱。

您必須在組名前面加上 +，使其可與服務名稱區別。 若要在啟動 ServiceInstall 資料行中所列的服務之前要求系統啟動 service1 和至少一個訂購群組 MyGroup 成員，請輸入 service1 \[ ~ \] + MyGroup \[ ~ \] \[ ~ \] 。

</dd> <dt>

<span id="StartName"></span><span id="startname"></span><span id="STARTNAME"></span>StartName
</dt> <dd>

服務會以此資料行中的字串所提供的名稱來登入。 如果服務類型是服務 \_ WIN32 的 \_ 進程， \_ 請使用下列格式的帳戶名稱： DomainName \\ UserName。 如果帳戶屬於內建網域，則允許指定。 \\使用者。 如果服務類型是服務 \_ WIN32 \_ 共用 \_ 進程或服務 \_ 互動式 \_ 進程，則必須使用 LocalSystem 帳戶。 如果將 StartName 指定為 null，且大部分服務都將此資料行保留空白，則 [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) 函數會使用 LocalSystem 帳戶。

</dd> <dt>

<span id="Password"></span><span id="password"></span><span id="PASSWORD"></span>密碼
</dt> <dd>

這個字串是 StartName 資料行中所指定之帳戶名稱的密碼。 請注意，使用者必須具有以服務方式登入的許可權。 如果 StartName 為 null 或空字串，則服務沒有密碼。 LocalSystem 的 Startname 為 null，因此此實例中的密碼為 null，因此大部分的服務會將此資料行保留空白。

請注意，刪除以使用者名稱和密碼安裝的服務之後，安裝程式就無法復原服務，而必須先使用自訂動作來取得密碼。 安裝程式可以取得有關服務的所有必要資訊，但密碼會儲存在系統的受保護部分中。 自訂動作會藉由提示使用者、從資料庫讀取屬性，或讀取檔案來取得密碼。 然後，自訂動作必須呼叫 [**ChangeServiceConfig**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga)，以提供密碼，才能重新安裝服務。

Windows Installer 不會將輸入密碼欄位中的值寫入記錄檔中。

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>參數
</dt> <dd>

此資料行包含執行服務所需的任何命令列引數或屬性。

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

[元件資料表](component-table.md)中第一個資料行的外部索引鍵。 請注意，若要使用 InstallService 資料表安裝此服務，此元件的 KeyPath 必須是服務的可執行檔。

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述
</dt> <dd>

此資料行包含所設定之服務的可當地語系化描述。 如果此資料行保留空白，則安裝程式會使用現有的服務描述（如果有的話）。 如需詳細資訊，請參閱 \_ Microsoft Windows 軟體開發套件 (SDK) 中的服務描述。 若要清除現有的描述，請 \[ ~ \] 在此資料行中輸入 ""。 這會為新的或現有的服務產生空白描述。

</dd> </dl>

## <a name="remarks"></a>備註

[*順序資料表*](s-gly.md)中的 [InstallServices](installservices-action.md)動作會處理此資料表中的資訊。 如需使用 *順序資料表* 的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。

此資料表包含 Win32 [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) 函數的大部分參數。

雖然您可以使用使用者介面來指定將服務安裝為從來源執行，但安裝程式實際上並不支援這種類型的安裝。 使用本機系統的許可權層級執行的服務，必須安裝為從本機硬碟執行。 請避免安裝可模擬特定使用者之許可權的服務，因為這可能會將安全性資料寫入至記錄檔或系統登錄。 這可能會在系統重新開機時產生安全性問題、密碼衝突或遺失設定資料。

若要在卸載期間刪除服務， [ServiceControl 資料表](servicecontrol-table.md) 中的服務必須有對應的記錄，而且 **msidbServiceControlEventUninstallDelete** 旗標必須出現在事件資料行中。 在卸載期間，安裝程式不會刪除 ServiceInstall 資料表中的服務，而不會在 ServiceControl 資料表中執行此專案。

如需如何保護服務安全的詳細資訊，請參閱 [MsiLockPermissionsEx 資料表](msilockpermissionsex-table.md)。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE66](ice66.md)  
[ICE69](ice69.md)  
</dl>

 

 
