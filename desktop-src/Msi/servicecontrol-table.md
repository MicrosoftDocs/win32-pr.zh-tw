---
description: ServiceControl 資料表是用來控制已安裝或已卸載的服務。注意：相依于全域組件快取中之元件的服務 (GAC) 無法使用 ServiceInstall 和 ServiceControl 資料表來安裝或啟動。
ms.assetid: c51cd9bd-3c55-4eec-ab67-172765adc51c
title: ServiceControl 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2abd123e937673694dffd53773a16fcbd704c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693724"
---
# <a name="servicecontrol-table"></a>ServiceControl 資料表

ServiceControl 資料表是用來控制已安裝或已卸載的服務。

> [!Note]  
> 依賴全域組件快取中的 [元件](assemblies.md) 存在 (GAC) 的服務無法使用 [ServiceInstall](serviceinstall-table.md) 和 ServiceControl 資料表來安裝或啟動。 如果您需要啟動相依于 GAC 中元件的服務，您必須使用 [InstallFinalize 動作](installfinalize-action.md) 或 [認可自訂動作](commit-custom-actions.md)之後排序的自訂動作。 如需將元件安裝至 GAC 的詳細資訊，請參閱將元件 [安裝到全域組件快取](installation-of-assemblies-to-the-global-assembly-cache.md)。

 

ServiceControl 資料表具有下列資料行。



| Column         | 類型                         | 答案 | Nullable |
|----------------|------------------------------|-----|----------|
| ServiceControl | [識別碼](identifier.md) | Y   | N        |
| Name           | [格式 化](formatted.md)   | N   | N        |
| 事件          | [整數](integer.md)       | N   | N        |
| 引數      | [格式 化](formatted.md)   | N   | Y        |
| 等候           | [整數](integer.md)       | N   | Y        |
| 元件\_    | [識別碼](identifier.md) | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="ServiceControl"></span><span id="servicecontrol"></span><span id="SERVICECONTROL"></span>ServiceControl
</dt> <dd>

這是此資料表的主要索引鍵。

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>名字
</dt> <dd>

此資料行是為服務命名的字串。 您可以使用這個資料行來控制未安裝的服務。

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>事件
</dt> <dd>

此資料行包含要在命名服務上執行的作業。 請注意，當您停止服務時，所有相依于該服務的服務也會停止。 當刪除正在執行的服務時，安裝程式會停止服務。

此欄位中的值是位欄位，可以合併成代表數個作業的單一值。

下列值只會在安裝期間使用。



| 常數                           | 十六進位 | Decimal | Description                                                                        |
|------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| **msidbServiceControlEventStart**  | 0x001       | 1       | 在 [StartServices 動作](startservices-action.md)期間啟動服務。    |
| **msidbServiceControlEventStop**   | 0x002       | 2       | 在 [StopServices 動作](stopservices-action.md)期間停止服務。       |
| (無)                             | 0x004       | 4       | <reserved>                                                                   |
| **msidbServiceControlEventDelete** | 0x008       | 8       | 在 [DeleteServices 動作](deleteservices-action.md)期間刪除服務。 |



 

下列值只會在卸載期間使用。



| 常數                                    | 十六進位 | Decimal | Description                                                                        |
|---------------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| **msidbServiceControlEventUninstallStart**  | 0x010       | 16      | 在 [StartServices 動作](startservices-action.md)期間啟動服務。    |
| **msidbServiceControlEventUninstallStop**   | 0x020       | 32      | 在 [StopServices 動作](stopservices-action.md)期間停止服務。       |
| (無)                                      | 0x040       | 64      | <reserved>                                                                   |
| **msidbServiceControlEventUninstallDelete** | 0x080       | 128     | 在 [DeleteServices 動作](deleteservices-action.md)期間刪除服務。 |



 

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>參數
</dt> <dd>

用於啟動服務的引數清單。 引數是以 null 字元分隔 \[ ~ \] 。 例如，引數清單一、二和三列為： \[ ~ \] 兩個引數 \[ ~ \] 。

</dd> <dt>

<span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>等
</dt> <dd>

將此欄位保留為 null 或輸入值1，會導致安裝程式等候最多30秒，讓服務完成後再繼續。 等候可以用來允許重大事件的額外時間傳回失敗錯誤。 在此欄位中，值為0表示只等候，直到服務控制管理員 (SCM) 報告此服務處於擱置狀態，再繼續進行安裝。

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

[元件資料表](component-table.md)中第一個資料行的外部索引鍵。

</dd> </dl>

## <a name="remarks"></a>備註

[*順序資料表*](s-gly.md)中的 [StartServices](startservices-action.md)、 [StopServices](stopservices-action.md)和 [DeleteServices](deleteservices-action.md)動作會處理此資料表中的資訊。 如需使用 *順序資料表* 的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。

使用 [名稱] 欄來啟動、停止或刪除由安裝所取代的服務，或是相依于所安裝之新服務的服務。 例如，在 ServiceControl 資料行中輸入 MyService 可以將此服務系結至元件資料行中的 MyComponent \_ 。 如果在安裝時將事件資料行中的位欄位設定為 [啟動]，則安裝程式會在安裝 MyComponent 時開始 MyService。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



