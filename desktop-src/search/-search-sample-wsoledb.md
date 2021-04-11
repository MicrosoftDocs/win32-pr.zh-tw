---
description: WSOleDB 程式碼範例會示範 Active Template Library (ATL) OLE DB Windows Search 應用程式的存取，並示範兩種從 Windows Search 抓取結果的額外方法。
ms.assetid: c81bf3af-e023-4384-8c89-0fa9c8f08773
title: WSOleDB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6cecfc308fdfa9af796e64ab8bc6273f9c4d94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847813"
---
# <a name="wsoledb"></a>WSOleDB

WSOleDB 程式碼範例會示範 Active Template Library (ATL) OLE DB Windows Search 應用程式的存取，並示範兩種從 Windows Search 抓取結果的額外方法。

本主題包含下列各節。

- [需求](#requirements)
- [下載範例](#downloading-the-sample)
- [建立範例](#building-the-sample)
- [執行範例](#running-the-sample)
- [相關主題](#related-topics)

## <a name="requirements"></a>規格需求

| 產品     | 產品版本          |
|-------------|--------------------------|
| Windows     | Windows 7、8.1 或 10    |
| Windows SDK | 7.0 或更高版本           |

## <a name="downloading-the-sample"></a>下載範例

下列位置提供此範例。

| Location      | 路徑 URL                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub        | [WSOleDB 範例](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSOleDB)         |

> [!NOTE]  
> 針對所有 Windows 版本（包括 Windows 7），建議您直接從 GitHub 下載最新版本的範例。

## <a name="building-the-sample"></a>建立範例

1. 開啟 Windows 檔案總管，然後流覽至 **WSOleDB** 專案目錄。
2. 按兩下 WSOleDB .sln 檔案的圖示，在 Visual Studio 中開啟專案。
  
    > [!NOTE]  
    > .Sln 檔案是在舊版 Visual Studio 下建立的，因此，如果您執行 Visual Studio 2012 或更新版本，則需要進行升級。 這不會影響範例的行為。

3. 從 [ **組建** ] 功能表選取 [ **建立方案**]。

## <a name="running-the-sample"></a>執行範例

1. 使用命令提示字元視窗或 Windows 檔案總管，流覽至包含新可執行檔的目錄。
2. 在命令提示字元中，輸入 `WSOleDB.exe` ，或從 Windows 檔案總管中，按兩下 WSOleDB.exe 的圖示。

## <a name="related-topics"></a>相關主題

### <a name="reference"></a>參考

[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

### <a name="conceptual"></a>概念

[OLE DB 程式設計總覽](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a>其他範例

[搜尋程式碼範例](-search-samples-ovw.md)
