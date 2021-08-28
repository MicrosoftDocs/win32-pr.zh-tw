---
title: IMsRdpDeviceCollection2 AddDeviceByInstanceId 方法
description: 將未列出的裝置新增至裝置集合。
ms.assetid: 7ef200c5-b99e-40c9-80e1-0758ddfa0902
ms.tgt_platform: multiple
keywords:
- AddDeviceByInstanceId 方法遠端桌面服務
- AddDeviceByInstanceId 方法遠端桌面服務，IMsRdpDeviceCollection2 介面
- IMsRdpDeviceCollection2 介面遠端桌面服務，AddDeviceByInstanceId 方法
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.AddDeviceByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df11fa2a58aca505661da1f7643f8d1d6ff2f502e6c10bf835aa67a6e2d0615d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870818"
---
# <a name="imsrdpdevicecollection2adddevicebyinstanceid-method"></a>IMsRdpDeviceCollection2：： AddDeviceByInstanceId 方法

將未列出的裝置新增至裝置集合。

## <a name="syntax"></a>語法


```C++
HRESULT AddDeviceByInstanceId(
  [in] RedirectDeviceType Type,
  [in] BSTR               InstanceId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*類型* \[在\]
</dt> <dd>

類型： **[ **RedirectDeviceType**](redirectdevicetype.md)**

[**RedirectDeviceType**](redirectdevicetype.md)列舉的值，這個值會指定要新增的裝置類型。

</dd> <dt>

*InstanceId* \[在\]
</dt> <dd>

類型： **BSTR**

要加入之裝置的實例識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RedirectDeviceType**](redirectdevicetype.md)
</dt> <dt>

[**IMsRdpDeviceCollection2**](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





