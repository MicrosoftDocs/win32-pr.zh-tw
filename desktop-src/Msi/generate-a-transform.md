---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiGenXfm.vbs。 此範例腳本可從兩個 Windows Installer 資料庫產生轉換。 如需詳細資訊，請參閱資料庫轉換。
ms.assetid: bfa918b8-8d90-4e14-8a06-6c3d5b5dc13b
title: 產生轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92617c2e007b9deb01685679d4940095285b8218
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693736"
---
# <a name="generate-a-transform"></a>產生轉換

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiGenXfm.vbs。 此範例腳本可從兩個 Windows Installer 資料庫產生轉換。 如需詳細資訊，請參閱 [資料庫轉換](database-transforms.md)。

此範例將示範如何使用：

[**(安裝程式物件) 的 OpenDatabase 方法**](installer-opendatabase.md)

[](installer-lasterrorrecord.md) [**安裝程式物件** 的 LastErrorRecord 方法](installer-object.md)

[](database-generatetransform.md) [**資料庫物件** 的「進行」（method）方法](database-object.md)

您將需要 CScript.exe 或 WScript.exe 版本的 Windows Script Host 才能使用此範例。 若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令列。 如果第一個引數是/？，則會顯示說明 或者，如果指定的引數太少。 若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。 此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。

**cscript WiGenXfm.vbs \[ 原始資料庫路徑的路徑，以 \] \[ 修改轉換檔案的資料庫 \] \[ 路徑\]**

指定原始 Windows Installer 資料庫的路徑。 指定已修改之資料庫的路徑。 指定要建立之轉換檔案的路徑。 如果省略轉換檔的路徑，則只會比較兩個資料庫。

如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。 如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。

請注意， [當地語系化範例](a-localization-example.md) 會示範如何 [產生自訂轉換](generating-a-customization-transform.md)。

 

 



