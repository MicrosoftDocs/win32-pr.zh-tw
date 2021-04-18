---
description: '[OpenSearch 程式碼] 範例示範如何使用 [OpenSearch] 通訊協定建立同盟搜尋服務，以及 ( 的 [ (搜尋) 連接器]) 檔案的 [.osdx]。'
ms.assetid: 792884e4-826b-4474-82e1-1680d4d8b602
title: OpenSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8656efec434744d14714529d1e7b0d01a5349ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386124"
---
# <a name="opensearch"></a>OpenSearch

[OpenSearch 程式碼] 範例示範如何使用 [ [opensearch](https://github.com/dewitt/opensearch) ] 通訊協定建立同盟搜尋服務，以及 ( 的 [ (搜尋) 連接器]) 檔案的 [.osdx]。

本主題包含下列各節。

-   [需求](#requirements)
-   [下載範例](#downloading-the-sample)
-   [建立範例](#building-the-sample)
-   [執行範例](#running-the-sample)
-   [相關主題](#related-topics)

## <a name="requirements"></a>規格需求



| 產品     | 最小產品版本 |
|-------------|-------------------------|
| Windows     | Windows 7               |
| Windows SDK | 7.0                     |



 

## <a name="downloading-the-sample"></a>下載範例

下列位置提供此範例。



| Location      | 路徑 URL                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub  | [OpenSearch 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/OpenSearch)      |



 

 

> [!Note]  
> 針對所有 Windows 版本（包括 Windows 7），建議您直接從 GitHub 下載最新版本的範例。

 

## <a name="building-the-sample"></a>建立範例

若要從命令提示字元建立範例：

1.  開啟 [命令提示字元] 視窗，並流覽至 **AdventureSearch** 專案目錄。 
2.  輸入 `msbuild AdventureSearch.sln`。

若要使用 Microsoft Visual Studio (慣用的) 來建立範例：

1.  開啟 Windows 檔案總管，然後流覽至 **AdventureSearch** 專案目錄。
2.  按兩下 AdventureSearch .sln 檔案的圖示，在 Visual Studio 中開啟專案。
    > [!Note]  
    > .Sln 副檔名不會顯示在 [預設資料夾設定] 下。 在這種情況下，它可以透過其唯一圖示或其類型描述「Microsoft Visual Studio 解決方案」來識別。

     

3.  從 [ **組建** ] 功能表選取 [ **建立方案**]。

## <a name="running-the-sample"></a>執行範例

1.  使用命令提示字元視窗或 Windows 檔案總管，流覽至包含新可執行檔的目錄。
2.  在命令提示字元中，輸入 `AdventureSearch.exe` ，或從 Windows 檔案總管中，按兩下 AdventureSearch.exe 的圖示。
3.  在命令提示字元中，輸入 `GetOSDX.exe` ，或從 Windows 檔案總管中，按兩下 GetOSDX.exe 的圖示。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[搜尋連接器描述架構的總覽](search-sconn-desc-schema-entry.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows 中的同盟搜尋](-search-federated-search-overview.md)
</dt> <dt>

[搜尋程式碼範例](-search-samples-ovw.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[程式庫描述架構](../shell/library-schema-entry.md)
</dt> </dl>

 

 
