---
description: GetContainerFormat 方法的 IWICBitmapCodecInfo_GetContainerFormat_Proxy 函數 Proxy 函式。
ms.assetid: d8a2387a-fb75-4812-b046-51359071281d
title: IWICBitmapCodecInfo_GetContainerFormat_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 729b4e2fe0f21fd1e96082e53194fd49bbc39ae1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086366"
---
# <a name="iwicbitmapcodecinfo_getcontainerformat_proxy-function"></a>IWICBitmapCodecInfo \_ GetContainerFormat \_ Proxy 函式

[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICBitmapCodecInfo_GetContainerFormat_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ GUID                *pguidContainerFormat
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[ **IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***

這個 [**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) 物件的指標。

</dd> <dt>

*pguidContainerFormat* \[擴展\]
</dt> <dd>

類型： **GUID \***

接收容器 GUID 的指標。

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



 

 




