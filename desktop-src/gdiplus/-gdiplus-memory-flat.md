---
description: Windows GDI + 會公開由大約600函式組成的一般 API。 這些一般 API 函式是由 GdiplusBase c + + 類別包裝。
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: 記憶體函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ed10574f9cc88c5b7ca8a2b0ed09924fe8c5192
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395823"
---
# <a name="memory-functions"></a>記憶體函數

Windows GDI + 會公開一個包含大約600函式的一般 API，這些函式會在 Gdiplus.dll 中執行，並在 Gdiplusflat 中宣告。 GDI + 一般 API 中的函式是由大約 40 c + + 類別的集合所包裝。 建議您不要直接呼叫一般 API 中的函式。 每當您呼叫 GDI + 時，您都應該呼叫 c + + 包裝函式所提供的方法和函式。 Microsoft 產品支援服務將不會提供直接呼叫一般 API 的程式碼支援。 如需使用這些包裝函式方法的詳細資訊，請參閱 [Gdi + 一般 API](-gdiplus-flatapi-flat.md)。

下列一般 API 函式是由 [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) c + + 類別包裝。

## <a name="memory-functions-and-corresponding-wrapper-methods"></a>記憶體函數和對應的包裝函式方法



| 一般函數                                          | 包裝函式方法                                                                                                                                      | 備註                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipAlloc (size \_ t size) <br/> | [**GpStatus WINGDIPAPI GdiplusBase void \* (operator new)  (size \_ t \_ 大小)**](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | 配置一個 Windows GDI + 物件的記憶體。 <br/> GdipAlloc 宣告于 GdiplusMem 中。<br/>  |
| GpStatus WINGDIPAPI GdipFree (void \* ptr) ;<br/>   | [**GpStatus WINGDIPAPI GdiplusBase void (運算子 delete)  (void \* in \_ pVoid)**](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | 解除配置一個 Windows GDI + 物件的記憶體。 <br/> GdipFree 宣告于 GdiplusMem 中。<br/> |



 

 

 
