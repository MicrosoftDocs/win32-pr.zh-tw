---
description: GetSpecVersion 方法的 Proxy 函式。
ms.assetid: 363e55c2-d6e8-4ddc-a063-c5be08232a67
title: IWICComponentInfo_GetSpecVersion_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetSpecVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a29b57e84b7cf9ceee67ac4f64ac090e697366fbe0698a891c8fbcc87e3ff5b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206581"
---
# <a name="iwiccomponentinfo_getspecversion_proxy-function"></a>IWICComponentInfo \_ GetSpecVersion \_ Proxy 函式

[**GetSpecVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getspecversion)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICComponentInfo_GetSpecVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchSpecVersion,
  _Inout_ WCHAR             *wzSpecVersion,
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

*cchSpecVersion* \[在\]
</dt> <dd>

類型： **UINT**

*WzSpecVersion* 緩衝區的大小。

</dd> <dt>

*wzSpecVersion* \[in、out\]
</dt> <dd>

類型： **WCHAR \***

當此方法傳回時，會包含元件規格版本的文化特性 invarient 字串。 版本形式為 NN. nn. nn. nn. nn. nn. nn。

</dd> <dt>

*pcchActual* \[擴展\]
</dt> <dd>

類型： **UINT \***

接收元件規格版本實際長度的指標。

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



 

 




