---
description: 取得 IWiaPreview：： GetNewPreview 方法快取的未篩選影像。
ms.assetid: 121b6866-cca1-4170-9bdf-225491f942f5
title: 'IWiaPreview：： UpdatePreview 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.UpdatePreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: b5f48462d926d96acebf4a74f0a843d82f9cd97190585b954565d5da649ff9f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549688"
---
# <a name="iwiapreviewupdatepreview-method"></a>IWiaPreview：： UpdatePreview 方法

取得 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md) 方法快取的未篩選影像。

## <a name="syntax"></a>語法


```C++
HRESULT UpdatePreview(
  [in] LONG      lOptions,
  [in] IWiaItem2 *pChildWiaItem
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lOptions* \[在\]
</dt> <dd>

類型： **LONG**

指定應用程式是否需要 WIA 2.0 Preview 元件，將快取影像的子領域或整個快取影像傳遞給影像處理篩選。

<dt>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**WiaPreviewReturnOriginalImage**


</dt> <dd>

將整個快取的影像傳遞至影像處理篩選。

</dd> </dl> </dd> <dt>

*pChildWiaItem* \[在\]
</dt> <dd>

類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

指定 [**IWiaItem2**](-wia-iwiaitem2.md)專案的指標，這是 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md)方法的 *PWiaItem2* 參數所指定之 **IWiaItem2** 專案的子系。 或者，如果應用程式需要整個平板的預覽，請指定 **IWiaPreview：： GetNewPreview** 方法的 *pWiaItem2* 參數指標。 當 *pChildWiaItem* 是 **IWiaPreview：： GetNewPreview** 之 *pWiaItem2* 參數的子系時，這個子專案通常是由分割篩選所建立。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

這個方法會透過影像處理篩選準則傳遞快取的未篩選影像，然後將篩選的資料寫入應用程式提供的資料流程。 WIA 2.0 Preview 元件會藉由呼叫影像處理篩選器的 [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) 方法來抓取此資料流程，然後呼叫應用程式回呼的 **GetNextStream** 執行。 在呼叫 **IWiaPreview：： UpdatePreview** 之前，應用程式必須先呼叫 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md) ，以從掃描器取得映射;否則，方法會傳回錯誤。

WIA 2.0 Preview 元件會儲存從驅動程式下載的未篩選映射。 將 WIA 2.0 專案傳遞至 **IWiaPreview：： UpdatePreview** ，可能只代表從驅動程式下載影像的小型區域。 如果發生這種情況，WIA 2.0 Preview 元件在將此區域傳遞給影像處理篩選器之前，實際上會從快取的影像中將它截斷，然後再將篩選的影像資料傳遞回應用程式。

若要讓應用程式將整個快取的影像傳遞至影像處理篩選 (接著將它傳遞給應用程式) ，它必須在呼叫 **IWiaPreview：： UpdatePreview** 時，將 *LOptions* 設定為 **WiaPreviewReturnOriginalImage** 。 將 *lOptions* 設定為 **WiaPreviewReturnOriginalImage** 時，應用程式必須確定傳遞至 **IWiaPreview：： UpdatePreview** 的專案的範圍設定 ([**wia \_ ip \_ 範圍**](-wia-wiaitempropscanneritem.md)和 **wia \_ ip \_ YEXTENT**) 符合完整快取的影像。 在此情況下，影像處理篩選不需要採取任何不同的動作;它只會根據 *pChildWiaItem* 的屬性來篩選影像 (一般來說，在此案例中， *pChildWiaItem* 是傳遞給 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md)) 的相同專案。 系統會忽略不同的子領域，並使用相同的設定篩選整個映射。 有幾個原因會導致應用程式這麼做。

1.  應用程式可能不支援針對分割篩選所偵測 (到的每個區域，個別變更設定 (例如 [**wia \_ ip \_ 亮度**](-wia-wiaitempropscanneritem.md) 和 **wia \_ ip \_ 對比**) ，也可能甚至不會想要使用分割篩選) 。 應用程式更容易以 **WiaPreviewReturnOriginalImage** 呼叫 **IWiaPreview：： UpdatePreview** ，讓它一律會從 WIA 2.0 Preview 元件收到完整的影像。
2.  WIA 2.0 Preview 元件不支援預覽影像的影像格式，在這種情況下，它無法執行動作來剪下所需的區域。 WIA 2.0 Preview 元件的影像格式支援僅限於有 Windows GDI+ 1.1 編碼器和解碼器的格式。 這些格式為點陣圖 (BMP)  (包含 BITMAPFILEHEADER) 的點陣圖、圖形交換格式 (GIF) 、JPEG、便攜網狀圖形 (PNG) ，以及標記的影像檔案格式 (TIFF) 。

請注意，如果應用程式將 **WiaPreviewReturnOriginalImage** 傳遞至 **IWiaPreview：： UPDATEPREVIEW**，則 WIA 2.0 Preview 元件可以支援任何影像或像素格式。

**IWiaPreview：： UpdatePreview** 會設定 [**WIA \_ DPS \_ PREVIEW**](-wia-wiaitempropscannerdevice.md) 屬性 (，並在傳回之前將它重設，除非它是在) 之前設定。 這可讓驅動程式 (和硬體) 以及映射處理篩選器，知道專案是預覽掃描。

應用程式必須確定 *pChildWiaItem* 具有相同的影像格式 ([**wia \_ IPA \_ 格式**](-wia-wiaitempropcommonitem.md)) 和解析度 ([**wia \_ ips \_ XRES**](-wia-wiaitempropscanneritem.md)和 **wia \_ Ip \_ YRES**) 在傳遞至 [**pWiaItem：： IWiaPreview**](-wia-iwiapreview-getnewpreview.md)時的 *GetNewPreview* 。 子專案的格式必須對應至 WIA 2.0 Preview 元件的快取影像格式， (WIA 2.0 Preview 元件不會執行任何影像轉換) 。

## <a name="examples"></a>範例

每次使用者變更時都應該呼叫 UpdateRegion，例如，所代表之子專案的亮度或對比 `dwRegionNumber` 。 此子專案先前是由分割篩選 ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)所建立。 寫入 [IStream](/windows/win32/api/objidl/nn-objidl-istream) 的影像會由傳輸回呼介面的 [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) 方法傳回。 在此範例中，會省略 GetSubRegionItem 的程式碼。

呼叫此函式之後，應用程式通常會重繪螢幕上的區域。


```C++
HRESULT
UpdateRegion(
   IN  DWORD dwRegionNumber)
{
   IWiaItem2 *pSubRegion = GetSubRegionItem(dwRegionNumber);

   return m_pWiaPreview->UpdatePreview(0,pSubRegion);
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
