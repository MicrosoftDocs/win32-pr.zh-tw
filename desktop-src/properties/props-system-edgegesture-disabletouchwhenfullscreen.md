---
description: 當應用程式視窗處於作用中狀態，且處於全螢幕模式 (或擁有的視窗為使用中時，防止 edge 手勢的行為) 。
ms.assetid: F4242C05-181B-44FC-BE6C-8ABB76079981
title: EdgeGesture. DisableTouchWhenFullscreen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 208962f11b96420a8e0ef771ada846a3f802e815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996954"
---
# <a name="systemedgegesturedisabletouchwhenfullscreen"></a>EdgeGesture. DisableTouchWhenFullscreen

當應用程式視窗處於作用中狀態，且處於全螢幕模式 (或擁有的視窗為使用中時，防止 edge 手勢的行為) 。

> [!Note]  
> 在全螢幕模式中，應用程式視窗的大小與螢幕解析度相符。

 

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10，1703版、Windows 10、1607版、Windows 10、1511版、Windows 10、version 1507、Windows 8.1、Windows 8

```
propertyDescription
   name = System.EdgeGesture.DisableTouchWhenFullscreen
   shellPKey = PKEY_EdgeGesture_DisableTouchWhenFullscreen
   formatID = 32CE38B2-2C9A-41B1-9BC5-B3784394AA44
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a>備註

在 Windows 8 中，與畫面邊緣互動的使用者會顯示系統 UI，例如應用程式橫條、常用鍵和執行中的應用程式。

針對全螢幕的遠端應用程式，本機電腦上的這個 UI 行為可能會覆寫並干擾遠端會話的 UI。 這個屬性可讓應用程式停用本機電腦上的 edge UI。

若要停用 edge UI，請將此屬性設定為 VARIANT \_ TRUE。 預設值為 VARIANT \_ FALSE。

這個屬性不會影響 Windows Store 應用程式。

下列範例顯示如何設定 edge UI 行為。


```
HRESULT SetTouchDisableProperty(HWND hwnd, BOOL fDisableTouch)
{
    IPropertyStore* pPropStore;
    HRESULT hrReturnValue = SHGetPropertyStoreForWindow(hwnd, IID_PPV_ARGS(&pPropStore));
    if (SUCCEEDED(hrReturnValue))
    {
        PROPVARIANT var;
        var.vt = VT_BOOL;
        var.boolVal = fDisableTouch ? VARIANT_TRUE : VARIANT_FALSE;
        hrReturnValue = pPropStore->SetValue(PKEY_EdgeGesture_DisableTouchWhenFullscreen, var);
        pPropStore->Release();
    }
    return hrReturnValue;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> </dl>

 

 
