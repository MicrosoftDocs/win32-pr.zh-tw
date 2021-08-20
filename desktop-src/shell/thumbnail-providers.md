---
description: WindowsVista 比舊版 Windows 更容易使用檔案專屬的縮圖影像。
title: 縮圖處理常式
ms.topic: article
ms.date: 07/02/2018
ms.assetid: ed9e17bb-aa28-4f8c-8b5a-9b57cab1c438
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 66641be49f8d118abc24c1a9a3fc8452fdacb51894452689276d87c910774d9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675710"
---
# <a name="thumbnail-handlers"></a>縮圖處理常式

WindowsVista 比舊版 Windows 更容易使用檔案專屬的縮圖影像。 WindowsVista 在所有的視圖、對話方塊以及提供它們的任何檔案類型中使用它們。 其他應用程式也可以使用您的縮圖。 縮圖顯示也已變更。 現在可以使用連續的使用者可選取大小，而不是在 Windows XP 中提供的圖示和縮圖等離散大小。

> [!Note]  
> 您可能會聽到這些縮圖稱為「即時」圖示。

 

32位解析度和大型256x256 圖元的縮圖通常用於 Windows Vista UI 中。 檔案格式擁有者應該準備好以該大小顯示其縮圖。 它們也應該針對反映特定檔案內容的縮圖提供非靜態影像。 例如，文字檔的縮圖應顯示檔的縮圖版本，包括其文字。

已引進 [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) 介面，可讓您更輕鬆且更直接地提供縮圖，而不是使用 [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) 。 請注意，在 Windows Vista 中，使用 **IExtractImage** 的現有程式碼仍然有效。 不過，在 **詳細資料** 窗格中不支援 **IExtractImage** 。

本主題將討論下列內容：

