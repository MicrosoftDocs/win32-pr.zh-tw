---
description: IEnumString：： Reset 的 Windows 影像處理元件 (WIC) proxy 函數。
ms.assetid: 084a3de0-c6de-4ce2-ba78-5d1bacb56cb0
title: IEnumString_Reset_WIC_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumString_Reset_WIC_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 64057e0f49b105232f980ac3d73014156e2da732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989907"
---
# <a name="ienumstring_reset_wic_proxy-function"></a>IEnumString \_ Reset \_ WIC \_ Proxy 函式

IEnumString：： Reset 的 Windows 影像處理元件 (WIC) proxy 函數。

## <a name="syntax"></a>語法


```C++
HRESULT IEnumString_Reset_WIC_Proxy(
  _In_  IEnumString *THIS_PTR,
  _In_  ULONG       celt,
  _Out_ LPOLESTR    *rgelt,
  _Out_ ULONG       *pceltFetched
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **IEnumString \** _

PARAMDESC

</dd> <dt>

_celt * \[ in\]
</dt> <dd>

類型： **ULONG**

</dd> <dt>

*rgelt* \[擴展\]
</dt> <dd>

類型： **LPOLESTR \** _

</dd> <dt>

_pceltFetched * \[ out\]
</dt> <dd>

類型： **ULONG \** _

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



 

 




