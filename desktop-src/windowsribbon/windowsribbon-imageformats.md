---
title: 指定功能區影像資源
description: Windows 功能區架構是一種豐富的命令呈現系統，其設計目的是要在功能區使用者介面 (UI) 中廣泛地支援影像資源。 所有影像資源都是在功能區標記中宣告，或從功能區主機應用程式進行查詢。
ms.assetid: 37b57992-8da8-4e6b-869d-72a136f6ad77
keywords:
- Windows功能區、影像資源
- 功能區、影像資源
- Windows功能區、透明度
- 功能區、透明度
- Windows功能區、色彩深度
- 功能區、色彩深度
- Windows功能區，對比
- 功能區，對比
- Windows 功能區中的影像資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c485de9c0d9d1b51b09d4a2b9dba95dd30a778922750a7f388c7a5c8963cda6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932584"
---
# <a name="specifying-ribbon-image-resources"></a>指定功能區影像資源

Windows 功能區架構是一種豐富的命令呈現系統，其設計目的是要在功能區使用者介面 (UI) 中廣泛地支援影像資源。 所有影像資源都是在 [功能區標記](windowsribbon-schema.md) 中宣告，或從功能區主機應用程式進行查詢。

針對 Windows 8 和更新版本，功能區架構支援下列圖形格式：32位 ARGB 點陣圖 (BMP) 檔和可移植網狀圖形 (PNG) 具有透明度的檔。

針對 Windows 7 及更早版本，影像資源必須符合 Windows 中所使用的標準 BMP 圖形格式。

> [!Note]  
> 如果提供不支援的影像格式給架構，則可能會發生編譯錯誤。

 

## <a name="image-sizes"></a>映射大小

若要在調整應用程式視窗大小時提供功能區控制項配置的更大彈性，功能區架構會以下列兩種大小的其中一種來接受和轉譯影像：大型或小型。

下圖說明透過彈性控制項配置支援多個功能區大小的功能區應用程式，以及使用可用的小型影像來取代大型影像。

下列螢幕擷取畫面顯示具有縮放控制項大型影像的功能區。

![螢幕擷取畫面，顯示使用縮放控制項之大型影像的功能區。](images/overviews/imageresources-largeimage.png)

下列螢幕擷取畫面顯示相同的功能區，以縮放控制項的小型影像調整大小

![螢幕擷取畫面，顯示針對縮放控制項使用小型影像的功能區。](images/overviews/imageresources-smallimage.png)

下列螢幕擷取畫面顯示功能區處於隱藏狀態。 當所有可能的控制項版面配置都已用盡，而且無法使用可用的應用程式工作區來轉譯功能區時，就會隱藏功能區。

![顯示折迭功能區的螢幕擷取畫面。](images/overviews/imageresources-noimage.png)

若為任何影像，確切的圖元大小取決於所使用監視器的顯示解析度或每英寸 (DPI) 的點。 在 96 DPI 時，大型影像的大小為32x32 圖元，而小型影像的大小為16x16 圖元。 影像大小會以線性方式增加，如下表所示。



| DPI     | 小型影像  | 大型影像  |
|---------|--------------|--------------|
| 96 DPI  | 16x16 圖元 | 32x32 圖元 |
| 120 DPI | 20x20 圖元 | 40x40 圖元 |
| 144 DPI | 24x24 圖元 | 48x48 圖元 |
| 192 DPI | 32x32 圖元 | 64x64 圖元 |



 

功能區架構會視需要調整影像資源。 不過，由於調整大小可能會產生不必要的成品和影像效能，因此強烈建議應用程式提供一組小型的影像資源，以跨越各種常用的 DPI 設定。 如果找不到完全相符的，則最接近的影像會向上或向下擴充。

為了方便這項工作，您可以使用每個 [**命令**](windowsribbon-element-command.md)專案的一組 [**影像**](windowsribbon-element-image.md)元素，在功能區標記中宣告影像資源。 在執行時間，架構會根據每個 **影像** 元素的 *MinDPI* 屬性，選取要顯示的影像。

> [!IMPORTANT]
>
> 當設計用來支援特定螢幕 DPI 設定的影像資源集合透過一組 [**影像**](windowsribbon-element-image.md)元素提供給功能區架構時，架構會使用 *MinDPI* 屬性值符合目前螢幕 DPI 設定的 **影像**。
>
> 如果未使用符合目前螢幕 DPI 設定的 *MinDPI* 值來宣告 [**影像**](windowsribbon-element-image.md)元素，則架構會挑選最接近目前螢幕 DPI 設定的最接近 *MinDPI* 值的 **影像**，並向上調整影像資源。 否則，如果未使用 *MinDPI* 屬性值（小於目前的螢幕 DPI 設定）來宣告 **影像** 元素，則架構會挑選大於目前螢幕 DPI 設定的最接近 *MinDPI* 值，並將影像資源向下調整。

 

下列範例說明如何宣告一組影像來容納各種功能區大小和系統設定。


