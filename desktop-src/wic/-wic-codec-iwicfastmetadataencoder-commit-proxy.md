---
description: Commit 方法的 IWICFastMetadataEncoder_Commit_Proxy 函數 Proxy 函式。
ms.assetid: 5b3b90ad-9d67-4fbd-b01e-c7478df8dd45
title: IWICFastMetadataEncoder_Commit_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFastMetadataEncoder_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 69f94853761affe09472a18ca27585a74f398846dd06ef54abb88fe3c9b7ce71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117668401"
---
# <a name="iwicfastmetadataencoder_commit_proxy-function"></a>IWICFastMetadataEncoder \_ Commit \_ Proxy 函式

[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-commit)方法的 Proxy 函數。

## <a name="syntax"></a>語法


```C++
HRESULT IWICFastMetadataEncoder_Commit_Proxy(
  _In_ IWICFastMetadataEncoder *THIS_PTR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[ **IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\***

這個 [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) 物件的指標。

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



 

 




