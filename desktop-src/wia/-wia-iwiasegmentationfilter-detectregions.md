---
description: 決定影像的子領域，這些子領域會在平板玻璃上配置，讓每個子領域都可以取得個別的影像專案。
ms.assetid: 899d61f0-2dd8-4a68-827e-89e85ebb5143
title: 'IWiaSegmentationFilter：:D etectRegions 方法 (Wia. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 94fe2f5076e9ff7cc0de0f7c916f6edacf2d03fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113300"
---
# <a name="iwiasegmentationfilterdetectregions-method"></a>IWiaSegmentationFilter：:D etectRegions 方法

決定影像的子領域，這些子領域會在平板玻璃上配置，讓每個子領域都可以取得個別的影像專案。

## <a name="syntax"></a>語法


```C++
HRESULT DetectRegions(
  [in] LONG      lFlags,
  [in] IStream   *pInputStream,
  [in] IWiaItem2 *pWiaItem2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

目前未使用。 應該設定為零。

</dd> <dt>

*pInputStream* \[在\]
</dt> <dd>

類型： **[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _

指定 [IStream](/windows/win32/api/objidl/nn-objidl-istream) 預覽影像的指標。

</dd> <dt>

_pWiaItem2 * \[ in\]
</dt> <dd>

類型： **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

指定取得 *pInputStream* 之 [_ *IWiaItem2* *](-wia-iwiaitem2.md)專案的指標。 分割篩選會建立此專案的子專案。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

這個方法會判斷 pInputStream 所代表之影像的子領域。 針對每個子領域偵測到的子領域，它會針對 *pWiaItem2* 參數中指定的 [**IWiaItem2**](-wia-iwiaitem2.md)專案建立子專案。 針對每個子專案，分割篩選必須使用下列 [**掃描器 WIA 專案屬性常數**](-wia-wiaitempropscanneritem.md)，設定要掃描之區域周框矩形的值。

-   [**WIA \_ IP \_ XPOS**](-wia-wiaitempropscanneritem.md)
-   [**WIA \_ IP \_ YPOS**](-wia-wiaitempropscanneritem.md)
-   [**WIA \_ IP \_ 範圍**](-wia-wiaitempropscanneritem.md)
-   [**WIA \_ IP \_ YEXTENT**](-wia-wiaitempropscanneritem.md)

如果驅動程式支援反扭曲，則更高階的篩選器可能也需要其他 [**掃描器 WIA 專案屬性常數**](-wia-wiaitempropscanneritem.md) ，例如 **WIA \_ ip \_ 反扭曲 \_ X** 和 **wia \_ ip \_ \_**。

如果應用程式呼叫 **IWiaSegmentationFilter：:D etectregions** 超過一次，應用程式必須先刪除最後一次呼叫 **IWiaSegmentationFilter：:D etectregions** 所建立的子專案。

如果應用程式將任何屬性變更為 *pWiaItem2*，請在將影像取得至 *pInputStream* ，以及其對 **IWiaSegmentationFilter：:D etectregions** 的呼叫之間，原始屬性 (亦即，當取得串流時，專案具有的屬性) 必須還原。 這可以藉由 [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) 和 [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream)來完成。

如果應用程式的呼叫將相同的資料流程傳遞給分割篩選一次以上，則必須重設 [IStream](/windows/win32/api/objidl/nn-objidl-istream) 。 應用程式也必須在初始下載之後和呼叫 IWiaSegmentationFilter 之前重設資料流程 **：:D etectregions**。

## <a name="examples"></a>範例

分割會在資料流程上執列區域偵測， (`pImageStream`) 傳遞至 DetectSubregions。 請參閱此範例中使用的 CreateSegmentationFilter 方法 [**GetExtension**](-wia-iwiaitem2-getextension.md) 。


```C++
HRESULT
DetectSubregions(
   IN IStream   *pImageStream,
   IN IWiaItem2 *pWiaItem2)
{
   HRESULT                 hr                  = S_OK;
   IWiaSegmentationFilter* pSegmentationFilter = NULL;

   if (!pWiaItem2 || !pImageStream)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      hr = CreateSegmentationFilter(pWiaItem2, &pSegmentationFilter);
   }

   if (SUCCEEDED(hr))
   {
      hr = pSegmentationFilter->DetectRegions(0,pImageStream, pWiaItem2); 
   }

   if (pSegmentationFilter)
   {
      pSegmentationFilter->Release();
      pSegmentationFilter = NULL;
   }

   return hr;
}
```



DownloadPreviewImage 會藉由呼叫預覽元件的 [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) 方法，從掃描器下載影像資料。 如果應用程式使用者想要叫用分割篩選器，它就會呼叫 DetectSubregions，它會針對它所偵測到的每個區域，在 pWiaItem2 中建立子專案。 如需此範例中使用的 DetectSubregions 方法，請參閱 **IWiaSegmentationFilter：:D etectregions** 。

在此範例中，應用程式使用者 `m_bUseSegmentationFilter` 可以按一下核取方塊來設定。 如果應用程式支援此程式，則應該先透過呼叫 [**CheckExtension**](-wia-iwiaitem2-checkextension.md)來檢查驅動程式是否有分割篩選。 如需說明如何完成此操作的 CheckImgFilter 方法範例，請參閱 [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) 。


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
         // The constructor of AppWiaTransferCallback sets the reference count 
         // to 1.
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
         // Do not create an instance of preview component if the driver 
         // does not come with an image-processing filter.
         // You can use a segmentation filter, however, if the driver
         // comes with one (omitted here).
      }
   }

   return hr;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
