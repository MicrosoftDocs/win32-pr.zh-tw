---
description: 此範例可讓模組取用者個別設定編輯控制項、總和檢查碼屬性，以及壓縮屬性。
ms.assetid: f0500856-18d0-45e5-992a-57e01fb2cca5
title: 可設定的元件範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971b2a7c442acb96d7ba00a444c8c3a038c339f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983333"
---
# <a name="configurable-component-example"></a>可設定的元件範例

在此範例中，下列 ModuleConfiguration 和 ModuleSubstitution 資料表可讓模組取用者個別設定編輯控制項的 Password 屬性、檔案的總和檢查碼屬性，以及相同檔案的壓縮屬性。

[ModuleSubstitution 資料表](modulesubstitution-table.md)



| 資料表   | 資料列           | 資料行     | 值                        |
|---------|---------------|------------|------------------------------|
| 控制 | Dialog1;Edit1 | 屬性 | \[= 密碼\]                |
| 檔案    | File1         | 屬性 | \[= Checksum \] \[ = 已壓縮\] |



 

[ModuleConfiguration 資料表](moduleconfiguration-table.md)



| Name       | 格式   | 類型 | CoNtextData                              | DefaultValue | 屬性 | DisplayName | Description |
|------------|----------|------|------------------------------------------|--------------|------------|-------------|-------------|
| 密碼   | 字元 |      | 2097152;True = 2097152;False = 0             | 0            | 0          |             |             |
| 總和檢查碼   | 字元 |      | 1024;Checksum = 1024;無總和檢查碼 = 0         | 0            | 0          |             |             |
| Compressed | 字元 |      | 24576;壓縮 = 16384;未壓縮 = 8192 | 8192         | 0          |             |             |



 

 

 



