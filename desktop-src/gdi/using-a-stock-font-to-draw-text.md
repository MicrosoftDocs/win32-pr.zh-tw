---
description: 系統提供六種股票字型。
ms.assetid: 349ea57f-dd25-4e33-bbdf-63a320eae3a0
title: 使用股票字型來繪製文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9bd140a931a13f6232235036fb7b9cf3de1a20505666e869f214219b7a60a95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468328"
---
# <a name="using-a-stock-font-to-draw-text"></a>使用股票字型來繪製文字

系統提供六種股票字型。 股票字型是一種邏輯字型，可讓應用程式藉由呼叫 [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) 函式並指定要求的字型來取得。 下列清單包含您可以指定的值，以取得股票字型。



| 值                 | 意義                                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ANSI \_ 固定 \_ 字型     | 根據 Windows 字元集指定等寬字型。 通常會使用一個宋體。                                                                                                                                                                                                |
| ANSI \_ VAR \_ 字型       | 根據 Windows 字元集來指定比例字型。 通常會使用 MS Sans Serif。                                                                                                                                                                                              |
| 裝置 \_ 預設 \_ 字型 | 指定指定裝置的慣用字型。 這通常是顯示裝置的系統字型;不過，對於某些點矩陣印表機，這是在裝置上的字型。 使用這個字型 (列印的速度通常比使用下載的點陣圖字型) 的列印速度還要快。    |
| OEM \_ 固定 \_ 字型      | 根據 OEM 字元集指定等寬字型。 針對 IBM 電腦和 compatibles，OEM 字型是以 IBM PC 字元集為基礎。                                                                                                                                                 |
| 系統 \_ 字型          | 指定系統字型。 這是根據 Windows 字元集的比例字型，由作業系統用來顯示視窗標題、功能表名稱，以及對話方塊中的文字。 系統字型一律可供使用。 其他字型則只有在已安裝時才可使用。 |
| 系統 \_ 固定 \_ 字型   | 指定與舊版 Windows 中的系統字型相容的等寬字型。                                                                                                                                                                                                        |



 

如需字型的詳細資訊，請參閱 [關於](about-fonts.md)字型。

下列範例會取出變數股票字型的控制碼、將其選取為裝置內容，然後使用該字型來寫入字串：


```C++
HFONT hFont, hOldFont; 

// Retrieve a handle to the variable stock font.  
hFont = (HFONT)GetStockObject(ANSI_VAR_FONT); 

// Select the variable stock font into the specified device context. 
if (hOldFont = (HFONT)SelectObject(hdc, hFont)) 
{
    // Display the text string.  
    TextOut(hdc, 10, 50, L"Sample ANSI_VAR_FONT text", 25); 

    // Restore the original font.        
    SelectObject(hdc, hOldFont); 
}
```



如果無法使用其他股票字型， [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) 會傳回系統字型的控制碼 (系統 \_ 字型) 。 只有當應用程式的裝置內容的對應模式是 MM TEXT 時，才應該使用股票字型 \_ 。

 

 



