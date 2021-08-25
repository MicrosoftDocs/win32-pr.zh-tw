---
description: 瞭解列印架構中的使用者可設定關鍵字，以進行色彩管理，例如 PageColorManagement 和 PageBlackGenerationProcessing。
ms.assetid: 296255b8-fe5c-46dd-b717-487aaae0db80
title: 色彩管理和列印架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e7e5a86b9f598183a4b3765e1cc38836b4ee7bb62e1835e06575392771dc5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846381"
---
# <a name="color-management-and-the-print-schema"></a>色彩管理和列印架構

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

使用者可設定的元素關鍵字可以是 XPS 專屬或非 XPS 特定。 如果它們不是 XPS 專用，關鍵字可能會用於舊版的 GDI 式列印。 如果應用程式決定在 PrintTicket 中設定這些關鍵字，驅動程式會根據列印架構中所呈現的定義，決定要採取的適當動作和行為。 任何這些關鍵字都可以在 ICM 的內容中使用。 如需詳細資訊，請參閱 Windows Vista SDK。



| 列印架構使用者可設定關鍵字       | DEVMODE 相等     | XPS 特定   |
|----------------------------------------------|------------------------|----------------|
| PageColorManagement<br/>               | dmICMMethod<br/> | No<br/>  |
| PageBlackGenerationProcessing<br/>     | 無<br/>        | Yes<br/> |
| PageBlendColorSpace<br/>               | 無<br/>        | Yes<br/> |
| PageSourceColorProfile<br/>            | 無<br/>        | No<br/>  |
| PageDestinationColorProfile<br/>       | 無<br/>        | No<br/>  |
| PageICMRenderingIntent<br/>            | dmICMIntent<br/> | No<br/>  |
| JobOptimalDestinationColorProfile<br/> | 無<br/>        | No<br/>  |
| PageDeviceColorSpaceUsage<br/>         | 無<br/>        | Yes<br/> |



 

## <a name="pagecolormanagement-system-handling"></a>PageColorManagement 系統處理

若為 PageColorManagement，系統會提供自動處理 PrintTicket 至 DEVMODE 或 DEVMODE 轉換（如有必要）。 這取決於應用程式 (Win32 或 WPF) 之間的特定列印路徑，以及 (以 GDI 為基礎或 XPSDrv) 的驅動程式。 如果從 Windows Presentation Foundation 應用程式列印到 Microsoft XPSDrv 列印驅動程式，則不應在 PrintTicket 或 PrintCapabilities 檔中通告系統的 PageColorManagement 公用選項;在此情況下，系統無法自動處理色彩管理。 從 Win32 應用程式列印到 Microsoft XPSDrv 列印驅動程式，可能會導致應用程式與 GDI 之間的色彩管理不過，在轉換成 XPS 格式之後，XPS 檔與驅動程式和/或裝置之間將不會自動處理色彩管理的系統，因為 XPS 格式標記每個元素都有完整的色彩資訊，而且會由驅動程式或裝置來處理此資訊。



| PageColorManagement 公用選項 | DEVMODE 值                  |
|------------------------------------|--------------------------------|
| 無<br/>                    | DMICMMETHOD \_ 無<br/>   |
| 裝置<br/>                  | DMICMMETHOD \_ 裝置<br/> |
| 驅動程式<br/>                  | DMICMMETHOD \_ 驅動程式<br/> |
| 系統<br/>                  | DMICMMETHOD \_ 系統<br/> |



 

## <a name="pageicmrenderingintent-system-handling"></a>PageICMRenderingIntent 系統處理

若為 PageICMRenderingIntent，系統會提供自動處理 PrintTicket 至 DEVMODE 或 DEVMODE 轉換（如有必要）。 這取決於應用程式 (Win32 或 Windows Presentation Foundation) 之間的特定列印路徑，以及 (以 GDI 為基礎或 XPSDrv) 的驅動程式。



