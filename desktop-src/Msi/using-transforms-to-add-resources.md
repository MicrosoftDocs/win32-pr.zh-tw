---
description: 自訂應用程式（例如公司範本）所需的資源，可以透過包含應用程式安裝套件的轉換來與應用程式一起部署。
ms.assetid: 3d9328d0-4d95-449c-bf2b-5487f7ba5971
title: 使用轉換來新增資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2999371079ac57d0e44800c9374d496db6eb400864fed3422d88f2b03731724
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038988"
---
# <a name="using-transforms-to-add-resources"></a>使用轉換來新增資源

自訂應用程式（例如公司範本）所需的資源，可以透過包含應用程式安裝套件的轉換來與應用程式一起部署。 使用轉換來部署資源（例如檔案、登錄機碼或快速鍵）時，應遵循下列規則。

-   轉換應該將一或多個新元件新增至安裝資料庫，以包含其他資源。 轉換不應將資源新增至已存在於安裝中的元件。
-   轉換應該將一或多個新功能新增至安裝資料庫，以包含這些新元件。 這些新功能不應該是任何現有功能的父系，但可能會同時引進新的父項和子功能。 新功能的名稱應該是在此產品的所有其他轉換中都是唯一的。 這兩項轉換都不應該在 [功能資料表](feature-table.md) 的 feature 資料行中所列的相同名稱的產品中新增功能，並包含不同的元件或資源。

 

 



