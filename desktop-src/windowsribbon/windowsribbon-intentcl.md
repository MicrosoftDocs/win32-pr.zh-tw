---
title: 編譯功能區標記
description: 若要讓 Windows 功能區架構使用功能區標記檔案，必須將標記檔案編譯成二進位格式的資源檔。
ms.assetid: ef9fea92-8c67-461d-9d74-2e259e407fb0
keywords:
- Windows 功能區，編譯標記
- 功能區，編譯標記
- Windows 功能區，編譯器工作流程
- 功能區、編譯器工作流程
- 'Windows 功能區、UI 命令編譯器 (UICC.exe) '
- '功能區、UI 命令編譯器 (UICC.exe) '
- 'UI 命令編譯器 (UICC.exe) '
- 'UICC.exe (UI 命令編譯器) '
- 編譯 Windows 功能區標記
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671e03d7d3a941f1c97891d87c170e65e326d70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507356"
---
# <a name="compiling-ribbon-markup"></a>編譯功能區標記

若要讓 Windows 功能區架構使用 [功能區標記](windowsribbon-schema.md) 檔案，必須將標記檔案編譯成二進位格式的資源檔。 Windows 軟體開發套件 (SDK)  (7.0 （含）以後版本的 (UICC) 的專用標記編譯器會隨附于此用途。 除了編譯標記的二進位版本之外，UICC 會產生 ID 定義標頭 ( .h) 檔案，該檔案會將所有標記專案公開至功能區主應用程式，以及在組建階段用來將影像和字串資源連結至主應用程式的資源 ( .rc) 檔。

-   [編譯器工作流程](#compiler-workflow)
-   [命令列語法](#command-line-syntax)
    -   [引數和選項](#arguments-and-options)
    -   [範例](#example)
-   [相關主題](#related-topics)

## <a name="compiler-workflow"></a>編譯器工作流程

下圖說明功能區標記編譯器的工作流程。

![顯示功能區標記編譯器工作流程的圖表。](images/overviews/overviews-intentcl.png)

## <a name="command-line-syntax"></a>命令列語法

下列範例顯示功能區標記編譯器的命令列語法。


```
UICC <ribbonFile> <binaryFile> [options]
```



### <a name="arguments-and-options"></a>引數和選項

下表說明此工具的引數和選項。

> [!Note]  
> 所列的命令列選項必須依照指定的順序來指定。

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>選項</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>/header<headerFile></td>
<td>產生名為的標頭檔 <headerFile> ，其中包含標記命令識別碼資源符號。 如果省略，則不會產生標頭檔。</td>
</tr>
<tr class="even">
<td>/res<resourceFile></td>
<td>產生稱為的資源檔， <resourceFile> 此檔案會在組建階段將所有影像和字串資源、二進位標記檔和標頭檔連結至主應用程式。 如果省略，則不會產生資源檔。</td>
</tr>
<tr class="odd">
<td>/name<ribbonName></td>
<td>登入之二進位標記檔案的資源名稱 <resourceFile> 。 預設值為 APPLICATION_RIBBON。</td>
</tr>
<tr class="even">
<td>/W{0\1\2}</td>
<td>根據嚴重性來篩選事件訊息。 
<table>
<tbody>
<tr class="odd">
<td>0<br/></td>
<td>僅限錯誤訊息。<br/></td>
</tr>
<tr class="even">
<td>1<br/></td>
<td>僅限錯誤和警告訊息。<br/></td>
</tr>
<tr class="odd">
<td><strong>2</strong><br/></td>
<td>預設值。 <br/> 錯誤、警告和參考訊息。<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="example"></a>範例

下列範例示範如何使用功能區標記編譯器，為功能區應用程式產生一組一般的資源檔。

`UICC.exe RibbonMarkup.xml RibbonMarkup.bml /header:RibbonIds.h /res:RibbonUI.rc`

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用功能區標記宣告命令和控制項](windowsribbon-schema.md)
</dt> <dt>

[建立功能區應用程式](windowsribbon-stepbystep.md)
</dt> </dl>

 

 





