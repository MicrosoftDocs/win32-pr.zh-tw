---
description: 請注意，您無法使用 SelfRegModules 和 SelfUnRegModules 動作來指定安裝程式註冊或取消註冊自行註冊 Dll 的順序。
ms.assetid: 46ee5ea2-35fd-4352-8a45-572d6fb5e080
title: 指定自我註冊的順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb26fbebad3167fbea95679a1ea7a29c28946ae6fa2dd2b014be6ade986e28f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039678"
---
# <a name="specifying-the-order-of-self-registration"></a>指定自我註冊的順序

請注意，您無法使用 [SelfRegModules](selfregmodules-action.md) 和 [SelfUnRegModules](selfunregmodules-action.md) 動作來指定安裝程式註冊或取消註冊自行註冊 dll 的順序。 這些動作會註冊 [SelfReg 資料表](selfreg-table.md)中列出的所有模組。 安裝程式不會自行註冊 .exe 的檔案。

若要指定安裝程式註冊或取消註冊模組的順序，您必須針對每個模組使用兩個 [自訂動作](custom-actions.md) 。 一個用於 DllRegisterServer 的自訂動作，另一個用於 DllUnregisterServer。 然後，這些自訂動作必須在 [InstallExecuteSequence 資料表](installexecutesequence-table.md) 中，于要註冊或取消註冊 DLL 的位置，于順序中撰寫。

下列範例說明如何撰寫資料庫，以排程在動作順序的特定點自行註冊 DLL。

[檔資料表](file-table.md) (部分) 



| 檔案  | 元件\_ | FileName  | 順序 |
|-------|-------------|-----------|----------|
| mydll.dll | myComponent | Mydll.dll | 13       |



 

[元件資料表](component-table.md) (部分) 



| 元件   | ComponentId | 目錄\_ | KeyPath |
|-------------|-------------|-------------|---------|
| myComponent | {*GUID*}  | myFolder    | mydll.dll   |



 

[目錄資料表](directory-table.md)



| 目錄 | 目錄 \_ 父系 | DefaultDir          |
|-----------|-------------------|---------------------|
| TARGETDIR |                   | SourceDir           |
| myFolder  | TARGETDIR         | myFolder \| 我的資料夾 |



 

[CustomAction 資料表](customaction-table.md)



| 動作     | 類型 | 來源   | 目標                                     |
|------------|------|----------|--------------------------------------------|
| mydllREG   | 3170 | myFolder | " \[ SystemFolder \] msiexec"/y " \[ \# mydll.dll \] " |
| mydllUNREG | 3170 | myFolder | " \[ SystemFolder \] msiexec"/z " \[ \# mydll.dll \] " |



 

[InstallExecuteSequence 資料表](installexecutesequence-table.md) (部分) 



| 動作           | 條件         | 順序 |
|------------------|-------------------|----------|
| SelfUnregModules |                   | 2200     |
| mydllUNREG       | $myComponent = 2    | 2201     |
| RemoveFiles      |                   | 3500     |
| InstallFiles     |                   | 4000     |
| SelfRegModules   |                   | 6500     |
| mydllREG         | $myComponent>2 | 6501     |



 

 

 



