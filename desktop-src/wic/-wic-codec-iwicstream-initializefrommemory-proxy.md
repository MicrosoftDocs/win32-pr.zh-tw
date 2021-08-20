---
description: InitializeFromMemory 方法的 IWICStream_InitializeFromMemory_Proxy 函數 Proxy 函式。
ms.assetid: 737526ac-fe79-4d53-83c5-33102f5ac67b
title: IWICStream_InitializeFromMemory_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICStream_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1cc3d18c0b649fd18946ea1e0fb0fe6ecc421d9067a98766e308c38a2b4890af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118033422"
---
# <a name="iwicstream_initializefrommemory_proxy-function"></a>IWICStream \_ InitializeFromMemory \_ Proxy 函式

[**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICStream_InitializeFromMemory_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ BYTE       *pbBuffer,
  _In_ DWORD      cbBufferSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[ **IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\***

這個 [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) 物件的指標。

</dd> <dt>

*pbBuffer* \[在\]
</dt> <dd>

類型：**位元組 \***

用來初始化資料流程的緩衝區指標。

</dd> <dt>

*cbBufferSize* \[在\]
</dt> <dd>

類型： **DWORD**

緩衝區的大小。

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



 

 




