---
description: Enhanced-Format 中繼檔
ms.assetid: 8d7015cb-5e1d-4805-a7a8-1f8b693e0681
title: Enhanced-Format 中繼檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbae113c65e4dd05e67c155c2323698cd023191
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972685"
---
# <a name="enhanced-format-metafiles"></a>Enhanced-Format 中繼檔

*增強格式的中繼檔* 是由下列元素所組成：

-   標頭
-   GDI 物件控制碼的資料表
-   私用調色板
-   中繼檔記錄的陣列

增強的中繼檔提供真正的裝置獨立性。 您可以將儲存在增強型中繼檔中的圖片，視為在特定時刻拍攝之影片顯示的「快照集」。 此「快照集」會維護其維度，不論它在印表機上的位置、繪圖器、桌面或任何應用程式的工作區。

您可以使用增強的中繼檔儲存使用 GDI 函數所建立的圖片 (包括) 的新路徑和轉換函式。 由於增強的元檔案格式是標準化的，因此以這種格式儲存的圖片可以從一個應用程式複製到另一個應用程式;而且，由於圖片與裝置無關，因此保證會在任何輸出裝置上維持其形狀與比例。

-   [增強的中繼檔記錄](enhanced-metafile-records.md)
-   [增強的中繼檔建立](enhanced-metafile-creation.md)
-   [增強的中繼檔作業](enhanced-metafile-operations.md)

 

 



