---
description: 宣告篩選資訊
ms.assetid: ed3c1d44-ccef-4dde-819b-f5d4d3be6d1e
title: 宣告篩選資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c22fb13b524bed56e8cc9d51e573f2729f843e56565db2793d1a8b4568af52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953197"
---
# <a name="declaring-filter-information"></a>宣告篩選資訊

第一個步驟是視需要宣告篩選資訊。 DirectShow 定義下列用來描述篩選、釘選和媒體類型的結構：



| 結構                                               | 描述             |
|---------------------------------------------------------|-------------------------|
| [**AMOVIESETUP \_ 篩選**](amoviesetup-filter.md)       | 描述篩選。     |
| [**AMOVIESETUP \_ 釘選**](amoviesetup-pin.md)             | 描述 pin。        |
| [**AMOVIESETUP \_ 媒體媒體**](amoviesetup-mediatype.md) | 描述媒體類型。 |



 

這些結構是嵌套的。 **AMOVEIESETUP \_ 篩選** 結構有指向 **AMOVIESETUP \_ 釘** 選結構陣列的指標，其中每個結構都有指向 **AMOVEIESETUP \_ 媒體** 陣列的指標。 這些結構會結合在一起，以提供足夠的資訊給 [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) 介面，以找出篩選。 它們並不是篩選的完整描述。 例如，如果篩選器會建立多個相同 pin 的實例，您應該只針對該 pin 宣告一個 [**AMOVIESETUP \_ 釘**](amoviesetup-pin.md) 選結構。 此外，不需要篩選以支援其所註冊的每個媒體類型組合;也不需要註冊每個支援的媒體類型。

將設定結構宣告為 DLL 內的全域變數。 下列範例顯示具有一個輸出圖釘的篩選準則：


```C++
static const WCHAR g_wszName[] = L"Some Filter";

AMOVIESETUP_MEDIATYPE sudMediaTypes[] = {
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB24 },
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB32 },
};

AMOVIESETUP_PIN sudOutputPin = {
    L"",            // Obsolete, not used.
    FALSE,          // Is this pin rendered?
    TRUE,           // Is it an output pin?
    FALSE,          // Can the filter create zero instances?
    FALSE,          // Does the filter create multiple instances?
    &GUID_NULL,     // Obsolete.
    NULL,           // Obsolete.
    2,              // Number of media types.
    sudMediaTypes   // Pointer to media types.
};

AMOVIESETUP_FILTER sudFilterReg = {
    &CLSID_SomeFilter,      // Filter CLSID.
    g_wszName,              // Filter name.
    MERIT_NORMAL,           // Merit.
    1,                      // Number of pin types.
    &sudOutputPin           // Pointer to pin information.
};
```



篩選名稱會宣告為靜態全域變數，因為它將會再次用於其他地方。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何註冊 DirectShow 篩選準則](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