```C++
<Command.LargeImages>
  <Image Source="res/CutLargeImage32.bmp" Id="116" Symbol="ID_CUT_LARGEIMAGE1" MinDPI="96" />
  <Image Source="res/CutLargeImage40.bmp" Id="117" Symbol="ID_CUT_LARGEIMAGE2" MinDPI="120" />
  <Image Source="res/CutLargeImage48.bmp" Id="118" Symbol="ID_CUT_LARGEIMAGE3" MinDPI="144" />
  <Image Source="res/CutLargeImage64.bmp" Id="119" Symbol="ID_CUT_LARGEIMAGE4" MinDPI="192" />
</Command.LargeImages>
<Command.SmallImages>
  <Image Source="res/CutSmallImage16.bmp" Id="122" Symbol="ID_CUT_SMALLIMAGE1" MinDPI="96" />
  <Image Source="res/CutSmallImage20.bmp" Id="123" Symbol="ID_CUT_SMALLIMAGE2" MinDPI="120" />
  <Image Source="res/CutSmallImage24.bmp" Id="124" Symbol="ID_CUT_SMALLIMAGE3" MinDPI="144" />
  <Image Source="res/CutSmallImage32.bmp" Id="125" Symbol="ID_CUT_SMALLIMAGE4" MinDPI="192" />
</Command.SmallImages>
<Command.LargeHighContrastImages>
  <Image Source="res/CutLargeImage32HC.bmp" Id="130" Symbol="ID_CUT_LARGEIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutLargeImage40HC.bmp" Id="131" Symbol="ID_CUT_LARGEIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutLargeImage48HC.bmp" Id="132" Symbol="ID_CUT_LARGEIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutLargeImage64HC.bmp" Id="133" Symbol="ID_CUT_LARGEIMAGE4HC" MinDPI="192" />
</Command.LargeHighContrastImages>
<Command.SmallHighContrastImages>
  <Image Source="res/CutSmallImage16HC.bmp" Id="135" Symbol="ID_CUT_SMALLIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutSmallImage20HC.bmp" Id="136" Symbol="ID_CUT_SMALLIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutSmallImage24HC.bmp" Id="137" Symbol="ID_CUT_SMALLIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutSmallImage32HC.bmp" Id="138" Symbol="ID_CUT_SMALLIMAGE4HC" MinDPI="192" />
</Command.SmallHighContrastImages>
```



如果在執行時間的標記中宣告的影像因為任何原因而失效，則會查詢主機應用程式是否有新的影像。 當這些映射以程式設計方式產生和載入時，應用程式應該會嘗試傳回根據 [SM \_ CXICON 系統](/windows/win32/api/winuser/nf-winuser-getsystemmetrics)計量所決定的預設系統圖示大小來調整大小的影像。

> [!Note]  
> 大型影像的 sm CXICON 大小為 sm \_ \_ CXICON，而小型影像的大小為 sm \_ CXICON/2，sm \_ CXICON/2。

 

## <a name="color-depth-transparency-and-contrast"></a>色彩深度、透明度和對比

一般影像預期會在每圖元32位 (BPP) ARGB 像素格式，並調整為預設系統圖示大小。 此格式支援透明和消除鋸齒 (使用每個通道) 的8位。

> [!WARNING]
> 在載入或儲存 32 BPP 影像時，許多影像編輯工具都不會保留最高順序的8位 Alpha 通道。

 

若要在高對比模式中正確顯示影像，其必須為 4 BPP palletized 像素格式。 轉譯影像時，功能區架構會根據影像的高對比內容重新對應特定色彩。

下表列出架構的高對比色彩轉譯行為。



像素色彩

RGB 值

行為

白色背景

深色背景

品紅

800080

透明

透明

黑

000000

色彩 \_ WINDOWTEXT

白色

白色

FFFFFF

色彩 \_ 視窗

黑

暗灰色

808080

色彩 \_ 3DSHADOW

色彩 \_ 3DSHADOW

灰色

C0C0C0

色彩 \_ 3DFACE

色彩 \_ 3DFACE

淺灰色

DFDFDF

色彩 \_ 3DLIGHT

色彩 \_ 3DLIGHT

深藍色

000080

n/a

白色



 

如需功能區架構所支援之影像格式的詳細資訊，請參閱下列各項：

-   [BITMAPINFOHEADER 結構](/previous-versions//dd183376(v=vs.85)) -描述 32 BPP ARGB 像素格式。
-   [CreateDIBSection](/windows/win32/api/wingdi/nf-wingdi-createdibsection) 函式-說明如何建立 32 BPP ARGB 像素格式的影像。
-   [LoadImage](/windows/win32/api/winuser/nf-winuser-loadimagea) 函式-說明如何載入 32 BPP ARGB 像素格式的影像。

## <a name="accessibility"></a>協助工具選項

依賴映射資源來提供資訊、傳達控制項功能，以及公開應用程式狀態，以在應用程式設計和開發期間增加協助工具需求的需求。

針對基本的高對比支援，功能區允許在高對比主題為使用中時，顯示一組個別的影像檔案。 這些影像可以是 32 BPP 或 4 BPP，其中的色彩會對應到特殊的小元件，其中的色彩會根據作用中高對比主題的前景和背景色彩反轉。

下列範例示範如何在功能區標記中宣告高對比影像資源：


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px.bmp" MinDPI="192" />
      </Command.LargeImages>
      <Command.LargeHighContrastImages>
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px-HC.bmp" MinDPI="192" />
      </Command.LargeHighContrastImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px.bmp" MinDPI="192" />
      </Command.SmallImages>
      <Command.SmallHighContrastImages>
        <Image Source="cmdNew-16px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="192" />
      </Command.SmallHighContrastImages>
    </Command>
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**SmallImages**](windowsribbon-element-command-smallimages.md)
</dt> <dt>

[UI \_ PKEY \_ SmallImage](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> <dt>

[**LargeImages**](windowsribbon-element-command-largeimages.md)
</dt> <dt>

[UI \_ PKEY \_ LargeImage](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> <dt>

[**SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)
</dt> <dt>

[UI \_ PKEY \_ SmallHighContrastImage](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> <dt>

[**LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)
</dt> <dt>

[UI \_ PKEY \_ LargeHighContrastImage](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md)
</dt> </dl>

 

 