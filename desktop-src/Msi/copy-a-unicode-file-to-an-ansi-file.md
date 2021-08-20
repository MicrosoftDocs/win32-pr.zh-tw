---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiToAnsi.vbs。 此範例說明如何使用腳本，將 Unicode 文字檔重寫為 ANSI 文字檔。
ms.assetid: cb22495f-968c-470a-a2f1-d0e068133956
title: 將 Unicode 檔案複製到 ANSI 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 224a9115da67848bd43aaceb7e5d8f529693558191e52a04de2e7645a4e60aeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143372"
---
# <a name="copy-a-unicode-file-to-an-ansi-file"></a>將 Unicode 檔案複製到 ANSI 檔案

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiToAnsi.vbs。 此範例說明如何使用腳本，將 Unicode 文字檔重寫為 ANSI 文字檔。

使用此範例需要 Windows 腳本主機的 CScript.exe 或 WScript.exe 版本。 若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令列。 如果第一個引數是/？，則會顯示說明 或者，如果指定的引數太少。 若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。 此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。

**cscript WiToAnsi.vbs ANSI 檔案的 Unicode 檔案路徑 \[ 路徑 \] \[\]**

指定要轉換的 Unicode 文字檔。 指定要建立的 ANSI 文字檔。 如果未指定 ANSI 檔案，則會取代 Unicode 檔案。

如需其他腳本範例，請參閱[Windows Installer 腳本範例](windows-installer-scripting-examples.md)。 針對不需要 Windows 腳本主機的範例公用程式，請參閱[Windows Installer 開發工具](windows-installer-development-tools.md)。

 

 



