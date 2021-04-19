---
description: 藉由複製原始產品的安裝套件和來原始目錄樹狀結構，開始撰寫升級套件。
ms.assetid: 279f0ab6-a6fc-4594-af6c-5a69d6167300
title: 匯入原始安裝資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390a51e1ef068124fcdf85142ab01406d92f9a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983770"
---
# <a name="importing-original-installation-database"></a>匯入原始安裝資料庫

藉由複製原始產品的安裝套件和來原始目錄樹狀結構，開始撰寫升級套件。 [安裝範例](an-installation-example.md)提供撰寫 MNP2000 安裝套件的指示。 您應該複製下列資料夾的內容：

C： \\ 範例 \\MNP2000.msi

C： \\ 範例 \\ 記事本\\

C： \\ 範例 \\ 二進位檔\\

C： \\ 範例 \\ 圖示\\

更新 [記事本] 資料夾的內容，使其符合 [規劃主要升級](planning-a-major-upgrade.md)中所述的來源。 移除所有過時的原始檔（例如 Baseball.txt），並取代為更新的檔案，例如 Baseba01.txt。 新增升級所提供的其他新檔案，例如 Opera01.txt。

將 MNP2000.msi 重新命名為 MNP2001.msi。 在後續步驟中，您將使用資料表編輯器，將此資料庫修改為 .msi 檔案以進行升級。 未在後續章節中明確修改的資料庫資料表，與原始產品資料庫中的資料表相同，MNP2000.msi。

[繼續](updating-directory-structure-for-an-upgrade.md)

 

 



