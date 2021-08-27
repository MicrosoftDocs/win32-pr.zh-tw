---
description: AnyPath 資料類型是一種文字字串，其中包含完整路徑或相對路徑。
ms.assetid: fe8a4d2a-1960-40af-a0e4-4d65accdd388
title: AnyPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab5d8e7aaf4e92c2b33379b92b00263df07366ff340346aa19518478f8f2394
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045778"
---
# <a name="anypath"></a>AnyPath

AnyPath 資料類型是一種文字字串，其中包含完整路徑或相對路徑。 指定相對路徑時，您可以將簡短名稱和長名稱分隔 () ，以包含簡短檔案名的長檔名 \| 。 請注意，您不能以這種方式指定目錄或完整路徑的多個層級。 路徑中可能包含以方括弧括住的屬性 (\[ \]) 。

有效 AnyPath 資料的範例：

-   \\\\伺服器 \\ 共用 \\ 暫存
-   c： \\ temp
-   \\臨時
-   project ~ 1 \| Project 狀態

不正確 AnyPath 資料範例：

-   c： \\ temp \\ project ~ 1 \| c： \\ temp one \\ Project 狀態
-   \\temp \\ project ~ 1 \| \\ temp one \\ Project 狀態

 

 



