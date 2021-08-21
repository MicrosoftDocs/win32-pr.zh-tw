---
description: 下列程式描述的案例會產生可永久隱藏功能的轉換。
ms.assetid: 43f36866-a9df-4035-a8ae-5ccbcb628a90
title: 產生轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df605dd01a494089d2e6ecd38c8b3c6d03ecb5d6335e2348682e1af16f79faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635986"
---
# <a name="generating-a-transform"></a>產生轉換

下列程式描述的案例會產生可永久隱藏功能的轉換。

**永久隱藏產品功能**

1.  複製原始安裝套件。
2.  將 [功能資料表](feature-table.md) 中顯示資料行的值設定為零，以修改複製。 這會指定隱藏此功能。
3.  藉由呼叫 [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)，從原始安裝套件建立轉換至新的安裝套件。
4.  藉由呼叫 [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)，在轉換中建立摘要資訊。

然後，您就可以在安裝期間套用轉換。 如需詳細資訊，請參閱套用 [轉換](applying-transforms.md)。

 

 



