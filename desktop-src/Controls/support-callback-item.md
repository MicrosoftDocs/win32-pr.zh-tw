---
title: 如何支援回呼專案
description: 本主題將示範如何提供回呼專案的支援。
ms.assetid: BD32666F-9445-4871-AE21-5DC9F5FC9C1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 056f64c086aeda94ccf928d93ae2c5db5e2187a4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933726"
---
# <a name="how-to-support-callback-items"></a>如何支援回呼專案

本主題將示範如何提供回呼專案的支援。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示


如果您的應用程式將會使用 ComboBoxEx 控制項中的回呼專案，必須準備好處理 [CBEN \_ GETDISPINFO](cben-getdispinfo.md) 通知程式碼。 ComboBoxEx 控制項會在需要擁有者來提供特定專案資訊時傳送此通知。 如需回呼專案的詳細資訊，請參閱 [回呼專案](comboboxex-controls.md)。

下列應用程式定義函式會藉由提供指定專案的屬性來處理 [CBEN \_ GETDISPINFO](cben-getdispinfo.md) 。 請注意，它會將傳入 [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema)結構的 **遮罩** 成員設定為 CBEIF \_ DI \_ SETITEM。 將 **mask** 設定為這個值會讓控制項保留專案資訊，讓它不需要再次要求資訊。

## <a name="complete-example"></a>完整範例


```C++
// DoItemCallback - Processes CBEN_GETDISPINFO by providing item
// attributes for a given callback item.

void WINAPI DoItemCallback(PNMCOMBOBOXEX pNMCBex)
{
    DWORD dwMask = pNMCBex->ceItem.mask;

    if(dwMask & CBEIF_TEXT)
    {
            // Insert code to provide item text.
    }

    if(dwMask & CBEIF_IMAGE) 
    {
        // Insert code to provide an item image index.
    }

    // Insert code to provide other callback information as desired.

    // Make the ComboBoxEx control hold onto the item information.
    pNMCBex->ceItem.mask = CBEIF_DI_SETITEM;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 ComboBoxEx 控制項](comboboxex-controls.md)
</dt> <dt>

[ComboBoxEx 控制項參考](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[使用 ComboBoxEx 控制項](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 