| PageICMRenderingIntent 公用選項 | DEVMODE 值                       |
|---------------------------------------|-------------------------------------|
| AbsoluteColorimetric<br/>       | DMICM \_ ABS \_ 色度<br/> |
| RelativeColorimetric<br/>       | DMICM \_ 色度<br/>      |
| 照片<br/>                | DMICM \_ 對比<br/>          |
| BusinessGraphics<br/>           | DMICM \_ 飽和<br/>          |



 

除了 PageColorManagement 或) PageICMRenderingIntent 以外，其他所有色彩管理相關關鍵字 (不會有這類自動處理。

## <a name="joboptimaldestinationcolorprofile-and-pagedestinationcolorprofile-usage"></a>JobOptimalDestinationColorProfile 和 PageDestinationColorProfile 使用量

應用程式可能會決定查詢 PrintCapabilities 檔以進行 JobOptimalDestinationColorProfile。 這可為應用程式提供最佳色彩設定檔，提供 PrintCapabilities 檔中定義的目前裝置設定。 如果應用程式決定要讓驅動程式對 JobOptimalDestinationColorProfile 所指定的目的地色彩設定檔執行色彩管理，則 PageColorManagement 和 PageDestinationColorProfile 會分別設定為 [驅動程式] 和 [DriverConfiguration]。 如果應用程式不想使用 JobOptionalDestinationColorProfile 並選擇使用它自己的，則應該將 PageColorManagement 設定為 [無]，並將 PageDestinationColorProfile 設定為 PrintTicket 中的 [應用程式]，以傳達應用程式已經對其指定的目的地色彩設定檔執行色彩管理。 另一種情況可能會在應用程式選擇使用驅動程式 PrintCapabilities 所傳回的最佳目的地色彩設定檔時，但決定自行進行色彩管理時也會發生。 在此情況下，PageColorManagement 會設定為 [無]，而 PageDestinationColorProfile 會設定為 [應用程式]。

## <a name="pagesourcecolorprofile-usage"></a>PageSourceColorProfile 使用方式

針對 PageSourceColorProfile，無論針對 PageColorManagement 選取的選項為何，應用程式都可以針對 PrintTicket 中的每個頁面指定來源色彩設定檔。 無論是否存在，驅動程式都會根據列印架構中所呈現的定義，決定每個案例的行為。 例如，應用程式可能會將 PageColorManagement 設定為 None，然後未在 PrintTicket 中設定 PageSourceColorProfile。 應用程式也可以設定 PageColorManagement 至驅動程式，然後在 PrintTicket 中設定 PageSourceColorProfile;在此情況下，此驅動程式會負責判斷 PrintSchema 指導方針內的行為。

## <a name="pagedevicecolorspaceusage"></a>PageDeviceColorSpaceUsage

PageDeviceColorSpaceUsage 是應用程式所設定的 XPS 特定使用者可設定元素。 它會針對 XPS 檔中相關聯的色彩空間設定檔處理，在 PrintTicket 中設定適當的選項，以提供裝置的指示。 應用程式和/或現有的 PrintTicket 可以在傳送至裝置的 PrintTicket 中指定這個關鍵字。 無論是否存在，驅動程式都會根據列印架構中所呈現的定義，決定每個案例的行為。

## <a name="print-schema-color-management-example-flow"></a>列印架構色彩管理範例 Flow

下圖說明使用色彩管理和列印架構的最可能案例的流程。 為了簡化和可讀性，只有下列使用者可設定的列印架構關鍵字會用來示範其使用方式： PageColorManagement、JobOptimalDestinaionColorProfile、PageSourceColorProfile 和 PageDestinationColorProfile。 實線表示應該發生的動作，而虛線表示可能會發生的動作。 下列案例不是會在應用程式、驅動程式和系統之間產生的保證互動，而是代表將會發生的最常見使用案例。

![顯示如何處理色彩管理設定的圖表](images/local-1992284846-colormanagementtest3.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




