---
title: 如何使用 TOM Guid
description: 在 MIDL 介面語句內的 Tom 中，會提供文字物件模型 (TOM) Guid \_ 。 若要使用相關聯的介面，您必須先使用 GUID 宣告介面。
ms.assetid: 48FF98C9-D42E-4E7F-874F-8E56F730E24E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c5c892ecac4b13a6e74aedad6c2a373908d2173c105ab0dbb0ec49c1439c36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828529"
---
# <a name="how-to-use-tom-guids"></a>如何使用 TOM Guid

在 MIDL 介面語句內的 Tom 中，會提供文字物件模型 (TOM) Guid \_ 。 若要使用相關聯的介面，您必須先使用 GUID 宣告介面。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="use-a-tom-guid"></a>使用 TOM GUID

下列範例程式碼示範如何使用 [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) 介面。


```C++
#define DEFINE_GUIDXXX(name, l, w1, w2, b1, b2, b3, b4, b5, b6, b7, b8) \
        EXTERN_C const GUID CDECL name \
                = { l, w1, w2, { b1, b2,  b3,  b4,  b5,  b6,  b7,  b8 } }

DEFINE_GUIDXXX(IID_ITextDocument,0x8CC497C0,0xA1DF,0x11CE,0x80,0x98,
                0x00,0xAA,0x00,0x47,0xBE,0x5D);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Text 物件模型](using-the-text-object-model.md)
</dt> <dt>

[使用 Rich Edit 控制項](using-rich-edit-controls.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




