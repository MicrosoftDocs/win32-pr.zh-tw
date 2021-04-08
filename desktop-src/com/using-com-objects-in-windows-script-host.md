---
title: 在 Windows Script Host 中使用 COM 物件
description: Microsoft Windows Script Host 是一個腳本公用程式，可讓您用來在基底作業系統內執行腳本。
ms.assetid: b13c1bdf-91ce-42a2-b66a-20d68952bb34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cb28fc0e388ba69f28c56e780d058d27f9e165
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103696341"
---
# <a name="using-com-objects-in-windows-script-host"></a>在 Windows Script Host 中使用 COM 物件

Microsoft Windows Script Host 是一個腳本公用程式，可讓您用來在基底作業系統內執行腳本。 您可以使用 Windows Script Host 將一般工作自動化，並建立功能強大的宏和登入腳本。 Windows Script Host 隨附于 VBScript 和 JScript ActiveX 腳本引擎。 其他軟體公司則提供 ActiveX 腳本引擎，適用于 PerlScript、PScript、Python 等語言。

若要在 Windows Script Host 所執行的腳本中使用 COM 物件，您必須先建立物件的實例。 建立 COM 物件之後，您就可以在腳本中使用它。

Windows Script Host 包含兩個應用程式。 其中一個會從 Windows 桌面 () 執行腳本，另一個則是 `WScript.exe` 從命令提示字元 () 執行腳本 `CScript.exe` 。

若要從桌面執行腳本，只要按兩下腳本檔即可。 指令檔是文字檔。 依照慣例，VBScript 檔案具有副檔名 `.vbs` 和 JScript 檔案 `.js` 。

若要從命令提示字元執行腳本，請 `Cscript.exe` 使用命令列執行應用程式，如下所示：

```console
cscript "c:\\sample scripts\\chart.vbs"
```

其中 `c:\\sample scripts\\chart.vbs` 是包含腳本之檔案的路徑。

您可以輸入下列命令列，以列印 Cscript.exe 所支援的參數清單：

```console
call cscript //?
```

若要在 Windows Script Host 所執行的腳本中使用 COM 物件，您必須先建立物件的實例。 在 VBScript 中，您可以藉由呼叫方法來完成這項作業 `CreateObject()` 。 在 JScript 中，您可以使用 `ActiveXObject` 物件或 `WScript.CreateObject()` 方法。 下列範例說明如何 `CreateObject()` 使用 VBScript 呼叫：


```VB
Dim objXL
Set objXL = CreateObject("Excel.Application")
 
```



下列範例說明如何 `ActiveXObject` 使用 JScript 建立物件：


```JScript
var objXL = new ActiveXObject("Excel.Application");
 
```
或者，使用 `WScript.CreateObject()` JScript 內的方法：

```JScript
var objXL = WScript.CreateObject("Excel.Application");
```


建立 COM 物件的實例之後，您可以撰寫使用物件的腳本，例如：


```VB
objXL.Visible = true;
 
```



除了 CreateObject 方法和 ActiveXObject 物件之外，VBScript 和 JScript 都提供 GetObject 的方法，後者會傳回物件實例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 COM 物件編寫腳本](scripting-with-com-objects.md)
</dt> </dl>

 

 




