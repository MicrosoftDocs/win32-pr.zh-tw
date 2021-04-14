---
description: Commit 方法的 Proxy 函數。
ms.assetid: 605801e5-00f8-4e4f-87d3-ad34d3568ee5
title: IWICBitmapFrameEncode_Commit_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0da0cb95a13148082d8263f622bb4089a7c9bd30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318259"
---
# <a name="iwicbitmapframeencode_commit_proxy-function"></a>IWICBitmapFrameEncode \_ Commit \_ Proxy 函式

[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit)方法的 Proxy 函數。

## <a name="syntax"></a>語法


```C++
HRESULT IWICBitmapFrameEncode_Commit_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _

這個 [_ *IWICBitmapFrameEncode* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)物件的指標。

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



 

 




