---
title: 建立裝置描述
description: UPnP 型裝置描述是一份 XML 檔，描述裝置的屬性和其中的嵌套裝置階層。
ms.assetid: b2a7d342-958c-439d-8b17-b4fdc5fbad12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52df95de15481c7004704b6f67cd9478083ac88
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932086"
---
# <a name="creating-a-device-description"></a>建立裝置描述

UPnP 型 [*裝置描述*](d-gly.md) 是一份 XML 檔，描述裝置的屬性和其中的嵌套裝置階層。 以 upnp 為基礎之裝置描述的架構（稱為 UPnP 範本語言 (UTL) 適用于裝置）是在 UPnP 裝置架構中定義。 裝置描述包含 [*服務描述*](s-gly.md)的連結。 服務描述的架構和服務的 UTL 也會在「UPnP 裝置架構」規格中定義。

> [!Note]  
> 從 www.upnp.org 使用服務描述時可能會發生問題。

 

裝置的開發人員必須提供裝置的裝置和服務描述。

託管裝置開發人員必須提供的裝置描述專案，與「UPnP 裝置架構」規格中定義的元素相同，但有下列例外：

-   **ControlURL** 和 **eventSubURL** 元素是必要的，而且必須是空的。 當裝置已發佈並宣告時，裝置主機會填入這些欄位的值。
-   **UDN** 元素必須包含裝置描述檔唯一的識別碼 (也就是說，它不需要是全域唯一的) 。 此識別碼可用來查詢裝置主機所產生的 UDN。
-   **SCPDURL** 元素不能包含服務描述的 url。 相反地，它們必須包含服務描述檔案的名稱。 服務描述檔案必須位於 [*資原始目錄*](r-gly.md)中。 在註冊過程中，必須將此目錄的位置提供給裝置主機，例如使用安裝程式。 這個路徑及其下的所有都是相對路徑，以註冊的路徑為基礎。
-   **Icon** 元素內的 **url** 元素不能包含裝置圖示的 url。 相反地，它們必須包含圖示檔的名稱。 如果有的話，圖示檔必須位於資原始目錄中。 這個路徑及其下的所有都是相對路徑，以註冊的路徑為基礎。
-   **URLBase** 元素不得存在。

> [!Note]  
> 裝置主機產生的所有 Url 都是相對 Url。 Url 會相對於裝置描述檔的位置，該檔會在初始裝置公告中傳送。

 

> [!IMPORTANT]
> 請勿將批註新增至您的裝置描述檔，因為當通用隨插即用裝置主機嘗試剖析檔時，可能會導致註冊失敗。

 

## <a name="string-length-limitations"></a>字串長度限制

下列字串長度用於具有 UPnP 技術的裝置主機 API：

-   **deviceType** –64個位元組
-   **friendlyName** -64 個位元組
-   **製造商** –64個位元組
-   **modelDescription** –128個位元組
-   **modelName** –32個位元組
-   **modelNumber** –32個位元組
-   **serialNumber** –64個位元組
-   **UPC** –12個位元組
-   **serviceType** –64個位元組
-   **serviceId** –64個位元組

 

 




