---
description: 使用具有 DirectShow 編輯服務的 Windows Media
ms.assetid: 26a88197-ec80-4443-9d50-e11df40dd1eb
title: 使用具有 DirectShow 編輯服務的 Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18fbfe715495834217b695f887305f1ecb21cb6f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106986434"
---
# <a name="using-windows-media-with-directshow-editing-services"></a>使用具有 DirectShow 編輯服務的 Windows Media

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

本節說明如何在 [DirectShow 編輯服務](directshow-editing-services.md) (DES) 應用程式中使用 Windows Media 內容。 有兩個主要案例：

-   來源剪輯。 DES 專案可以包含來自 Windows Media 檔案的音訊和影片剪輯。
-   目標格式。 Windows Media 是影片編輯專案最終輸出的理想格式。

若要使用 Windows Media 檔案，應用程式必須提供軟體憑證，也稱為金鑰。 它會藉由執行金鑰提供者物件來完成這項工作。 金鑰提供者是公開 **IServiceProvider** 介面的 COM 物件。 如需有關如何執行金鑰提供者的詳細資訊，請參閱 [解除鎖定 Windows Media FORMAT SDK](unlocking-the-windows-media-format-sdk.md)。

若要搭配使用 DES 與 Windows Media 檔案，下列 DES 物件需要軟體金鑰：

-   轉譯引擎，用於預覽或寫入檔案。
-   MediaDet 物件，用來從 ASF 檔案取得影片框架或媒體類型。
-   \[!重要\]  
    > 請勿使用智慧型轉譯引擎來讀取或寫入 Windows Media 檔案。 請一律使用基本轉譯引擎 (CLSID \_ RenderEngine) 。

     

若要為物件提供軟體金鑰，請查詢 **IObjectWithSite** 介面的物件，並以您的金鑰提供者指標呼叫 **IObjectWithSite：： SetSite** 。 例如，下列程式碼會提供軟體金鑰給轉譯引擎：


```C++
// Create your key provider, using an application-defined function:
IServiceProvider *pKey;
hr = MyCreateKeyProviderFunction(&pKey);  

// Query the Render Engine for IObjectWithSite.
IObjectWithSite *pOWS;
hr = pRenderEngine->QueryInterface(__uuidof(IObjectWithSite), 
    reinterpret_cast<void**>(&pOWS));
if (SUCCEEDED(hr))
{
    // Give it your key provider.
    hr = pOWS->SetSite(pKey);
    pOWS->Release();
}
pKey->Release();
```



若要在 DES 專案中使用 Windows Media source 剪輯，只要在轉譯引擎上呼叫 **IObjectWithSite：： SetSite** ，並使用您的金鑰提供者指標。

如需撰寫 Windows Media 檔案的相關資訊，請參閱 [以 DES 撰寫 Windows media](writing-a-windows-media-file-in-des.md)檔案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DirectShow 編輯服務](using-directshow-editing-services.md)
</dt> </dl>

 

 



