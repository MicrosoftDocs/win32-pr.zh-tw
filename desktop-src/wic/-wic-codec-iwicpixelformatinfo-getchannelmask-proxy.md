---
description: GetChannelMask 方法的 Proxy 函式。
ms.assetid: c96e6078-4648-4333-8a25-bcb03a2cd50b
title: IWICPixelFormatInfo_GetChannelMask_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelMask_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0db2c14e89aba2b13cb95209b81f6d0da5d9d949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194783"
---
# <a name="iwicpixelformatinfo_getchannelmask_proxy-function"></a>IWICPixelFormatInfo \_ GetChannelMask \_ Proxy 函式

[**GetChannelMask**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICPixelFormatInfo_GetChannelMask_Proxy(
  _In_    IWICPixelFormatInfo *THIS_PTR,
  _In_    UINT                uiChannelIndex,
  _In_    UINT                cbMaskBuffer,
  _Inout_ BYTE                *pbMaskBuffer,
  _Out_   UINT                *pcbActual
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _

這個 [_ *IWICPixelFormatInfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)物件的指標。

</dd> <dt>

*uiChannelIndex* \[在\]
</dt> <dd>

類型： **UINT**

要取出之通道遮罩的索引。

</dd> <dt>

*cbMaskBuffer* \[在\]
</dt> <dd>

類型： **UINT**

*PbMaskBuffer* 緩衝區的大小。

</dd> <dt>

*pbMaskBuffer* \[in、out\]
</dt> <dd>

類型： **BYTE \** _

遮罩緩衝區的指標。

</dd> <dt>

_pcbActual * \[ out\]
</dt> <dd>

類型： **UINT \** _

取得通道遮罩所需的實際緩衝區大小。

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



 

 




