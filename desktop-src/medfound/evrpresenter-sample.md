---
description: EVRPresenter 範例
ms.assetid: 791a9816-4c40-4683-8b32-22f73d7fe84d
title: EVRPresenter 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe874483313d96f2ee6d9481fca7695d3ecfdba492f3e976f9f6c107c6114b1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118063652"
---
# <a name="evrpresenter-sample"></a>EVRPresenter 範例

示範如何將 [增強型影片](enhanced-video-renderer.md) 轉譯器的自訂展示者 (EVR) 。 自訂展示者可以搭配 DirectShow EVR 篩選器或 Microsoft 媒體基礎 EVR 接收使用。

## <a name="apis-demonstrated"></a>示範的 Api

這個範例會示範下列媒體基礎介面：

-   [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient)
-   [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)
-   [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)
-   [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)

## <a name="usage"></a>使用方式

EVRPresenter 範例會建立一個 DLL，它是展示者的 COM 伺服器。 使用自訂展示者之前，您必須先註冊 DLL。

若要在媒體基礎中使用此範例：

1.  建置範例。
2.  Regsvr32 EvrPresenter.dll。
3.  建立並執行 [MFPlayer 範例](/previous-versions//bb970516(v=vs.85))。
4.  從 [ **檔案** ] 功能表選取 [ **開啟** 檔案]。
5.  在 [ **開啟** 檔案] 對話方塊中，選取 [ **自訂 EVR 展示者]。**
6.  選取要播放的檔案。

若要在 DirectShow 中使用此範例：

1.  建置範例。
2.  註冊 EvrPresenter.dll。
3.  建立並執行 EVRPlayer 範例。 此範例包含在 Windows SDK 中的 DirectShow 範例。
4.  **在 [檔案**] 功能表中，選取 [EVR 展示 **者**]。
5.  選取要播放的檔案。

## <a name="requirements"></a>規格需求



| 產品                                                        | 版本   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>下載範例

此範例可在[Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip)中取得。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[增強的影片轉譯器](enhanced-video-renderer.md)
</dt> <dt>

[如何撰寫 EVR 展示者](how-to-write-an-evr-presenter.md)
</dt> <dt>

[媒體基礎 SDK 範例](media-foundation-sdk-samples.md)
</dt> </dl>

 

 
