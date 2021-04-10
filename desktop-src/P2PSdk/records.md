---
description: 記錄是一種方式，可讓您在圖形中的節點或群組中的成員之間進行通訊。
ms.assetid: f4c0869f-f147-4c2b-9418-3b407e22cb16
title: 記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c2d3c5ae3bd80bc0b3c0ca100155fc8efd7c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944758"
---
# <a name="records"></a>記錄

記錄是一種方式，可讓您在圖形中的節點或群組中的成員之間進行通訊。 記錄包含下列兩個部分：

-   記錄標頭
-   特定的不透明資料內容

標頭包含記錄的相關資訊，包括發行的版本、建立者和資料類型。 標頭也包含 XML 屬性欄位，可讓應用程式加入描述資料的名稱/值屬性，並有效率地在記錄資料庫中搜尋先前發行的特定記錄。 內容是應用程式定義的資料，對等基礎結構而言是不透明的。

當記錄發佈時， (標頭和資料) 會在整個圖形或群組中溢滿。 同步對等會接收這項資料，並將它儲存在本機資料庫中。 未同步和離線的對等會在下一次連接時接收資料，並與對等圖形或群組進行同步處理。

如需使用記錄的詳細資訊，請參閱下列主題：

-   [記錄相依性](record-dependencies.md)
-   [記錄管理](record-management.md)
-   [記錄屬性架構](record-attribute-schema.md)
-   [記錄搜尋查詢格式](record-search-query-format.md)

 

 