-   [縮圖流程](#thumbnail-processes)
-   [縮圖快取和調整大小](#thumbnail-cache-and-sizing)
-   [縮圖覆蓋](#thumbnail-overlays)
-   [縮圖裝飾](#thumbnail-adornments)
-   [註冊您的縮圖處理常式](#registering-your-thumbnail-handler)
-   [相關主題](#related-topics)

## <a name="thumbnail-processes"></a>縮圖流程

處理常式（包括縮圖處理常式）依預設會在個別進程中執行。 您可以在 [**IShellItem：： BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler)的呼叫中傳遞 **Null** 值作為系結內容，以強制處理常式在同進程執行，如下所示：


```
IShellItem::BindToHandler(NULL, BHID_ThumbnailHandler,..)
```



您也可以藉由在登錄中設定 DisableProcessIsolation 專案，選擇不使用進程外的程式，如本範例所示。 ) {E357FCCD-A995-4576-B01F-234630154E96} (CLSID 的類別識別碼是 [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) 執行的 clsid。

```
HKEY_CLASSES_ROOT
   CLSID
      {E357FCCD-A995-4576-B01F-234630154E96}
         DisableProcessIsolation = 1
```

## <a name="thumbnail-cache-and-sizing"></a>縮圖快取和調整大小

需要縮圖時，Windows 先檢查影像的縮圖快取。 如果在快取中找不到影像，則會呼叫縮圖解壓縮程式。 當映射的上次修改時間晚于快取中的複本時，也會呼叫它。

此快取中的縮圖影像會儲存成一組不同的大小。 所有大小都會以圖元為單位。

-   32x32
-   96x96
-   256 x 256
-   1024x1024

> [!Note]  
> 這些值可能會變更。 您的程式碼不應假設一律會使用任何特定的大小。

 

如果影像不是正方形，您就不應該自行填補。 Windows 負責遵循原始的外觀比例，並將影像填補為正方形大小。

當系統要求特定大小的影像時，除非找到完全相符的影像，否則 Windows Vista 一律會抓取下一個最大的影像，並將其向下調整為所要求的大小。 影像的大小絕對不會像舊版 Windows 中的情況一樣調整。

下表提供所要求大小和可用大小之間關聯性的一些範例。



| 您提供的映射大小上限 | 解壓縮程式要求的大小 | 您提供                                 |
|--------------------------------|---------------------------------|---------------------------------------------|
| 156x120                        | 256 x 256                         | 156x120 (不要填補、維持外觀比例)  |
| 2048x1024                      | 256 x 256                         | 256x128 (不要填補、維持外觀比例)  |



 

您可以在登錄中將截止點宣告為相關聯應用程式的程式識別碼專案的一部分。 在此大小以下時，不會使用縮圖。

```
HKEY_CLASSES_ROOT
   .{ProgId}
      ThumbnailCutoff
```

ThumbnailCutoff 專案是這些 REG DWORD 值的其中一個 \_ 。

| 值 | Cutoff | HighDPI 敏感性 |
|-------|--------|-------------------|
| 0     | 32x32  | 是               |
| 1     | 16x16  | Yes               |
| 2     | 48x48  | Yes               |
| 3     | 16x16  | Yes               |


每英寸的高點 (DPI) 敏感度表示縮圖的圖元尺寸會自動調整為較大的 DPI。 例如，在 96 DPI 的32x32 影像會是 120 DPI 的40x40 影像。

如果未指定 ThumbnailCutoff 專案，預設的截止值會是 20x20 (不會區分 DPI) 。

## <a name="thumbnail-overlays"></a>縮圖覆蓋

縮圖覆迭是在縮圖右下角顯示的小型影像，讓開發人員有機會將品牌辨識套用至縮圖。 覆迭會在登錄中宣告為相關聯應用程式的程式識別碼專案的一部分，如下所示：

```
HKEY_CLASSES_ROOT
   .{ProgId}
      TypeOverlay
```

TypeOverlay 專案包含的 REG \_ SZ 值會解讀如下：

-   如果此值是資源參考 (內嵌于 DLL 中的 **.ico** 檔案) 例如 `ISVComponent.dll,-155` ，該映射會用來做為具有該副檔名之檔案的覆迭。 請注意，在此範例中， **155** 是資源識別碼，而且如果 DLL 不存在於標準路徑中 (例如 C： **/Windows/System32**) ，則需要完整路徑，而不只是 dll 名稱。
-   如果此值為空字串，則不會對影像套用任何覆迭。
-   如果值不存在，則會使用相關聯應用程式的預設圖示。

縮圖的重迭只能透過此機制提供，並由 Windows 套用。 請勿自行套用覆迭。

## <a name="thumbnail-adornments"></a>縮圖裝飾

像是陰影的裝飾會根據使用者目前選取的主題套用至縮圖。 裝飾是由 Windows 提供;請勿自行建立。 Windows 可以隨時變更特定裝飾的外觀，因此，如果您擁有自己的擁有者，就會發生與系統同步的風險。 您的縮圖可能會看似已過期或不存在。

可能的裝飾會在登錄中宣告為相關聯應用程式的程式識別碼專案的一部分，如下所示：

```
HKEY_CLASSES_ROOT
   .{ProgId}
      Treatment
```

處理專案包含下列其中一個 REG \_ DWORD 值：



| 值 | 意義         |
|-------|-----------------|
| 0     | 無裝飾    |
| 1     | 陰影     |
| 2     | 相片框線    |
| 3     | 影片 Sprockets |


根據預設，陰影會套用至影像。

## <a name="registering-your-thumbnail-handler"></a>註冊您的縮圖處理常式

縮圖處理常式的註冊是以標準檔案關聯為基礎。

縮圖處理常式 Shell 延伸模組的 GUID 為 `E357FCCD-A995-4576-B01F-234630154E96` 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider)
</dt> <dt>

[建立縮圖處理常式](building-thumbnail-providers.md)
</dt> <dt>

[縮圖處理常式指導方針](thumbnail-provider-guidelines.md)
</dt> </dl>

 

 



