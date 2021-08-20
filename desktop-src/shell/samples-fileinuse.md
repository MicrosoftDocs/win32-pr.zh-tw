---
description: 示範如何自訂 [使用中的檔案] 對話方塊，以顯示應用程式中目前開啟之檔案的其他資訊和選項。
title: 檔案使用中範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 22EFE7CC-D223-46b3-BD6B-293E3FA0BA01
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 27e0a216aed33d7b0295303539c6f46e489b4c4cba37fa7aedf0a7f2eddd7b60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968797"
---
# <a name="file-is-in-use-sample"></a>檔案使用中範例

示範如何自訂 [ **使用中** 的檔案] 對話方塊，以顯示應用程式中目前開啟之檔案的其他資訊和選項。

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



 

如需其他需求，請參閱 \_ 範例隨附的 IFileIsInUsesample.docx 檔。

## <a name="downloading-the-sample"></a>下載範例

| 位置      | 路徑 URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [FileIsInUse 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse) |

## <a name="building-the-sample"></a>建立範例

若要從命令提示字元視窗建立範例：

1.  開啟 [命令提示字元] 視窗，並流覽至 **FileIsInUse** 專案目錄。
2.  輸入 `msbuild FileIsInUse.sln`。

若要使用 Microsoft Visual Studio (慣用的) 來建立範例：

1.  開啟 Windows 檔案總管，然後流覽至 **FilesInUse** 專案目錄。 例如，完整的預設安裝路徑為 `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileIsInUse` 。
2.  按兩下 FileIsInUseSample .sln 檔案的圖示，在 Visual Studio 中開啟專案。
    > [!Note]  
    > .Sln 副檔名不會顯示在 [預設資料夾設定] 下。 在這種情況下，它可以透過其唯一圖示或其類型描述「Microsoft Visual Studio 解決方案」來識別。

     

3.  從 [ **組建** ] 功能表選取 [ **建立方案**]。

## <a name="running-the-sample"></a>執行範例

1.  使用命令提示字元視窗或 Windows 檔案總管，流覽至包含新可執行檔的目錄。
2.  在命令提示字元中，輸入 `FileIsInUseSample.exe` ，或從 Windows 檔案總管中，按兩下 FileIsInUseSample.exe 的圖示。

如需此程式碼範例的詳細資訊，請參閱 \_ 範例隨附的 IFileIsInUsesample.docx 檔。

 

 



