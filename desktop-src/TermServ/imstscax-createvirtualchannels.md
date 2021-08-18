---
title: IMsTscAx CreateVirtualChannels 方法
description: 針對每個指定的虛擬通道名稱建立用戶端虛擬通道物件。
ms.assetid: 3afd2f1c-abd5-4f85-93fb-6d1173f09b07
ms.tgt_platform: multiple
keywords:
- CreateVirtualChannels 方法遠端桌面服務
- CreateVirtualChannels 方法遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，CreateVirtualChannels 方法
- CreateVirtualChannels 方法遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，CreateVirtualChannels 方法
- CreateVirtualChannels 方法遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，CreateVirtualChannels 方法
- CreateVirtualChannels 方法遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，CreateVirtualChannels 方法
- CreateVirtualChannels 方法遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，CreateVirtualChannels 方法
- CreateVirtualChannels 方法遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，CreateVirtualChannels 方法
- CreateVirtualChannels 方法遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，CreateVirtualChannels 方法
- CreateVirtualChannels 方法遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，CreateVirtualChannels 方法
- CreateVirtualChannels 方法遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，CreateVirtualChannels 方法
- CreateVirtualChannels 方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，CreateVirtualChannels 方法
topic_type:
- apiref
api_name:
- IMsTscAx.CreateVirtualChannels
- IMsRdpClient.CreateVirtualChannels
- IMsRdpClient2.CreateVirtualChannels
- IMsRdpClient3.CreateVirtualChannels
- IMsRdpClient4.CreateVirtualChannels
- IMsRdpClient5.CreateVirtualChannels
- IMsRdpClient6.CreateVirtualChannels
- IMsRdpClient7.CreateVirtualChannels
- IMsRdpClient8.CreateVirtualChannels
- IMsRdpClient9.CreateVirtualChannels
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d3ef4e7c8471c655d4ecfaf54a1c4b0f35b2362c67c334bd94e57da8e99d390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138481"
---
# <a name="imstscaxcreatevirtualchannels-method"></a>IMsTscAx：： CreateVirtualChannels 方法

針對每個指定的虛擬通道名稱建立用戶端虛擬通道物件。

## <a name="syntax"></a>語法


```C++
HRESULT CreateVirtualChannels(
  [in] BSTR newVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*newVal* \[在\]
</dt> <dd>

有效虛擬通道名稱的逗號分隔清單。 這份清單中每個名稱的長度最少可以是一個，最多七個字母字元。 整個字串的長度最少為1，最多可為300個字母字元。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **S \_ OK** 。 如果傳遞的參數不符合指定的準則，則會傳回 **E \_ INVALIDARG** 。

## <a name="remarks"></a>備註

呼叫這個方法之前，請先呼叫這個方法，然後再呼叫 [**連線**](imstscax-connect.md)方法。

如需虛擬通道命名限制的相關資訊，請參閱 [虛擬通道用戶端註冊](virtual-channel-client-registration.md) 。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





