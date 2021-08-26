---
title: 確定文字以正確的閱讀方向顯示
description: 某些語言（例如阿拉伯文和希伯來文）需要由右至左的閱讀方向。
ms.assetid: fa9a3dd6-575a-4877-a488-22845c6726c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3774e4d237863a218cadf5206e4dc4921bceaeaa06c00ab81057f80dd8ee6549
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982168"
---
# <a name="ensure-text-is-displayed-with-the-correct-reading-direction"></a>確定文字以正確的閱讀方向顯示

某些語言（例如阿拉伯文和希伯來文）需要由右至左的閱讀方向。 針對[DirectWrite](direct-write-portal.md)的文字格式物件，預設的閱讀方向是由左至右。 DirectWrite 不會自動從地區設定推斷讀取方向，因此您必須自行進行。

首先，使用 windowsx 中定義的 GetWindowStyleEx 宏，取得要轉譯文字之視窗的擴充樣式旗標。


```C++
// Get the window extended style flagsfor the current window.
DWORD dwStyle = GetWindowExStyle(hwnd_);
```



宏會傳回由數個旗標所組成的 DWORD 值，並結合了位 OR 運算。 您必須判斷是否有影響讀取方向的特定旗標。

有兩個不同的旗標與閱讀方向相關： WS \_ ex \_ LAYOUTRTL 和 ws \_ ex \_ RTLREADING。

使用位 AND 運算子 (&) 搭配 dwStyle 變數和 WS \_ EX \_ LAYOUTRTL 宏來儲存布林值，指出配置是否經過鏡像處理。


```C++
// Is the WS_EX_LAYOUTRTL flag present?
BOOL bWSLayout = dwStyle & WS_EX_LAYOUTRTL;
```



針對 WS \_ EX RTLREADING 旗標進行相同的動作 \_ 。


```C++
// Is the WS_EX_RLTREADING flag present?
BOOL bWSReading = dwStyle & WS_EX_RTLREADING;
```



使用 [**IDWriteTextFormat：： SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) 方法設定讀取方向。 預設值為從左至右，因此您只需要設定從右至左的讀取方向。

> [!Note]  
> WS \_ EX \_ LAYOUTRTL 會鏡像整個版面配置，並隱含由右至左的閱讀方向，因此只有在其中一個旗標存在時，才會設定閱讀方向。 如果兩者都存在，則會彼此取消，而文字格式的讀取方向應該是由左至右。

 


```C++
// If either the WS_EX_LAYOUTRTL flag or the WS_EX_RLTREADING flag is present,
// but NOT BOTH, set the reading direction to right to left.
if ((bWSLayout && !bWSReading)
||  (!bWSLayout && bWSReading))
{
    pTextFormat_->SetReadingDirection(DWRITE_READING_DIRECTION_RIGHT_TO_LEFT);
}
```



 

 
