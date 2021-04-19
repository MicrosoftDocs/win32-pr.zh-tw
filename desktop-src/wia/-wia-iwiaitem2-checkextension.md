---
description: 檢查指定的延伸模組是否可在電腦上使用，並可供 IWiaItem2：： GetExtension 方法使用。
ms.assetid: 672f6418-4ce3-4570-a412-fe639c9f5eb8
title: 'IWiaItem2：： CheckExtension 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CheckExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 65b0b5b3ace1634a20dfa63382d82099fef0686e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974137"
---
# <a name="iwiaitem2checkextension-method"></a>IWiaItem2：： CheckExtension 方法

檢查指定的延伸模組是否可在電腦上使用，並可供 [**IWiaItem2：： GetExtension**](-wia-iwiaitem2-getextension.md) 方法使用。

## <a name="syntax"></a>語法


```C++
HRESULT CheckExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] BOOL   *pbExtensionExists
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

指定擴充功能的名稱。

</dd> <dt>

*riidExtensionInterface* \[在\]
</dt> <dd>

類型： **REFIID**

目前未使用。

</dd> <dt>

*pbExtensionExists* \[擴展\]
</dt> <dd>

類型： **BOOL \** _

接收 _ * BOOL * * 的指標。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**假**


</dt> <dd>

無法使用指定的延伸模組。

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**真**


</dt> <dd>

指定的擴充功能可供使用。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

使用這個方法，應用程式可以在呼叫 [**IWiaItem2：： GetExtension**](-wia-iwiaitem2-getextension.md) 方法之前，檢查是否有可用的延伸模組。 此外，應用程式也可以檢查有哪些延伸模組可供使用，而不需要共同建立每個擴充功能，然後決定要使用哪一個。

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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 




