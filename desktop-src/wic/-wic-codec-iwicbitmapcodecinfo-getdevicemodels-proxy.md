---
description: GetDeviceModels 方法的 Proxy 函式。
ms.assetid: de8f91f7-fef7-48bc-94fc-34c43175248b
title: IWICBitmapCodecInfo_GetDeviceModels_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetDeviceModels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b8fa6d6df6984569aa3fe49fc734f7699aa504d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972622"
---
# <a name="iwicbitmapcodecinfo_getdevicemodels_proxy-function"></a>IWICBitmapCodecInfo \_ GetDeviceModels \_ Proxy 函式

[**GetDeviceModels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemodels)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICBitmapCodecInfo_GetDeviceModels_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchDeviceModels,
  _Inout_ WCHAR               *wzDeviceModels,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _

這個 [_ *IWICBitmapCodecInfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)物件的指標。

</dd> <dt>

*cchDeviceModels* \[在\]
</dt> <dd>

類型： **UINT**

裝置型號緩衝區的大小。

</dd> <dt>

*wzDeviceModels* \[in、out\]
</dt> <dd>

類型： **WCHAR \** _

指標，接收與編解碼器相關聯的裝置型號名稱清單（以逗號分隔）。

</dd> <dt>

_pcchActual * \[ in、out\]
</dt> <dd>

類型： **UINT \** _

取得所有裝置模型名稱所需的實際緩衝區大小。

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



 

 




