---
title: IAVIStream 和 IAVIFile 介面
description: IAVIStream 和 IAVIFile 介面
ms.assetid: 3ab602da-239f-44ff-b43d-e0c380619d99
keywords:
- IAVIStream 介面
- IAVIFile 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f419de6864986bf72914dd5551ab6ad5b7093379b40180183171a7a498cea3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140936"
---
# <a name="iavistream-and-iavifile-interfaces"></a>IAVIStream 和 IAVIFile 介面

[**IAVIStream**](/windows/desktop/api/Vfw/nn-vfw-iavistream)和 [**IAVIFile**](/windows/desktop/api/Vfw/nn-vfw-iavifile)介面包含檔案和資料流程處理常式所使用的方法。 **PAVISTREAM** 資料型別是 avi 資料流程物件的指標， (透過 **IAVIStream**) 介面，而 **PAVIFILE** 資料類型則是透過 **IAVIFile** 介面)  (之 avi 檔案物件的指標。

若要在 C 中建立物件指標，請先為夠大的結構配置空間，以包含虛擬函式資料表和其他資料成員的指標。 為您的資料流程類型建立方法的虛擬函式資料表，然後將虛擬函式資料表的指標設定為虛擬函式資料表的位址。

 

 




