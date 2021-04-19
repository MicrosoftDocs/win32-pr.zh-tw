---
description: AnyPath 資料類型是一種文字字串，其中包含完整路徑或相對路徑。
ms.assetid: fe8a4d2a-1960-40af-a0e4-4d65accdd388
title: AnyPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ab6265874616bb0bb1a2f61098cdbabfa8ea24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993096"
---
# <a name="anypath"></a>AnyPath

AnyPath 資料類型是一種文字字串，其中包含完整路徑或相對路徑。 指定相對路徑時，您可以將簡短名稱和長名稱分隔 () ，以包含簡短檔案名的長檔名 \| 。 請注意，您不能以這種方式指定目錄或完整路徑的多個層級。 路徑中可能包含以方括弧括住的屬性 (\[ \]) 。

有效 AnyPath 資料的範例：

-   \\\\伺服器 \\ 共用 \\ 暫存
-   c： \\ temp
-   \\臨時
-   project ~ 1 個 \| 專案狀態

不正確 AnyPath 資料範例：

-   c： \\ temp \\ project ~ 1 \| c： \\ 暫存一個 \\ 專案狀態
-   \\temp \\ project ~ 1 \| \\ Temp 一個 \\ 專案狀態

 

 



