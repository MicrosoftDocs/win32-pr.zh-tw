---
title: 將屬性新增至範例音訊 DSP 外掛程式
description: 將屬性新增至範例音訊 DSP 外掛程式
ms.assetid: 9c6c2a34-4844-476b-8814-a95a236e75bb
keywords:
- Windows Media Player 外掛程式、音訊 DSP
- 外掛程式、音訊 DSP
- 數位信號處理外掛程式，音訊屬性
- DSP 外掛程式、音訊屬性
- 音訊 DSP 外掛程式，屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d180ab1054631b09997ac986529a641e6ff05ec3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969657"
---
# <a name="adding-properties-to-the-sample-audio-dsp-plug-in"></a>將屬性新增至範例音訊 DSP 外掛程式

Windows Media Player 外掛程式 Wizard 產生的音訊 DSP 範例程式碼會使用代表音訊音量比例因數的單一屬性。 您的外掛程式可能需要一個以上的屬性。 您可以使用下列步驟，在 Visual Studio 中輕鬆地將屬性新增至您的 DSP 外掛程式：

-   在屬於 proxy 存根專案一部分的 IDL 檔案中，定義介面定義程式碼中的方法。
    -   將方法執行程式新增至專案的主要 CPP 檔案：

    ```C++
    STDMETHODIMP CYourProject::get_color(COLORREF *pColor)
    {
        if ( NULL == pColor )
        {
            return E_POINTER;
        }

        *pColor = m_Color;

        return S_OK;
    }

    STDMETHODIMP CYourProject::put_color(COLORREF newColor)
    {
        m_Color = newColor;
        
        return S_OK;
    }
    
    ```

    

最後，為了讓使用者可以存取屬性，您會想要對屬性頁的執行進行變更。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行音訊 DSP 外掛程式**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




