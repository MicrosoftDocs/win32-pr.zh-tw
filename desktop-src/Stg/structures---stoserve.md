---
title: 結構-StoServe
description: COPaper 會將畫筆色彩、寬度和座標封裝成 INKDATA 結構，並將其儲存在記憶體中管理的動態配置陣列中。
ms.assetid: 25e68c39-5306-4ad6-85dd-a8a5e256abf0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9868f38d7915185b8d3511bd1bf6faa9c7a1e1b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932114"
---
# <a name="structures---stoserve"></a>結構-StoServe

COPaper 會將畫筆色彩、寬度和座標封裝成 **INKDATA** 結構，並將其儲存在記憶體中管理的動態配置陣列中。

## <a name="inkdata-structure"></a>INKDATA 結構

以下是來自 **INKDATA** 結構的宣告（來自 PAPER. H）。

``` syntax
// The types of Ink Data.
#define INKTYPE_NONE  0
#define INKTYPE_START 1
#define INKTYPE_DRAW  2
#define INKTYPE_STOP  3

  // The Ink Data structure.
  typedef struct _INKDATA
  {
    SHORT nType;            // Ink Type.
    SHORT nX;               // X-coordinate of ink point.
    SHORT nY;               // Y-coordinate of ink point.
    SHORT nWidth;           // Ink line width in pixels.
    COLORREF crColor;       // Ink color.
  } INKDATA;
```

這些 **INKDATA** 封包的動態陣列是由 m \_ paInkData （ [**IPaper**](ipaper-methods.md) 實類別的成員）所指向。 陣列是使用初始配置在 **IPaper：： InitPaper** 方法內建立的。 如需詳細資訊，請參閱 **InitPaper** 方法和 CImpIPaper 執行的私用 NextSlot 公用程式方法。 [**InkStart**](inkstart-method.md)、 [**InkDraw**](inkdraw-method.md)和 [**InkStop**](cguipaper-methods.md)方法會使用 NextSlot 來取得陣列中的新位置。 當需要時，NextSlot 會動態擴充陣列。

用戶端會呼叫 [**IPaper：： erase**](ipaper-methods.md) 方法來清除目前的繪圖。 這個方法不會重新配置陣列;它只會將所有目前的筆墨資料標示為 INKTYPE \_ NONE，然後將陣列的資料結尾索引重設為零。

用戶端會呼叫 [**IPaper：： Lock**](ipaper-methods.md) 並 **解除鎖定** 方法，以管理要繪製之 COPaper 的擁有權。 提供這些方法的目的，是要在多個用戶端之間組織存取，以保存在共用 COPaper 中的繪圖。

## <a name="paper_properties-structure"></a>紙張 \_ 屬性結構

用戶端會呼叫 [**IPaper：： Resize**](ipaper-methods.md) 方法，告知 COPaper 使用者已調整目前的繪圖紙張矩形大小。 當所有紙張資料都儲存在複合檔案中時，此座標資料會保存在 **紙張 \_ 屬性** 結構中，並與筆墨資料一起儲存。

以下是從 PAPER. .H 的 **紙張 \_ 屬性** 聲明。

``` syntax
#define PAPER_TITLE_SIZE 64
  typedef struct _PAPER_PROPERTIES
  {
    LONG lInkDataVersion;
    LONG lInkArraySize;
    COLORREF crWinColor;
    RECT WinRect;
    WCHAR wszTitle[PAPER_TITLE_SIZE];
    WCHAR wszAuthor[PAPER_TITLE_SIZE];
    WCHAR wszReserved1[PAPER_TITLE_SIZE];
    WCHAR wszReserved2[PAPER_TITLE_SIZE];
  } PAPER_PROPERTIES;
```

檔 **\_ 屬性** 結構的設計目的，是要在 DllPaper 元件演進時隨時加入新的筆墨資料格式。 [**IPaper**](ipaper-methods.md)介面的一般程度已足夠，因為 DllPaper 元件的後續版本可能會在執行相同的 **IPaper** 介面時儲存不同的筆墨資料格式。 由於 **IPaper** 的方法不會相依于特定的筆墨資料格式，因此支援不同筆墨資料格式的新版本 DllPaper 元件可以使用這個相同的介面。

儲存在複合檔案中的紙張屬性會記錄筆墨資料陣列的目前大小。 然後可以配置適當的陣列大小，以容納從檔案讀取的筆墨資料。

**紙張 \_ 屬性** 結構也會儲存紙張表面的繪圖矩形大小和背景視窗色彩。

雖然未在 **StoServe** / **StoClien** 範例中使用，但也可以儲存繪圖示題和作者名稱。

因為用來存取複合檔案的 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面會管理這項資訊，所以建立日期和上次修改日期不包含在這些紙張屬性中。

 

 




