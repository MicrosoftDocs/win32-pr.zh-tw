---
title: IMsTscAx SendOnVirtualChannel 方法
description: 透過先前使用 CreateVirtualChannels 方法建立的虛擬通道，將資料傳送至遠端桌面工作階段主機 (RD 工作階段主機) 伺服器。
ms.assetid: 795ef508-bdf7-4897-84b1-931615262293
ms.tgt_platform: multiple
keywords:
- SendOnVirtualChannel 方法遠端桌面服務
- SendOnVirtualChannel 方法遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，SendOnVirtualChannel 方法
- SendOnVirtualChannel 方法遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，SendOnVirtualChannel 方法
- SendOnVirtualChannel 方法遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，SendOnVirtualChannel 方法
- SendOnVirtualChannel 方法遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，SendOnVirtualChannel 方法
- SendOnVirtualChannel 方法遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，SendOnVirtualChannel 方法
- SendOnVirtualChannel 方法遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，SendOnVirtualChannel 方法
- SendOnVirtualChannel 方法遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，SendOnVirtualChannel 方法
- SendOnVirtualChannel 方法遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，SendOnVirtualChannel 方法
- SendOnVirtualChannel 方法遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，SendOnVirtualChannel 方法
- SendOnVirtualChannel 方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，SendOnVirtualChannel 方法
topic_type:
- apiref
api_name:
- IMsTscAx.SendOnVirtualChannel
- IMsRdpClient.SendOnVirtualChannel
- IMsRdpClient2.SendOnVirtualChannel
- IMsRdpClient3.SendOnVirtualChannel
- IMsRdpClient4.SendOnVirtualChannel
- IMsRdpClient5.SendOnVirtualChannel
- IMsRdpClient6.SendOnVirtualChannel
- IMsRdpClient7.SendOnVirtualChannel
- IMsRdpClient8.SendOnVirtualChannel
- IMsRdpClient9.SendOnVirtualChannel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03c5b84ff9cb272d5560f3b6588301a05a3e9a003db1b28f841a77b2e0618b37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125298"
---
# <a name="imstscaxsendonvirtualchannel-method"></a>IMsTscAx：： SendOnVirtualChannel 方法

透過先前使用 [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) 方法建立的虛擬通道，將資料傳送至遠端桌面工作階段主機 (RD 工作階段主機) 伺服器。

## <a name="syntax"></a>語法


```C++
HRESULT SendOnVirtualChannel(
  [in] BSTR ChanName,
  [in] BSTR ChanData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ChanName* \[在\]
</dt> <dd>

呼叫 [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)時所指定的虛擬通道名稱。

</dd> <dt>

*ChanData* \[在\]
</dt> <dd>

要透過虛擬通道傳送的資料，以 **BSTR** 形式傳送。 這項資料不會限制為以 null 結束的字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

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

[**CreateVirtualChannels**](imstscax-createvirtualchannels.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





