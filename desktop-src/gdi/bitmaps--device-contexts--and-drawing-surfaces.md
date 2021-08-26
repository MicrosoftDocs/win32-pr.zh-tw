---
description: 裝置內容 (DC) 是一種資料結構，用來定義繪圖物件、其相關聯的屬性，以及影響裝置上輸出的圖形模式。 若要建立 DC，請呼叫 CreateDC 函式;若要取出 DC，請呼叫 GetDC 函數。
ms.assetid: 4feafb23-bf5a-493a-9d1d-96170711b907
title: 點陣圖、裝置內容和繪圖表面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed42215dc98ce179f9d36ddc0a24244c018c4177287d1fdfff974a2814e14d64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966388"
---
# <a name="bitmaps-device-contexts-and-drawing-surfaces"></a>點陣圖、裝置內容和繪圖表面

*裝置內容* (DC) 是一種資料結構，用來定義繪圖物件、其相關聯的屬性，以及影響裝置上輸出的圖形模式。 若要建立 DC，請呼叫 [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) 函式;若要取出 DC，請呼叫 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 函數。

在傳回識別該 DC 的控制碼之前，系統會選取一個繪圖介面至 DC。 如果應用程式呼叫 [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) 函式以建立 VGA 顯示器的裝置內容，此繪圖介面的維度為 640 480 圖元。 如果應用程式呼叫 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 函式，則維度會反映工作區的大小。

在應用程式開始繪圖之前，必須藉由呼叫 [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) 函式，在 DC 中選取具有適當寬度和高度的點陣圖。 當應用程式將 DC 的控制碼傳遞給其中一個圖形裝置介面 (GDI) 繪圖函式時，所要求的輸出會出現在選取的繪圖介面上。

如需詳細資訊，請參閱 [記憶體裝置](memory-device-contexts.md)內容。

 

 



