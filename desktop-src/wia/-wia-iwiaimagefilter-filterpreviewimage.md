---
description: 篩選預覽影像。
ms.assetid: 1710211a-a35c-4a51-b3bb-6f03f234f247
title: 'IWiaImageFilter：： FilterPreviewImage 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.FilterPreviewImage
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 96b1d8ce92a847dcd4ffcebca6b45df2b652ad74c1216fc60b8aac72bb6a12ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659718"
---
# <a name="iwiaimagefilterfilterpreviewimage-method"></a>IWiaImageFilter：： FilterPreviewImage 方法

篩選預覽影像。

## <a name="syntax"></a>語法


```C++
HRESULT FilterPreviewImage(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaChildItem2,
  [in] RECT      InputImageExtents,
  [in] IStream   *pInputStream
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

未使用。 設定為0。

</dd> <dt>

*pWiaChildItem2* \[在\]
</dt> <dd>

類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

處理的專案。

</dd> <dt>

*InputImageExtents* \[在\]
</dt> <dd>

類型： **RECT**

座標 (在預覽元件內部快取之影像的實體取得區域) 。

</dd> <dt>

*pInputStream* \[在\]
</dt> <dd>

類型： **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\***

已篩選之快取影像資料的 [IStream](/windows/win32/api/objidl/nn-objidl-istream) 介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

請勿直接從您的應用程式呼叫這個方法。

*pWiaChildItem2* 必須是傳遞至 [**IWiaImageFilter：： InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md)之 *pWiaItem2* 的子專案。

*InputImageExtents* 是必要的，因為影像處理篩選器會負責從透過 *pInputStream* 傳入的影像資料中，剪下 *pWiaChildItem2* 所代表的影像區域。

應用程式必須確定 *pWiaChildItem2* 具有相同的影像格式 (WIA \_ IPA \_ 格式) 、解析度 (WIA \_ ips \_ XRES 和 WIA \_ IP \_ YRES) 和位深度 (wia \_ IPA \_ 深度) ，因為 *pWiaItem2* 已傳遞至 [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
