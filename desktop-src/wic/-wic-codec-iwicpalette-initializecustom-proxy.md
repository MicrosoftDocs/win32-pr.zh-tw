---
description: InitializeCustom 方法的 Proxy 函式。
ms.assetid: fe742b12-5338-41b0-b90b-aec852a26518
title: IWICPalette_InitializeCustom_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeCustom_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3b64daf458a6b916f0f9e2ba23e135d6c7328a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975880"
---
# <a name="iwicpalette_initializecustom_proxy-function"></a>IWICPalette \_ InitializeCustom \_ Proxy 函式

[**InitializeCustom**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializecustom)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICPalette_InitializeCustom_Proxy(
  _In_ IWICPalette *THIS_PTR,
  _In_ WICColor    *pColors,
  _In_ UINT        colorCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _

這個 [_ *IWICPalette* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)物件的指標。

</dd> <dt>

*pColors* \[在\]
</dt> <dd>

類型： **WICColor \** _

色彩陣列的指標。

</dd> <dt>

_colorCount * \[ in\]
</dt> <dd>

類型： **UINT**

*PColors* 中的色彩數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果此函式成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

## <a name="requirements"></a>需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]<br/>                                                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt> </dl> |



 

 




