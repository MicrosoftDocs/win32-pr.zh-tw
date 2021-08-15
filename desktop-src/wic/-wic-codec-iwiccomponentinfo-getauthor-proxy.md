---
description: GetAuthor 方法的 Proxy 函式。
ms.assetid: fb76009e-cc01-4dec-9403-04bf6b53db80
title: IWICComponentInfo_GetAuthor_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetAuthor_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c83d42f499c8f821f5b342f08749a2167aac9cc61334fe2fc2d9e9134b5e2b49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206669"
---
# <a name="iwiccomponentinfo_getauthor_proxy-function"></a>IWICComponentInfo \_ GetAuthor \_ Proxy 函式

[**GetAuthor**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getauthor)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICComponentInfo_GetAuthor_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchAuthor,
  _Inout_ WCHAR             *wzAuthor,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[ **IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\***

這個 [**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) 物件的指標。

</dd> <dt>

*cchAuthor* \[在\]
</dt> <dd>

類型： **UINT**

*WzAuthor* 緩衝區的大小。

</dd> <dt>

*wzAuthor* \[in、out\]
</dt> <dd>

類型： **WCHAR \***

接收元件作者名稱的指標。

傳回的字串是預設的地區設定，預設為1033。

</dd> <dt>

*pcchActual* \[擴展\]
</dt> <dd>

類型： **UINT \***

接收元件作者名稱實際長度的指標。

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



 

 




