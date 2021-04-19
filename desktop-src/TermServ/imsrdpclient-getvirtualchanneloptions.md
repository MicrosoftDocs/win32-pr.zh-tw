---
title: IMsRdpClient GetVirtualChannelOptions 方法
description: 抓取為虛擬通道設定的選項。
ms.assetid: d2ec9fb2-c0dc-49f1-a86b-d7abca13a322
ms.tgt_platform: multiple
keywords:
- GetVirtualChannelOptions 方法遠端桌面服務
- GetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，GetVirtualChannelOptions 方法
- GetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，GetVirtualChannelOptions 方法
- GetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，GetVirtualChannelOptions 方法
- GetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，GetVirtualChannelOptions 方法
- GetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，GetVirtualChannelOptions 方法
- GetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，GetVirtualChannelOptions 方法
- GetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，GetVirtualChannelOptions 方法
- GetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，GetVirtualChannelOptions 方法
- GetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，GetVirtualChannelOptions 方法
- GetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，GetVirtualChannelOptions 方法
topic_type:
- apiref
api_name:
- IMsRdpClient.GetVirtualChannelOptions
- IMsRdpClient2.GetVirtualChannelOptions
- IMsRdpClient3.GetVirtualChannelOptions
- IMsRdpClient4.GetVirtualChannelOptions
- IMsRdpClient5.GetVirtualChannelOptions
- IMsRdpClient6.GetVirtualChannelOptions
- IMsRdpClient7.GetVirtualChannelOptions
- IMsRdpClient8.GetVirtualChannelOptions
- IMsRdpClient9.GetVirtualChannelOptions
- IMsRdpClient10.GetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71548002ebc67dae8dc1a49e8144da3de608afb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106980292"
---
# <a name="imsrdpclientgetvirtualchanneloptions-method"></a>IMsRdpClient：： GetVirtualChannelOptions 方法

抓取為虛擬通道設定的選項。

## <a name="syntax"></a>語法


```C++
HRESULT GetVirtualChannelOptions(
  [in]  BSTR ChanName,
  [out] LONG *pChanOptions
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ChanName* \[在\]
</dt> <dd>

呼叫 [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) 方法時所指定的虛擬通道名稱。

</dd> <dt>

*pChanOptions* \[擴展\]
</dt> <dd>

為 *ChanName* 參數所指定的虛擬通道設定的選項。 如需可能選項的描述，請參閱 [**通道 \_ 定義**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient 定義為92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>        |



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

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**通道 \_ 定義**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[**CreateVirtualChannels**](imstscax-createvirtualchannels.md)
</dt> <dt>

[**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)
</dt> </dl>

 

 





