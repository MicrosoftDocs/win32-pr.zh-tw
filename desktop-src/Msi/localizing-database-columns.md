---
description: 使用資料表編輯器（例如 Orca 或 SQL 查詢）來修改 MNPFren.msi 資料庫中任何其他可當地語系化的資料行。
ms.assetid: b62cf529-71a0-47ff-99ea-a182c0fe4479
title: 當地語系化資料庫資料行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a72d4d4d82f45be66f41710dea7294a63051d69750ade49ae3b66761964b579f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629453"
---
# <a name="localizing-database-columns"></a>當地語系化資料庫資料行

使用資料表編輯器（例如 Orca 或 SQL 查詢）來修改 MNPFren.msi 資料庫中任何其他可當地語系化的資料行。 若要判斷特定資料表的哪些資料行可以當地語系化成另一種語言，請參閱該資料庫資料表的參考主題。 請參閱 [資料庫資料表](database-tables.md) ，以取得所有資料庫資料表的清單。

例如， [控制資料表](control-table.md) 中某些記錄的文字欄位可能需要當地語系化為法文。 字串「您確定要取消 \[ ProductName \] 安裝嗎？」 在此資料表中，您可以修改 [ [取消] 對話方塊](cancel-dialog.md) 中的，以法文顯示。 .msi 檔案中的原始記錄會如下所示。

[控制項資料表](control-table.md) (原始 .msi 檔案的部分) 



| 對話\_  | 控制 | 類型 | X   | Y   | 寬度 | 高度 | 屬性 | 屬性 | Text                                                          | 控制 \_ 下一步 | 說明 |
|-----------|---------|------|-----|-----|-------|--------|------------|----------|---------------------------------------------------------------|---------------|------|
| CancelDlg | Text    | Text | 48  | 15  | 194   | 30     | 3          |          | 確定要取消 \[ ProductName \] 安裝嗎？ |               |      |



 

您可以使用資料表編輯器來修改文字欄位，例如 SDK 或其他資料表編輯器提供的 Orca 資料表編輯器，或使用 SQL 查詢來變更控制資料表記錄的文字欄位。 在 Windows Installer SDK 中，會以公用程式 WiRunSQL.vbs 的形式提供示範腳本驅動資料庫查詢的範例。 使用下列命令列，以 WiRunSQL.vbs 和 Windows 腳本主機來修改欄位。 另請參閱[使用 SQL 和腳本的資料庫查詢範例](examples-of-database-queries-using-sql-and-script.md)。

**Cscript WiRunSQL.vbs MNPFren.msi "UPDATE Control SET Control. Text = ' Etes-vous sur de vouloir annuler l'installation de \[ ProductName \] ？ 'WHERE Control. Dialog \_ = ' CancelDlg '，control = ' Text ' "**

MNPFren.msi 中 (部分) 的[控制項資料表](control-table.md)



| 對話\_  | 控制 | 類型 | X   | Y   | 寬度 | 高度 | 屬性 | 屬性 | Text                                                                | 控制 \_ 下一步 | 說明 |
|-----------|---------|------|-----|-----|-------|--------|------------|----------|---------------------------------------------------------------------|---------------|------|
| CancelDlg | Text    | Text | 48  | 15  | 194   | 30     | 3          |          | Êtes-vous sûr de vouloir annuler l'installation de \[ ProductName \] ？ |               |      |



 

如果使用者取消安裝 MNPFren.msi，[ **取消] 對話方塊** 隨即出現，並顯示下列文字： "Êtes-vous sûr de vouloir annuler L'INSTALLATION de MNP2000？"

使用這個方法將 UI 文字當地語系化成不同的語言時，必須測試當地語系化的 UI，以確保控制項的大小夠大，足以顯示整個當地語系化的文字。 這應該使用可供顯示的所有字型大小設定進行測試。 當地語系化的文字可能需要比原始文字更多的空間，如果顯示在太小的控制項中，可能會被截斷。

[繼續](updating-productlanguage-and-productcode-properties.md)

 

 



