---
description: InitializeFromMemory 方法的 IWICColorCoNtext_InitializeFromMemory_Proxy 函數 Proxy 函式。
ms.assetid: d98fe40c-c3f1-4c46-a558-1910e3dee51b
title: IWICColorCoNtext_InitializeFromMemory_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorContext_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e662e4a88858d413636289e6418e38fb1a1fe0bb864620d029cc8975bde7278f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711469"
---
# <a name="iwiccolorcontext_initializefrommemory_proxy-function"></a>IWICColorCoNtext \_ InitializeFromMemory \_ Proxy 函式

[**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICColorContext_InitializeFromMemory_Proxy(
  _In_       IWICColorContext *THIS_PTR,
  _In_ const BYTE             *pbBuffer,
  _In_       UINT             cbBufferSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[ **IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

</dd> <dt>

*pbBuffer* \[在\]
</dt> <dd>

類型： **CONST BYTE \***

用來初始化 [**IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)的緩衝區。

</dd> <dt>

*cbBufferSize* \[在\]
</dt> <dd>

類型： **UINT**

*PbBuffer* 緩衝區的大小。

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



 

 




