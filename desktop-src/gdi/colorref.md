---
Description: COLORRE光圈值是用來指定 RGB 色彩。
ms.assetid: b87d3de2-7a13-44ef-8253-c6851a75fa54
title: 'COLORREF (Windef) '
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 6836cfcc1b18d0b20d5e347fb83206551b27de06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104992451"
---
# <a name="colorref"></a>COLORREF

COLORRE光圈值是用來指定 [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) 色彩。


```C++
typedef DWORD COLORREF;
typedef DWORD* LPCOLORREF;
```



## <a name="remarks"></a>備註

指定明確的 [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) 色彩時， **COLORREF** 值的十六進位形式如下：

`0x00bbggrr`

低序位位元組包含相對強度的紅色值;第二個位元組包含綠色的值;第三個位元組包含藍色的值。 高序位位元組必須為零。 單一位元組的最大值是0xFF。

若要建立 **COLORREF** 色彩值，請使用 [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) 宏。 若要將色彩值的紅色、綠色和藍色元件的個別值解壓縮，請分別使用 [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue)、 [GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)和 [GetBValue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) 宏。

## <a name="example"></a>範例

```cpp
// Color constants.
const COLORREF rgbRed   =  0x000000FF;
const COLORREF rgbGreen =  0x0000FF00;
const COLORREF rgbBlue  =  0x00FF0000;
const COLORREF rgbBlack =  0x00000000;
const COLORREF rgbWhite =  0x00FFFFFF;
```

從 GitHub 上的 [Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples) 取得的範例。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                    |
| 標頭<br/>                   | <dl> <dt>Windef (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[色彩總覽](colors.md)
</dt> <dt>

[色彩結構](color-structures.md)
</dt> <dt>

[GetBValue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue)
</dt> <dt>

[GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)
</dt> <dt>

[**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue)
</dt> <dt>

[RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb)
</dt> </dl>

 

 




