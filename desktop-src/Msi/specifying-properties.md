---
description: Windows Installer 屬性是安裝程式在安裝期間所使用的全域變數。
ms.assetid: 1c59939b-de0f-4bf4-ab1f-4f1aa2488bfa
title: 指定屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cd4294f35595e723491398172dc4c73337a1416
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984195"
---
# <a name="specifying-properties"></a>指定屬性

Windows Installer 屬性是安裝程式在安裝期間所使用的全域變數。 請參閱 [屬性](properties.md)底下的章節。 如果您在匯入 uisample.msi 從 Windows Installer SDK 使用的 [空白資料庫](importing-a-blank-database.md) ，則 MNP2000.msi 副本中的 [屬性資料表](property-table.md) 已經包含使用者介面所使用的許多屬性。 在本節中，您會將其他資訊新增至「記事本」範例安裝的特定屬性工作表。 另請參閱「 [程式資訊資料表」群組](program-information-tables-group.md)。

每個安裝套件中都需要有五個屬性，而且必須在 MNP2000.msi 的 [屬性工作表](property-table.md) 中更新 [記事本] 範例：

-   [**ProductCode**](productcode.md)
-   [**ProductLanguage**](productlanguage.md)
-   [**製造商**](manufacturer.md)
-   [**ProductVersion**](productversion.md)
-   [**ProductName**](productname.md)

雖然並非所有安裝套件都需要，未來可能會收到升級的應用程式也應該具有 [**UpgradeCode**](upgradecode.md) 屬性。 請參閱 [準備應用程式以進行未來的主要升級](preparing-an-application-for-future-major-upgrades.md)。

使用資料庫編輯器開啟 MNP2000.msi，並在屬性資料表中輸入下列資料。 此清單提供內建安裝程式屬性之參考主題的連結。 不是連結的屬性名稱是作者定義的屬性。 從 uisample.msi 匯入的許多屬性都適用于範例使用者介面。 稍後的 < 安裝範例一節消費者介面討論使用者介面。

[屬性工作表](property-table.md)



| 屬性                                         | 值                                     |
|--------------------------------------------------|-------------------------------------------|
| [**ARPHELPLINK**](arphelplink.md)               | https://www.microsoft.com/management       |
| BannerBitmap                                     | bannrbmp                                  |
| ButtonText \_ 回來                                 | < &回來                                |
| ButtonText \_ 流覽                               | Br&owse                                   |
| ButtonText \_ 取消                               | 取消                                    |
| ButtonText \_ Exit                                 | &結束                                     |
| ButtonText \_ 完成                               | &完成                                   |
| ButtonText \_ Ignore                               | &忽略                                   |
| ButtonText \_ 安裝                              | &安裝                                  |
| ButtonText \_ 下一步                                 | &下一個 >                                |
| ButtonText \_ No                                   | &否                                       |
| ButtonText \_ 確定                                   | 確定                                        |
| ButtonText \_ 移除                               | &移除                                   |
| ButtonText \_ 重設                                | &重設                                    |
| ButtonText \_ Resume                               | &繼續                                   |
| ButtonText \_ 重試                                | &重試                                    |
| ButtonText \_ Return                               | &傳回                                   |
| ButtonText \_ 是                                  | &是                                      |
| CompleteSetupIcon                                | completi                                  |
| ComponentDownload                                | ftp://anonymous@microsoft.com/components/ |
| CustomSetupIcon                                  | custicon                                  |
| [**DefaultUIFont**](defaultuifont.md)           | DlgFont8                                  |
| DialogBitmap                                     | dlgbmp                                    |
| DlgTitleFont                                     | {&DlgFontBold8}                           |
| ErrorDialog                                      | ErrorDlg                                  |
| ExclamationIcon                                  | exclamic                                  |
| 否                                            | 0                                         |
| Iagree                                           | No                                        |
| InfoIcon                                         | info                                      |
| InstallerIcon                                    | insticon                                  |
| [**INSTALLLEVEL**](installlevel.md)             | 3                                         |
| InstallMode                                      | 一般                                   |
| [**製造商**](manufacturer.md)             | Microsoft                                 |
| [**PIDTemplate**](pidtemplate.md)               | 12345<\#\#\#-%%%%%%%>@@@@@          |
| [**ProductCode**](productcode.md)               | {18A9233C-0B34-4127-A966-C257386270BC}    |
| [**產品**](productid.md)                   | 無                                      |
| [**ProductLanguage**](productlanguage.md)       | 1033                                      |
| [**ProductName**](productname.md)               | MNP2000                                   |
| [**ProductVersion**](productversion.md)         | 01.40.0000                                |
| Progress1                                        | 安裝                                |
| Progress2                                        | installs                                  |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md) | P                                         |
| RemoveIcon                                       | removico                                  |
| RepairIcon                                       | repairic                                  |
| 設定                                            | 設定                                     |
| True                                             | 1                                         |
| [**UpgradeCode**](upgradecode.md)               | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4}    |
| 精靈                                           | 安裝精靈                              |



 

[繼續](importing-the-installexecutesequence.md)

 

 



