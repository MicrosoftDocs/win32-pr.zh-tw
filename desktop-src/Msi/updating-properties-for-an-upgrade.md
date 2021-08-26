---
description: 因為升級會變更 .msi 檔案的名稱，並變更部分元件的元件碼，所以升級的產品程式碼必須與原始產品的產品碼變更。
ms.assetid: ebb1a217-fce6-43f0-9139-c0f4422c8fc4
title: 更新升級的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d340f56eaf78c585e28a52dc7b310bf1af047d7530e61b841267bc0b83251a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039178"
---
# <a name="updating-properties-for-an-upgrade"></a>更新升級的屬性

因為升級會變更 .msi 檔案的名稱，並變更部分元件的元件碼，所以升級的產品程式碼必須與原始產品的產品碼變更。 如需需要升級才能變更 [ [**ProductCode**](productcode.md) ] 屬性之案例的說明，請參閱 [變更產品代碼](changing-the-product-code.md)。 變更 ProductCode 的升級稱為 [主要升級](major-upgrades.md)。

升級封裝的 [**ProductName**](productname.md) 屬性、 [**ProductVersion**](productversion.md) 屬性、 [**ProductLanguage**](productlanguage.md) 屬性和 [**UpgradeCode**](upgradecode.md) 屬性可以從原始產品變更或保持不變。 根據這些屬性的值，Windows Installer 可以決定是否要將未來的升級套件套用至目前的升級。

您必須將 [升級資料表](upgrade-table.md) 的 ActionProperty 資料行中指定的屬性加入至 [**SecureCustomProperties**](securecustomproperties.md) 屬性。

使用資料庫編輯器開啟 MNP2001.msi，並在 [屬性資料表](property-table.md)中輸入下列資料。 此清單提供內建安裝程式屬性之參考主題的連結。 不是連結的屬性名稱是作者定義的屬性。 許多屬性都是從 SDK 隨附的 Uisample.msi 匯入的。 如需詳細資訊，請參閱匯 [入消費者介面](importing-the-user-interface.md)。

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
| [**ProductCode**](productcode.md)               | {34CF587C-1D8F-4DD5-ADFE-440F4B593987}    |
| [**ProductID**](productid.md)                   | 無                                      |
| [**ProductLanguage**](productlanguage.md)       | 1033                                      |
| [**ProductName**](productname.md)               | MNP2001                                   |
| [**ProductVersion**](productversion.md)         | 01.50.0000                                |
| Progress1                                        | 安裝                                |
| Progress2                                        | installs                                  |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md) | P                                         |
| RemoveIcon                                       | removico                                  |
| RepairIcon                                       | repairic                                  |
| 設定                                            | 設定                                     |
| True                                             | 1                                         |
| [**UpgradeCode**](upgradecode.md)               | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4}    |
| 精靈                                           | 安裝精靈                              |
| SecureCustomProperties                           | OLDAPPFOUND                               |



 

[繼續](updating-sequence-tables-for-an-upgrade.md)

 

 



