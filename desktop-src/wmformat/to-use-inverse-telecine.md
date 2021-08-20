---
title: 使用反轉電影處理
description: 使用反轉電影處理
ms.assetid: 7752d1ac-34b1-446a-a69c-29463c9e10f7
keywords:
- Windows媒體格式 SDK，反向電視
- Windows媒體格式 SDK，電影
- Advanced Systems Format (ASF) ，反向電視
- ASF (Advanced Systems Format) ，反向電視
- Advanced Systems Format (ASF) ，電影
- ASF (Advanced Systems Format) ，電影
- 反向電影
- 電影
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7885caffea83460d73b1eca26dbfd94eb50d99ac4aa8589113875ffc4358c029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585318"
---
# <a name="to-use-inverse-telecine"></a>使用反轉電影處理

電視影片是將每秒24個畫面格的電影轉換成影片60，每秒 (半框架) 的影片。 此程式會將每個影片框架中的影像放在多個影片欄位中。

當您使用電影來數位編碼從電影建立的影片時，壓縮程式可能會造成運動成品和其他降低品質。 為了避免影響數位輸出的品質，Windows Media 視訊9編解碼器支援反向電視電影。 使用反向電視影片時，編解碼器會在編碼內容之前，從輸入影片重建原始的24個影片畫面格。

若要使用反向電視電影，您必須：

-   使用設定檔，並將影片串流設定為每秒24個畫面格。
-   知道輸入影片的欄位設定。

若要使用反向電視來輸入寫入器的輸入，請執行下列步驟。

1.  照常設定寫入器。 如需詳細資訊，請參閱 [寫入 ASF](writing-asf-files.md)檔。
2.  開始撰寫範例之前，請呼叫 **IWMWriter：： QueryInterface** 來取得 [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)介面的指標。
3.  針對所需的輸入編號呼叫 [**IWMWriterAdvanced2：： SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) ，以識別要重建的資料流程。 將 g \_ wszDeinterlaceMode 當作設定，並以 WM \_ DM \_ 的方式，將 \_ INVERSETELECINE 作為值進行傳遞。
4.  再次呼叫 **SetInputSetting** ，以設定 g \_ wszInitialPatternForInverseTelecine。
5.  照常寫入檔案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Advanced 主題**](advanced-topics.md)
</dt> <dt>

[**IWMWriter 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**IWMWriterAdvanced2 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)
</dt> </dl>

 

 




