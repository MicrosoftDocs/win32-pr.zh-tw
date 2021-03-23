---
title: 使用描述中繼資料表
description: 描述項資料表中，每個都識別描述元堆積中的範圍，都會系結至命令清單上目前的根簽章所定義的位置。
ms.assetid: 4ECEC07A-7ABC-4C5F-B23C-36F0D92643FE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e589274fbb93e48e4d65e545a62999e654b7688f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104961"
---
# <a name="using-descriptor-tables"></a>使用描述中繼資料表

描述項資料表中，每個都識別描述元堆積中的範圍，都會系結至命令清單上目前的根簽章所定義的位置。

-   [索引描述中繼資料表](#indexing-descriptor-tables)
-   [相關主題](#related-topics)

著色器可以找出組成描述中繼資料表的描述項所參考的資源。 其他資源系結：索引緩衝區、頂點緩衝區、資料流程輸出緩衝區、轉譯目標和深度樣板都是直接在命令清單上完成，而不是透過描述項。 總括來說：

下列資源參考可以共用相同的描述中繼資料表和堆積：

-   著色器資源檢視
-   未排序的存取權視圖
-   常數緩衝區查看

下列資源參考必須位於自己的描述元堆積中：

-   取樣器

下列資源不會放在描述中繼資料表或堆積中，而是直接使用命令清單進行系結：

-   索引緩衝區
-   頂點緩衝區
-   串流輸出緩衝區
-   呈現目標
-   深度樣板視圖

## <a name="indexing-descriptor-tables"></a>索引描述中繼資料表

著色器無法從著色器中給定的呼叫位置，以動態方式從描述項資料表界限進行索引編制。 不過，您可以在描述中繼資料表中選取描述項，以在相同描述元類型範圍內的著色器程式碼中動態編制索引， (例如在 SRVs) 的連續區域中編制索引。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[描述中繼資料表](descriptor-tables.md)
</dt> </dl>

 

 




