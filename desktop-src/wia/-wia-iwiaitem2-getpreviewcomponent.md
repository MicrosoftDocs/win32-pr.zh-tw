---
description: 取得 Windows 的影像取得 (WIA) 2.0 預覽元件。
ms.assetid: 0b773c4c-f080-41fa-8902-4243a80fc67c
title: 'IWiaItem2：： GetPreviewComponent 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetPreviewComponent
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3ac3705b4be60ce53fee411df1142fb64bbd1c393864b644e260829080be8f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450428"
---
# <a name="iwiaitem2getpreviewcomponent-method"></a>IWiaItem2：： GetPreviewComponent 方法

取得 Windows 的影像取得 (WIA) 2.0 預覽元件。

## <a name="syntax"></a>語法


```C++
HRESULT GetPreviewComponent(
  [in]  LONG        lFlags,
  [out] IWiaPreview **ppWiaPreview
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

未使用。 設定為0。

</dd> <dt>

*ppWiaPreview* \[擴展\]
</dt> <dd>

類型： **[ **IWiaPreview**](-wia-iwiapreview.md)\*\***

傳回預覽元件之 [**IWiaPreview**](-wia-iwiapreview.md) 介面指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

使用此函式可針對 WIA 2.0 硬體裝置之物件樹狀結構中的任何 [**IWiaItem2**](-wia-iwiaitem2.md) 物件，將指標傳回至 wia 2.0 preview 元件的位址。

應用程式必須在透過 *ppWiaPreview* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWiaItem2**](-wia-iwiaitem2.md)
</dt> <dt>

[**IWiaPreview**](-wia-iwiapreview.md)
</dt> </dl>

 

 
