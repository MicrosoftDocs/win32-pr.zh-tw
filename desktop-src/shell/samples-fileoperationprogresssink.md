---
description: 示範如何使用 IFileOperationProgressSink 介面方法來監視 IFileOperation 介面動作的詳細資料。
title: 檔案作業進度接收
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 196ABB75-1FE0-44f5-9060-59AAB4231567
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fe0ba5c86fdb2df5fe168559aa019941897563823e75670b0813ecb7e9e44d69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820348"
---
# <a name="file-operation-progress-sink"></a>檔案作業進度接收

示範如何使用 [**IFileOperationProgressSink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) 介面方法來監視 [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) 介面動作的詳細資料。

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
| GitHub  | [FileOperationProgressSink 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/FileOperationProgressSink) |

## <a name="building-the-sample"></a>建立範例

若要從命令提示字元視窗建立範例：

1.  開啟 [命令提示字元] 視窗，並流覽至 **FileOperationProgressSink** 專案目錄。
2.  輸入 `msbuild FileOperationProgressSinkSample.sln`。

若要使用 Microsoft Visual Studio (慣用的) 來建立範例：

1.  開啟 Windows 檔案總管，然後流覽至 **FilesInUse** 專案目錄。 例如，完整的預設安裝路徑為 `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample` 。
2.  按兩下 FileOperationProgressSinkSample .sln 檔案的圖示，在 Visual Studio 中開啟專案。
    > [!Note]  
    > .Sln 副檔名不會顯示在 [預設資料夾設定] 下。 在這種情況下，它可以透過其唯一圖示或其類型描述「Microsoft Visual Studio 解決方案」來識別。

     

3.  從 [ **組建** ] 功能表選取 [ **建立方案**]。

## <a name="running-the-sample"></a>執行範例

1.  使用命令提示字元視窗或 Windows 檔案總管，流覽至包含新可執行檔的目錄。
2.  在命令提示字元中，輸入 `FileOperationProgressSinkSample.exe` ，或從 Windows 檔案總管中，按兩下 FileOperationProgressSinkSample.exe 的圖示。

 

 



