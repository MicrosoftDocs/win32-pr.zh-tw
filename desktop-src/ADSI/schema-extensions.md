---
title: 架構延伸模組
description: ADSI 架構的架構可讓您將新的架構類別加入至架構類別容器，並在執行時間將新的屬性加入至現有的架構類別物件。
ms.assetid: 935d39ca-cfb9-4aa3-aa0e-b614f7b359f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c7fdc4b363fea83029fc5526464bd5825fa851dbe82e874911a0ab45d869843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178817"
---
# <a name="schema-extensions"></a>架構延伸模組

ADSI 架構的架構可讓您將新的架構類別加入至架構類別容器，並在執行時間將新的屬性加入至現有的架構類別物件。 後者的功能不需要新的程式碼。 對於允許可延伸目錄服務的命名空間，這是一項重要的功能。 提供者元件必須允許此擴充性，並知道要存取和儲存類別實例和其屬性值的位置。 在典型的可延伸目錄服務中，這項資訊會以與任何其他架構類別和屬性定義相同的方式儲存在目錄服務資料庫中。

> [!Note]  
> 在 COM 介面詞彙中，只有屬性可以加入至現有的架構類別，而不是方法。 加入新的方法需要加入該方法的新實，因此需要額外的程式碼。

 

如需特定提供者架構的範例，請參閱 [架構管理](schema-management.md)。

 

 




