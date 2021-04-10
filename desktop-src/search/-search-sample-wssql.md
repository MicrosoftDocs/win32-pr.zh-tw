---
description: WSSQL 程式碼範例會示範如何透過結構化查詢語言 (SQL)  (SQL) ，在 Microsoft OLE DB 和 Windows Search 之間進行通訊。
ms.assetid: 28663608-66b3-4404-9426-5a4b5f52a408
title: WSSQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac8f76b995d21a562f843344d1722cecec433af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847812"
---
# <a name="wssql"></a>WSSQL

WSSQL 程式碼範例會示範如何透過結構化查詢語言 (SQL)  (SQL) ，在 Microsoft OLE DB 和 Windows Search 之間進行通訊。

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
| GitHub        | [WSSQL 範例](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSSQL)           |

> [!NOTE]  
> 針對所有 Windows 版本（包括 Windows 7），建議您直接從 GitHub 下載最新版本的範例。

## <a name="building-the-sample"></a>建立範例

1. 開啟 Windows 檔案總管，然後流覽至 **WSSQL** 專案目錄。
2. 按兩下 WSSQL .sln 檔案的圖示，在 Visual Studio 中開啟專案。
    > [!NOTE]  
    > .Sln 檔案是在舊版 Visual Studio 下建立的，因此，如果您執行 Visual Studio 2012 或更新版本，則需要進行升級。 這不會影響範例的行為。

3. 從 [ **組建** ] 功能表選取 [ **建立方案**]。

## <a name="running-the-sample"></a>執行範例

1. 使用命令提示字元視窗或 Windows 檔案總管，流覽至包含新可執行檔的目錄。
2. 在命令提示字元中，輸入 `WSSQL.exe` ，或從 Windows 檔案總管中，按兩下 WSSQL.exe 的圖示。

## <a name="related-topics"></a>相關主題

### <a name="conceptual"></a>概念

[使用 Windows Search SQL 語法](-search-sql-windowssearch-entry.md)

[一般查詢語言資訊](-search-sql-generalqueryinfo.md)

[OLE DB 程式設計總覽](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a>其他範例

[搜尋程式碼範例](-search-samples-ovw.md)
