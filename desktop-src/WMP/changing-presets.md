---
title: 變更預設值
description: 變更預設值
ms.assetid: f8a5565d-676b-4679-a4cb-4bd7551cf41c
keywords:
- 視覺效果、光暈範例
- 自訂視覺效果，發光範例
- 程式設計指南，視覺效果
- 範例，發光視覺效果
- 發光視覺效果範例
- 視覺效果，預設
- 自訂視覺效果，預設
- 視覺效果中的預設值，發光範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03828614093836c5f9a3b422167b62f11b8f2489eb30556d42a2d80495935ec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863908"
---
# <a name="changing-presets"></a>變更預設值

下列預設的程式碼區段已變更為允許三個預設值：

## <a name="getpresettitle"></a>GetPresetTitle

插入此程式碼以取代產生的預設程式碼：


```C++
    switch (nPreset)
    {
    case PRESET_RED:
        bstrTemp.LoadString(IDS_REDPRESETNAME); 
        break;

    case PRESET_GREEN:
        bstrTemp.LoadString(IDS_GREENPRESETNAME); 
        break;

    case PRESET_BLUE:
        bstrTemp.LoadString(IDS_BLUEPRESETNAME); 
        break;
    }

```



## <a name="enumerations"></a>列舉

下列在 h.264 中的列舉已變更為允許三個預設：


```C++
enum {
    PRESET_RED = 0,
    PRESET_GREEN,
    PRESET_BLUE,
    PRESET_COUNT
};

```



## <a name="resource-header"></a>資源標頭

下列資源定義于 resources 中，以允許三個預設：


```C++
#define IDS_REDPRESETNAME               102
#define IDS_GREENPRESETNAME             103
#define IDS_BLUEPRESETNAME              104

```



請注意，您也必須將 **\_ APS \_ NEXT \_ SYMED \_ 值** 的資源編號變更為106。

## <a name="resource-file"></a>資源檔案

您必須在 Glowdll .rc 檔中變更下列字串，以允許三個預設值，並為其指定名稱：


```C++
    IDS_REDPRESETNAME       "Glow Red"
    IDS_GREENPRESETNAME     "Glow Green"
    IDS_BLUEPRESETNAME      "Glow Blue"

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**發光範例**](the-glow-sample.md)
</dt> </dl>

 

 




