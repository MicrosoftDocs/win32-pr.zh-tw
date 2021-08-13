---
description: 您可以使用安裝程式，藉由執行合併來將某個資料庫中的資訊新增至另一個資料庫。
ms.assetid: c53ef3d2-b3dc-4cd1-bd98-a856a223917f
title: 合併資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2931bb624037f2f909b99cfeb19a64fcb4abef689fe988a308d35766f50b1dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628704"
---
# <a name="merging-databases"></a>合併資料庫

您可以使用安裝程式，藉由執行合併來將某個資料庫中的資訊新增至另一個資料庫。 合併[和轉換](merges-and-transforms.md)操作整個資料庫，而合併合併兩個資料庫到一個。 合併適用于開發團隊，因為它們可讓大型應用程式的安裝資料庫分成較小的部分，之後再輕易到完整的安裝資料庫中。

**將數個元件資料庫合併成單一完整資料庫**

1.  另外開發部分元件資料庫。
2.  藉由呼叫 [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) 函數，將每個元件資料庫合併到主要產品資料庫。

 

 



