---
description: 取得可能隨附于 Windows 映像取得 (WIA) 2.0 設備磁碟機的延伸模組介面。
ms.assetid: 70f20f33-905c-4a88-8065-1cf876e98302
title: 'IWiaItem2：： GetExtension 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 4c9738afe60d79b73149c9dd7dda8c3bbd1017c3b41d023b47160b624bcd7c8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450410"
---
# <a name="iwiaitem2getextension-method"></a>IWiaItem2：： GetExtension 方法

取得可能隨附于 Windows 映像取得 (WIA) 2.0 設備磁碟機的延伸模組介面。

## <a name="syntax"></a>語法


```C++
HRESULT GetExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] VOID   **ppOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

目前未使用。 應該設定為零。

</dd> <dt>

*bstrName* \[在\]
</dt> <dd>

類型： **BSTR**

指定呼叫應用程式要求指標的延伸模組名稱。

<dt>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**SegmentationFilter**


</dt> <dd>

分割篩選延伸。 這是此參數目前唯一有效的值。

</dd> </dl> </dd> <dt>

*riidExtensionInterface* \[在\]
</dt> <dd>

類型： **REFIID**

指定延伸模組介面的識別碼。

</dd> <dt>

*ppOut* \[擴展\]
</dt> <dd>

類型： **VOID \* \***

接收擴充介面指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

應用程式會叫用這個方法，以建立擴充物件來執行其中一個 WIA 2.0 驅動程式擴充功能介面。 **IWiaItem2：： GetExtension** 會在 *riidExtensionInterface* 參數中儲存擴充物件的擴充功能介面位址。 然後，應用程式會使用介面指標來呼叫其方法。

應用程式必須在透過 *riidExtensionInterface* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。

## <a name="examples"></a>範例

CreateSegmentationFilter 會在傳入的 [**IWiaItem2**](-wia-iwiaitem2.md)介面上呼叫 **IWiaItem2：： GetExtension** ，以建立驅動程式分割篩選的實例 ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)) 。


```C++
HRESULT
CreateSegmentationFilter(
   IWiaItem2               *pWiaItem2,
   IWiaSegmentationFilter  **ppSegmentationFilter)
{
   HRESULT                 hr         = S_OK;
   IWiaSegmentationFilter *pSegFilter = NULL;
    
   if (!pWiaItem2 || !ppSegmentationFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_SEGMENTATION_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->GetExtension(0,
                                      bstrFilterString,
                                      IID_IWiaSegmentationFilter,
                                      (void**)&pSegFilter);
         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   if (SUCCEEDED(hr))
   {
     *ppSegmentationFilter = pSegFilter;
      pSegFilter = NULL;
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
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
