---
description: 大部分的命名空間延伸是 Shell 命名空間的子集。
ms.assetid: 00b6b281-b157-4a61-9852-8aafd9ba68d3
title: 顯示命名空間延伸模組的 Self-Contained 視圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6f8555cfb8cdac6248c5ea1c70ce8af29bfd16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973376"
---
# <a name="displaying-a-self-contained-view-of-a-namespace-extension"></a>顯示命名空間延伸模組的 Self-Contained 視圖

大部分的命名空間延伸是 Shell 命名空間的子集。 當您建立連接點時，如 [指定命名空間延伸模組的位置](nse-junction.md)所述，Windows 檔案總管可讓使用者流覽至您的命名空間延伸模組，就像任何其他資料夾一樣。 不過，您也可以使用 Windows 檔案總管，只顯示命名空間延伸模組的內容。 此顯示選項有時稱為 *根視圖*。 雖然不常用，但在某些類型的延伸模組中，根視圖可能較適合一般的視圖。

使用根視圖時，會建立 Windows 檔案總管的新實例，將延伸模組的內容顯示為個別的命名空間。 根目錄檢視的樹狀檢視只會顯示屬於延伸模組一部分的資料夾。 使用者無法從根視圖流覽至 Shell 命名空間的其他部分。

針對根視圖，擴充功能的執行方式就如同一般的視圖一樣。 唯一的差別在於，Windows 檔案總管會顯示延伸模組內容的方式。 您甚至可以讓相同的延伸模組具有一般和根目錄的觀點。

若要開啟延伸模組的視圖，您必須使用/root 旗標啟動 Explorer.exe 的實例。 有幾種不同的方式可以啟動根目錄檢視，視擴充功能的本質而定。

-   [如何使用連接點開啟根視圖](how-to-use-a-junction-point-to-open-a-rooted-view.md)
-   [如何使用快捷方式檔案開啟根視圖](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
-   [如何顯示檔案的根目錄檢視](how-to-display-a-rooted-view-of-a-file.md)

 

 



