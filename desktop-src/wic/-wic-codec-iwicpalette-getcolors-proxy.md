---
description: GetColors 方法的 Proxy 函式。
ms.assetid: 31590de3-f35c-4253-9a80-2f59c795bf3f
title: IWICPalette_GetColors_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColors_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e39e8825b78175fabb5a37e331236e7bf0d9ed73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193715"
---
# <a name="iwicpalette_getcolors_proxy-function"></a>IWICPalette \_ GetColors \_ Proxy 函式

[**GetColors**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolors)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICPalette_GetColors_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _In_  UINT        colorCount,
  _Out_ WICColor    *pColors,
  _Out_ UINT        *pcActualColors
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _

這個 [_ *IWICPalette* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)物件的指標。

</dd> <dt>

*colorCount* \[在\]
</dt> <dd>

類型： **UINT**

*PColors* 陣列的大小。

</dd> <dt>

*pColors* \[擴展\]
</dt> <dd>

類型： **WICColor \** _

接收調色板色彩的指標。

</dd> <dt>

_pcActualColors * \[ out\]
</dt> <dd>

類型： **UINT \** _

取得調色板色彩所需的實際大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： _ *HRESULT**

如果此函式成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

## <a name="requirements"></a>需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]<br/>                                                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt> </dl> |



 

 




