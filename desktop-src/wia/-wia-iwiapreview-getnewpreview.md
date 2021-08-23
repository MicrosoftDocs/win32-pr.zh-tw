---
description: 在內部快取從驅動程式傳回之未篩選的映射。
ms.assetid: 09cb242d-d1d6-4130-8b49-0770940471d8
title: 'IWiaPreview：： GetNewPreview 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.GetNewPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2200452fe586a4755a4560f0f68094e5f107e9e7d69a823bafac4d33bc1c6ce8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965557"
---
# <a name="iwiapreviewgetnewpreview-method"></a>IWiaPreview：： GetNewPreview 方法

在內部快取從驅動程式傳回之未篩選的映射。

## <a name="syntax"></a>語法


```C++
HRESULT GetNewPreview(
  [in] IWiaItem2            *pWiaItem2,
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pWiaItem2* \[在\]
</dt> <dd>

類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

指定影像的 [**IWiaItem2**](-wia-iwiaitem2.md) 專案指標。

</dd> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

目前未使用。 應該設定為零。

</dd> <dt>

*pWiaTransferCallback* \[在\]
</dt> <dd>

類型： **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)\***

指定呼叫應用程式之 [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

應用程式必須先呼叫 **IWiaPreview：： GetNewPreview** ，然後再呼叫 [**IWiaPreview：:D etectregions**](-wia-iwiapreview-detectregions.md)。

**IWiaPreview：： GetNewPreview** 會設定 [**WIA \_ DPS \_ PREVIEW**](-wia-wiaitempropscannerdevice.md) 屬性 (，並在傳回之前將它重設，除非它是在) 之前設定。 這可讓驅動程式和硬體以及影像處理篩選器知道專案是預覽掃描。

就內部而言，Windows 影像取得 (WIA) 2.0 preview 元件會藉由在 *pWiaItem2* 上呼叫 [**GetExtension**](-wia-iwiaitem2-getextension.md)來建立驅動程式影像處理篩選的實例。 當應用程式呼叫 **IWiaPreview：： GetNewPreview** 時，WIA 2.0 preview 元件會執行此動作。 WIA 2.0 preview 元件也會初始化 **IWiaPreview：： GetNewPreview** 中的篩選準則。 在呼叫 [**IWiaPreview：： UpdatePreview**](-wia-iwiapreview-updatepreview.md)期間，WIA 2.0 preview 元件會使用相同的篩選實例。

在呼叫 WIA 2.0 preview 元件之前，應用程式應該呼叫 [**CheckExtension**](-wia-iwiaitem2-checkextension.md) ，以確定驅動程式隨附于影像處理篩選器。 它應該在它會傳遞至 **IWiaPreview：： GetNewPreview** 的專案上呼叫 **CheckExtension** 。 提供沒有影像處理篩選器的即時預覽是無用的。 如果應用程式在沒有影像處理篩選的情況下呼叫驅動程式的 **IWiaPreview：： GetNewPreview** ，則呼叫會失敗。

## <a name="examples"></a>範例

CheckImgFilter 會檢查驅動程式是否有影像處理篩選。 在呼叫預覽元件之前，應用程式應該確定驅動程式具有影像處理篩選。


```C++
HRESULT
CheckImgFilter(
   IN  IWiaItem2 *pWiaItem2,
   OUT BOOL      *pbHasImgFilter)
{
   HRESULT     hr = S_OK;

   if (!pWiaItem2 || !pbHasImgFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
     *pbHasImgFilter = FALSE;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_IMAGEPROC_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->CheckExtension(0,
                                        bstrFilterString,
                                        IID_IWiaSegmentationFilter,
                                        pbHasImgFilter);

         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   return hr;

}
```



DownloadPreviewImage 會藉由呼叫 preview 元件的 **IWiaPreview：： GetNewPreview** 方法，從掃描器下載影像資料。 如果應用程式使用者想要叫用分割篩選器，它就會呼叫 DetectSubregions，它會針對它所偵測到的每個區域，在 pWiaItem2 中建立子專案。 如需此範例中所使用的 DetectSubregions 方法，請參閱 [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) 。

在此範例中，應用程式使用者 `m_bUseSegmentationFilter` 可以按一下核取方塊來設定。 如果應用程式支援此程式，則應該先透過呼叫 [**CheckExtension**](-wia-iwiaitem2-checkextension.md)來檢查驅動程式是否有分割篩選。 請參閱 **IWiaPreview：： GetNewPreview** ，以取得顯示如何完成此操作的 CheckImgFilter 方法範例。


```C++
HRESULT
DownloadPreviewImage(
   IN IWiaItem2 *pWiaFlatbedItem2)
{
   HRESULT hr              = S_OK;
   BOOL    bHasImgFilter   = FALSE;

   IWiaTransferCallback *pAppWiaTransferCallback = NULL;

   hr = CheckImgFilter(pWiaFlatbedItem2, &bHasImgFilter)

   if (SUCCEEDED(hr))
   {
      if (bHasImgFilter)
      {
         IWiaPreview *pWiaPreview = NULL;

         // In this example, the AppWiaTransferCallback class implements 
         // the IWiaTransferCallback interface.  
         // The constructor of AppWiaTransferCallback sets the reference count to 1.
         pAppWiaTransferCallback = new AppWiaTransferCallback();

         hr = pAppWiaTransferCallback ? S_OK : E_OUTOFMEMORY;

         if (SUCCEEDED(hr))
         {
            // Acquire image from scanner
            hr = m_pWiaPreview->GetNewPreview(pWiaFlatbedItem2,
                                              0,
                                              pAppWiaTransferCallback);    
         }

         //
         // Check the application UI for whether the user wants
         // to use the segmentation filter indicated by the value 
         // of m_bUseSegmentationFilter.
         //
         // m_FlatbedPreviewStream is the stream that
         // AppWiaTransferCallback::GetNextStream returned for the
         // flatbed item.
         // This stream is where the image data is stored after
         // the successful return of GetNewPreview.
         // The stream is passed into the segmentation filter
         // for region detection.
         if (SUCCEEDED(hr) && m_bUseSegmentationFilter)
         {
            DetectSubregions(m_FlatbedPreviewStream, pWiaFlatbedItem2);
         }

         if (pAppWiaTransferCallback)
         {
            // If the call to GetNewPreview was successful, the
            // preview component calls AddRef on the callback so
            // this call doesn't delete the object.

            pAppWiaTransferCallback->Release();
         }

      }
      else
      {
         // Do not create an instance of preview component if the driver does
         // not come with an image processing filter.
         // You can use segmentation filter, however, if the driver
         // comes with one (omitted here).
      }
   }

   return hr;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 




