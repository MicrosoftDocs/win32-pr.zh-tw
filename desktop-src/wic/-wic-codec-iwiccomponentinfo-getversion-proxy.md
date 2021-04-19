---
description: GetVersion 方法的 Proxy 函數。
ms.assetid: b064b065-bc02-4943-b208-ce5e40c12aa2
title: IWICComponentInfo_GetVersion_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: bad3677068802861bce9c0c7d0c1b03e5d06d0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980087"
---
# <a name="iwiccomponentinfo_getversion_proxy-function"></a>IWICComponentInfo \_ GetVersion \_ Proxy 函式

[**GetVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getversion)方法的 Proxy 函數。

## <a name="syntax"></a>語法


```C++
HRESULT IWICComponentInfo_GetVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchVersion,
  _Inout_ WCHAR             *wzVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _

這個 [_ *IWICComponentInfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)物件的指標。

</dd> <dt>

*cchVersion* \[在\]
</dt> <dd>

類型： **UINT**

*WzVersion* 緩衝區的大小。

</dd> <dt>

*wzVersion* \[in、out\]
</dt> <dd>

類型： **WCHAR \** _

接收元件版本之文化特性不變字串的指標。

</dd> <dt>

_pcchActual * \[ out\]
</dt> <dd>

類型： **UINT \** _

接收元件版本實際長度的指標。

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



 

 




