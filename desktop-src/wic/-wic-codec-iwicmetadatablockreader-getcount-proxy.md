---
description: GetCount 方法的 Proxy 函式。
ms.assetid: 441bbbaf-5a6a-4d1e-bb8d-f79af6aa2708
title: IWICMetadataBlockReader_GetCount_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataBlockReader_GetCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9b85229a96f0cc2a983455b104091c042371d5294db2ef1807e728faf29285df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812198"
---
# <a name="iwicmetadatablockreader_getcount_proxy-function"></a>IWICMetadataBlockReader \_ GetCount \_ Proxy 函式

[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICMetadataBlockReader_GetCount_Proxy(
  _In_  IWICMetadataBlockReader *THIS_PTR,
  _Out_ UINT                    *pcCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[ **IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)\***

這個 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) 物件的指標。

</dd> <dt>

*pcCount* \[擴展\]
</dt> <dd>

類型： **UINT \***

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



 

 




