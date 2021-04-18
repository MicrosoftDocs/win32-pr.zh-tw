---
title: 將更新套用至目錄
description: 將更新套用至目錄
ms.assetid: 4aedb0d6-36c7-425c-b6d3-e16161cf6828
keywords:
- Windows Media Player 線上商店，將更新套用至目錄
- 線上商店，將更新套用至目錄
- 輸入1個線上商店，將更新套用至目錄
- Windows Media Player 線上商店，更新目錄
- 線上商店，更新目錄
- 輸入1個線上商店，更新目錄
- Windows Media Player 線上商店、類別目錄更新
- 線上商店、類別目錄更新
- 輸入1個線上商店、類別目錄更新
- 目錄更新
- 更新目錄
- 將更新套用至目錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d468edb7d09b8804fa924f7c31fc1be45d27c8fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968670"
---
# <a name="applying-an-update-to-a-catalog"></a>將更新套用至目錄

> [!Note]  
> 這通常不是因為診斷用途而完成，例如有助於確認差異檔案是否有效。 以這種方式產生的目錄不是壓縮格式，且不應該傳遞至 Windows Media Player。

 

您可以使用下列語法來建立新的類別目錄檔案，其中 *inputcatalog* 是原始目錄的位置，而 *inputdiff* 是要套用之差異檔案的位置。 類別目錄檔案必須是未壓縮的格式。


```C++
catcomp applydiff <inputcatalog> <inputdiff>
```



例如，下列程式會從 C： \\ Catalog210 \\ catalog. Wmdb 和 c： \\ Catalog210 catalog 建立新的目錄 \\ 。


```C++
catcomp applydiff C:\Catalog210\catalog.wmdb C:\Catalog210\catalog.diff
```



如果編譯成功，catcomp.exe 會建立下列輸出檔案。



| 檔案名稱        | 描述       |
|------------------|-------------------|
| catalog. wmdb. new | 新的類別目錄檔案。 |



 

 

 




