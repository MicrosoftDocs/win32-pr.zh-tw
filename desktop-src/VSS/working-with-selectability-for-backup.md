---
description: 下表說明可與備份作業相關的四種元件類型。
ms.assetid: d94e015b-6735-4a88-9d24-b73f0b5f6542
title: 使用 Selectability 進行備份
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82081bb9cef51572afc2a8b5c08cf845ee22736dd8fdc20edf60fa0082ce8c9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118842312"
---
# <a name="working-with-selectability-for-backup"></a>使用 Selectability 進行備份

下表說明可與備份作業相關的四種元件類型。



| 元件類型                                                                                                                                                                                                               | Description                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="Nonselectable-for-backup_components"></span><span id="nonselectable-for-backup_components"></span><span id="NONSELECTABLE-FOR-BACKUP_COMPONENTS"></span>其-備份元件<br/>             | 邏輯路徑中沒有可選取的備份祖系。<br/>                              |
| <span id="Selectable-for-backup_components"></span><span id="selectable-for-backup_components"></span><span id="SELECTABLE-FOR-BACKUP_COMPONENTS"></span>可選取的備份元件<br/>                         | 邏輯路徑中沒有可選取的備份祖系。<br/>                              |
| <span id="Nonselectable-for-backup_subcomponents"></span><span id="nonselectable-for-backup_subcomponents"></span><span id="NONSELECTABLE-FOR-BACKUP_SUBCOMPONENTS"></span>其-備份子元件<br/> | 其-備份元件，並在其路徑中具有可選取的備份父項目。<br/> |
| <span id="Selectable-for-backup_subcomponents"></span><span id="selectable-for-backup_subcomponents"></span><span id="SELECTABLE-FOR-BACKUP_SUBCOMPONENTS"></span>可選取的備份子元件<br/>             | 可選取的備份元件，並在其路徑中具有可選取的備份父項目。<br/>    |



 

此外，任何可選取的備份元件（不論是否具有可選取的備份祖先代）都會定義 [*元件集*](vssgloss-c.md) ，如果其他元件將它設定為其邏輯路徑中的上階。

管理選取元件以進行備份的規則可以摘要如下：

-   如果有任何元件的邏輯路徑中沒有可選取的備份上階（不論元件是否可供選取-備份或其備份），則必須 [*明確包含*](vssgloss-e.md)該元件。 這表示這些元件的中繼資料會加入至備份元件檔。

    要求者會使用 [**>ivssbackupcomponents：： AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) 方法明確地新增這些元件。

-   其備份子元件一律會 [*隱含地包含*](vssgloss-i.md) 在備份中。 這表示這些元件的中繼資料不是備份元件檔的一部分。
-   如果備份中明確包含上階，則會隱含地包含可選取的備份子元件。 在此情況下，這些元件的中繼資料不會加入至 [備份元件] 檔。 如果隱含選取的備份子元件定義了元件集，也會隱含地選取該元件集的成員。
-   可選取的備份子元件，其可選取備份的上階未明確包含在備份中，仍可使用 [**>ivssbackupcomponents：： AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) 方法明確包含在備份中。 元件的中繼資料就會加入至 [備份元件] 檔。 此外，如果可選取的備份子元件定義元件集，則該元件集的成員會隱含地包含在備份中。

在 [元件的邏輯路徑](logical-pathing-of-components.md) 中討論的「MyWriter」案例可用來作為說明備份 selectability 的範例。



| 元件名稱 | 邏輯路徑            | 可選取以進行備份 |
|----------------|-------------------------|-----------------------|
| 執行  | ""                      | N                     |
| "ConfigFiles"  | 執行           | N                     |
| "LicenseInfo"  | ""                      | Y                     |
| "Security"     | ""                      | Y                     |
| 使用者     | "Security"              | N                     |
| 數位憑證 | "Security"              | N                     |
| "writerData"   | ""                      | Y                     |
| Set1         | "writerData"            | N                     |
| Jan          | "writerData \\ Set1"      | N                     |
| 年          | "writerData \\ Set1"      | N                     |
| Set2         | "writerData"            | N                     |
| Jan          | \\"writerData      | N                     |
| 年          | \\"writerData      | N                     |
| 查詢        | "writerData \\ QueryLogs" | N                     |
| 用法        | "writerData"            | Y                     |
| Jan          | "writerData \\ Usage"     | N                     |
| 年          | "writerData \\ Usage"     | N                     |



 

只要備份 "MyWriter"，就會使用 [**>ivssbackupcomponents：： AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) 方法明確地包含 "可執行檔" 元件，並隱含地包含 "ConfigFiles" 元件。

元件 "LicenseInfo" 是獨立可選取的備份元件。 您可以自行決定是否要使用 [**>ivssbackupcomponents：： AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) 方法來選取它，但是它的選擇將不會選取其他元件。

可選取的備份元件「安全性」定義簡單的元件集，其中包含兩個其備份子元件：「使用者資訊」和「憑證」。 如果已明確包含「安全性」以進行備份，則「使用者資訊」和「憑證」一律也會隱含地納入。 除非包含「安全性」，否則沒有任何方法可在備份作業中包含子元件「使用者資訊」或「憑證」。

如果選取了元件 "writerData"，則會隱含地選取其備份元件 "Set1"、""、"" 和 "Query"，以及可選取的備份元件「使用量」。 這些元件中的每一個都有隱含選取以進行備份的子元件。 它們的任何中繼資料都不會加入至備份元件檔。

如果未選取元件 "writerData"，備份就不會包含其備份元件 "Set1"、""、"" 和 "Query"。

不過，要求者可能會選擇明確包含可選取的備份元件「使用量」。 此元件的中繼資料將會加入至 [備份元件] 檔。 「使用量」的子元件「Jan」和「Dec」將會隱含地新增至備份，但不會將其資訊新增至備份元件檔。

明確包含用於備份的元件將會在備份元件檔中建立對應的 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 實例。

要求 (者會使用 [**>ivssbackupcomponents：：) GetWriterComponents （**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) 包含在其檔中），並抓取儲存的 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 物件，藉以從備份元件檔中取得明確包含之元件的相關資訊。

由於檔案集資訊不 (檔案規格、路徑和遞迴旗標，) 備份元件檔中的元件，也不會有隱含新增元件的任何相關資訊，要求者必須查詢寫入器元資料檔案，以取得備份元件檔中包含之所有元件的完整資訊。

 

 




