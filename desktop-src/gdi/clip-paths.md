---
description: 如同裁剪區域，剪輯路徑是應用程式可以選取到裝置內容中的另一個繪圖物件。
ms.assetid: 35c4052b-3f11-40bc-9cc9-6f999326a656
title: 剪輯路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc4a93b0047110a6adb2f68d413e89cb1e97fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972757"
---
# <a name="clip-paths"></a>剪輯路徑

如同裁剪區域，剪輯路徑是應用程式可以選取到裝置內容中的另一個繪圖物件。 與裁剪區域不同的是，剪輯路徑一律是由應用程式所建立，而且會用來裁剪成一或多個不規則圖形。 例如，應用程式可以使用在文字字串中形成字元外框的線條和曲線來定義剪輯路徑。

若要建立剪輯路徑，首先必須建立描述所需不規則圖形的路徑。 路徑是藉由在呼叫 [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) 函式之後，以及在呼叫 [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) 函式之前，呼叫適當的圖形裝置介面 (GDI) 繪圖函式來建立。 這個函式集合稱為路徑括弧。 如需路徑和路徑括弧的詳細資訊，請參閱 [路徑](paths.md)。

建立路徑之後，您可以藉由呼叫 [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) 函式、識別裝置內容，並指定使用模式，將它轉換成剪輯路徑。 使用模式會決定系統如何結合新的剪輯路徑與裝置內容的原始裁剪區域。 下表描述使用模式。



| [模式]      | 描述                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| R G N \_ 和  | 剪輯路徑包含裝置內容之裁剪區域和目前路徑 (重迭區域) 的交集。    |
| R G N \_ 複製 | 剪輯路徑是目前的路徑。                                                                                           |
| R G N \_ 差異 | 剪輯路徑包含裝置內容的裁剪區域，其中已排除目前路徑的任何交集部分。        |
| R G N \_ 或   | 剪輯路徑包含裝置內容之裁剪區域和目前路徑的聯集 (組合區域) 。              |
| R G N \_ XOR  | 剪輯路徑包含裝置內容之裁剪區域和目前路徑的聯集，但不包括交集。 |



 

 

 



