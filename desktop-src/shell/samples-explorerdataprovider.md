---
description: 示範如何在瀏覽器中執行 Shell 命名空間延伸模組，包括內容功能表行為和自訂工作。
title: Explorer 資料提供者範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B1B20AF8-3DDE-467b-A49E-A77849CF9F1B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 223f498f42e33dda09206b1e21a44138fda54e261ec957efb62e55148a014d6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677835"
---
# <a name="explorer-data-provider-sample"></a>Explorer 資料提供者範例

示範如何在瀏覽器中執行 Shell 命名空間延伸模組，包括內容功能表行為和自訂工作。

本主題包含下列各節。

-   [需求](#requirements)
-   [下載範例](#downloading-the-sample)
-   [建立範例](#building-the-sample)
-   [執行範例](#running-the-sample)

## <a name="requirements"></a>規格需求



| 產品                                | 最小產品版本 |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 6.1                     |



 

## <a name="downloading-the-sample"></a>下載範例

| 位置      | 路徑 URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [ExplorerDataProvider 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/explorerdataprovider) |

## <a name="building-the-sample"></a>建立範例

若要從命令提示字元建立範例：

1.  開啟 [命令提示字元] 視窗，並流覽至 **ExplorerDataProvider** 專案目錄。
2.  輸入 `msbuild ExplorerDataProvider.sln`。

若要使用 Microsoft Visual Studio (慣用的) 來建立範例：

1.  開啟 Windows 檔案總管，然後流覽至 **ExplorerDataProvider** 專案目錄。
2.  按兩下 ExplorerDataProvider .sln 檔案的圖示，在 Visual Studio 中開啟專案。
3.  從 [ **組建** ] 功能表選取 [ **建立方案**]。 DLL 將會建立在預設的 \\ Debug 或 \\ Release 目錄中。

> [!Note]  
> 在 Windows SDK 中包含的此範例版本中，64位發行組建的設定不會在連結器的 **模組定義** 檔選項中包含 ExplorerDataProvider .def 檔。 您必須自行指定該檔案，才能在64位環境中建立。 將這一行加入 `ModuleDefinitionFile="ExplorerDataProvider.def"` 至 VCLinkerTool 區段， (從 ExplorerDataProvider vcproj 檔案的行 329) 開始，如下所示：
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>LinkIncremental=&quot;1&quot;
> AdditionalLibraryDirectories=&quot;&quot;c:\Program Files\Microsoft SDKs\Windows\v6.0\Lib\x64&quot;&quot;
> ModuleDefinitionFile=&quot;ExplorerDataProvider.def&quot;
> GenerateDebugInformation=&quot;true&quot;</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> 此範例從程式碼庫下載的版本已針對此問題更正，而不需要在您的部分進行任何額外的動作。
>
>  
>
> ## <a name="running-the-sample"></a>執行範例
>
> 1.  使用命令提示字元或 Windows 檔案總管，流覽至包含新 .dll 和 propdesc 檔案的目錄。
> 2.  在命令列中，輸入 `regsvr32.exe` 。
>     > [!Note]  
>     > 如果您是從提高許可權的命令提示字元執行此命令，自我註冊也會自動註冊 propdesc 檔案。 如果是從非提高許可權的命令提示字元執行，則命名空間延伸模組將可運作，但不含自訂屬性功能。
>
>      
>
> 3.  開啟 **我的電腦** 資料夾，並流覽該處有新的命名空間延伸模組。
>
>  
>
>  
>


