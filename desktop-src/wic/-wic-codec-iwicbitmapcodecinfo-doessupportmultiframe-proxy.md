---
description: DoesSupportMultiframe 方法的 Proxy 函式。
ms.assetid: ceee0090-ff23-4eb4-b0ea-de1d12bceef8
title: IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5e6e85d7e8454cf86aeac047f5269236a6091c108bd51b0e3be9828afe0766aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118034703"
---
# <a name="iwicbitmapcodecinfo_doessupportmultiframe_proxy-function"></a>IWICBitmapCodecInfo \_ DoesSupportMultiframe \_ Proxy 函式

[**DoesSupportMultiframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportmultiframe)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportMultiframe
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[ **IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***

這個 [**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) 物件的指標。

</dd> <dt>

*pfSupportMultiframe* \[擴展\]
</dt> <dd>

類型： **BOOL \***

如果編解碼器支援多框架影像，則為收到 **TRUE** 的指標;否則 **為 FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果此函式成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

## <a name="requirements"></a>需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsXP SP2，僅 Windows Vista \[ 桌面應用程式\]<br/>                                                                                              |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt> </dl> |



 

 




