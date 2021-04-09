---
description: IWiaImageFilter 介面是由影像處理篩選器開發人員所執行，並由 Windows 映像取得 (WIA) 2.0 所呼叫的延伸模組介面。
ms.assetid: 2abe913b-bb2b-486d-a3f4-d5932433fc82
title: 'IWiaImageFilter 介面 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 8d859b79d15db627bb09cb60f758791a8b5860f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849352"
---
# <a name="iwiaimagefilter-interface"></a>IWiaImageFilter 介面

**IWiaImageFilter** 介面是由影像處理篩選器開發人員所執行，並由 Windows 映像取得 (WIA) 2.0 所呼叫的延伸模組介面。

## <a name="members"></a>成員

**IWiaImageFilter** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IWiaImageFilter** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWiaImageFilter** 介面具有這些方法。



| 方法                                                                | 描述                                                                                             |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**ApplyProperties**](-wia-iwiaimagefilter-applyproperties.md)       | 可讓影像處理篩選器將屬性寫回驅動程式 (和裝置) 。<br/>     |
| [**FilterPreviewImage**](-wia-iwiaimagefilter-filterpreviewimage.md) | 篩選預覽影像。<br/>                                                                   |
| [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md)     | 初始化篩選。 在每個影像下載之前，由 WIA 2.0 呼叫。 <br/>                       |
| [**SetNewCallback**](-wia-iwiaimagefilter-setnewcallback.md)         | 針對要用於轉送呼叫的影像處理篩選設定新的應用程式回呼。<br/> |



 

## <a name="remarks"></a>備註

影像處理篩選器開發人員應該執行這個介面和 [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) 介面。

WIA 2.0 會呼叫篩選方法。 永遠不會直接從應用程式呼叫。

Microsoft 會提供 WIA 2.0 Preview 元件，它會快取從掃描器取得的原始、未篩選的預覽影像。 應用程式會使用 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來共同建立 WIA 2.0 Preview 元件 (CLSID WiaPreview) 的實例 \_ ，這會使用 [**IWiaItem2：： GetExtension**](-wia-iwiaitem2-getextension.md)載入篩選。 當應用程式呼叫 IWiaTransfer 時，會自動呼叫篩選準則 [**：:D 下載 o)**](-wia-iwiatransfer-download.md)。

掃描影像時，一律會執行影像處理篩選。 應用程式無法從掃描器取得影像，而不需要先套用圖像篩選。

篩選準則必須至少執行亮度和對比。 可為使用者提供亮度和對比控制項的一般 UI 可顯示精確的使用者預覽。

影像處理篩選絕對不應該修改 [**WiaTransferParams**](-wia-wiatransferparams.md)結構的 *lMessage* 成員。

若要讀取所需的屬性，影像處理篩選器應該呼叫 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)介面上的 [**IWiaPropertyStorage：： GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) ，藉由呼叫 [IWiaImageFilter：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))從專案取得該介面。 然後，篩選準則可將此資料流程上的 [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) 實例具現化，以讀取專案屬性。 影像處理篩選不應直接呼叫 [IWiaPropertyStorage：： ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) ，因為此方法會呼叫驅動程式 `drvReadItemProperties` ，但 WIA 2.0 服務已在呼叫中鎖定驅動程式， `drvAcquireItemData` 因此此呼叫將會超時且失敗。

篩選感興趣的屬性，例如亮度和對比設定。 篩選通常也需要從 *pWiaItem2* 讀取影像格式以及預覽屬性（ [**WIA \_ DPS \_ preview**](-wia-wiaitempropscannerdevice.md)）。 這些屬性全都用於篩選進程。

WIA 2.0 元件一律會將未篩選的資料寫入影像處理篩選器中。 篩選的資料流程所執行的影像處理演算法可以篩選資料一次以上，而且不需要擔心產生與篩選資料一次相同的結果。

篩選準則必須注意 [**WIA \_ DPS \_ PREVIEW**](-wia-wiaitempropscannerdevice.md) 內容，尤其是在硬體中處理某些篩選相關的工作時。 例如，特定的驅動程式可能會根據應用程式將亮度設定為 WIA 2.0 專案的方式，變更掃描器硬體中的燈泡亮度。 在最後一次掃描期間 (當應用程式呼叫 [**IWiaTransfer：:D 下載 o)**](-wia-iwiatransfer-download.md)) 驅動程式通常會修改掃描器的實體燈泡。 在此情況下，影像處理篩選可能完全不需要執行任何亮度處理。 不過，在預覽掃描期間，驅動程式不應該修改燈泡的亮度，而應該只在影像處理篩選器中處理。 WIA 2.0 Preview 元件和影像處理篩選準則必須根據設定在專案中的屬性，傳回精確的影像。

影像處理篩選準則必須支援驅動程式支援的所有影像格式。

系統一律會將影像處理篩選器提供給選取區域的影像，並將其設定為我們取得影像的專案。 不過請注意，如果映射支援 [**WIA \_ ip \_ 旋轉**](-wia-wiaitempropscanneritem.md) 屬性，該影像可能已經由驅動程式旋轉。

當應用程式呼叫 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md)或 [**IWiaTransfer：:D 下載 o)**](-wia-iwiatransfer-download.md)時，影像處理篩選是透過 [**IWiaItem2：： GetExtension**](-wia-iwiaitem2-getextension.md)建立，但通常不是由應用程式所建立，而是由 WIA 2.0 元件建立。

**IWiaImageFilter** 介面（如同所有元件物件模型 (COM) 介面）會繼承 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面方法。



| IUnknown 方法                                        | Description                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | 傳回受支援介面的指標。 |
| [IUnknown：： AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | 遞增參考次數。               |
| [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | 遞減參考次數。               |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
