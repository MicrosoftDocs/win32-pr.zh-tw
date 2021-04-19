---
description: 以 DES 撰寫 Windows Media 檔案
ms.assetid: 741ebcbc-62fb-4c7f-845f-a361f5b63f8c
title: 以 DES 撰寫 Windows Media 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0626a3ef609dee87d90a6d3c2caa023e9ac9a29a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106986450"
---
# <a name="writing-a-windows-media-file-in-des"></a>以 DES 撰寫 Windows Media 檔案

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

本節說明如何使用 (DES) 的 [DirectShow 編輯服務](directshow-editing-services.md) 來撰寫 Windows Media 檔案。

> [!IMPORTANT]
> 請勿使用智慧型轉譯引擎來寫入 Windows Media 檔案。 請一律使用基本轉譯引擎 (CLSID \_ RenderEngine) 。

 

若要寫入 Windows Media 檔案，請執行下列動作：

1.  使用您的金鑰提供者指標，在轉譯引擎上呼叫 **SetSite** 。
2.  建立圖形的前端。  (查看轉譯 [專案](rendering-a-project.md)。 ) 
3.  建立 [WM ASF 寫入](wm-asf-writer-filter.md) 器篩選器，並將它新增至圖形。
4.  使用 WM ASF 寫入器篩選器上的 [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) 介面來設定檔案名。
5.  將 WM ASF 寫入器設定為使用 Windows Media 設定檔。 每個設定檔都有預先定義的資料流程數目。 您必須選擇符合專案中群組的設定檔。

    [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)介面包含一些不同的方法來設定設定檔。 例如， **ConfigureFilterUsingProfileGuid** 方法會指定系統設定檔做為 GUID。 或者，您可以使用 Windows Media 格式方法來取得 **IWMProfile** 指標，然後呼叫 [**IConfigAsfWriter：： ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile)。 如需詳細資訊，請參閱設定 [ASF 寫入器](configuring-the-asf-writer.md)。

6.  將前端連接到 ASF 寫入器。 圖形的前端包含每個群組的一個輸出圖釘。 假設您指定了相容的設定檔，ASF 寫入器應該會有一組相符的輸入圖釘。 將每個輸出圖釘連接至對應的輸入 pin。 最簡單的方法是使用 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法。 首先，建立「 [Capture graph](capture-graph-builder.md) 產生器」的新實例，並使用篩選圖形管理員的指標將它初始化：

    ```C++
    ICaptureGraphBuilder2 *pBuild = 0;
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 0, CLSCTX_INPROC_SERVER,
        IID_ICaptureGraphBuilder2, (void**)&pBuild);
    pBuild->SetFiltergraph(pGraph); 
    ```

    

    接下來，藉由呼叫 [**IRenderEngine：： GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) 方法，取得每個群組的輸出圖釘。 呼叫 **RenderStream** 將 pin 連接至 ASF 寫入器：

    ```C++
    long cGroups = 0;
    hr = pTimeline->GetGroupCount(&cGroups);
    for (long i = 0; i < cGroups; i++)
    {
        IPin *pPin;
        hr = pRenderEngine->GetGroupOutputPin(i, &pPin);
        if (SUCCEEDED(hr))
        {
            hr = pBuild->RenderStream(0, 0, pPin, 0, pASF);
        }
        pPin->Release();
    }
    pBuild->Release
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用具有 DirectShow 編輯服務的 Windows Media](using-windows-media-with-directshow-editing-services.md)
</dt> </dl>

 

 



