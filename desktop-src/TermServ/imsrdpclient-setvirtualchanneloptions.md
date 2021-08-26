---
title: IMsRdpClient SetVirtualChannelOptions 方法
description: 設定遠端桌面 ActiveX 控制項的虛擬通道選項。
ms.assetid: c74c3917-5766-4d5b-8458-b051eb91cb28
ms.tgt_platform: multiple
keywords:
- SetVirtualChannelOptions 方法遠端桌面服務
- SetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，SetVirtualChannelOptions 方法
- SetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，SetVirtualChannelOptions 方法
- SetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，SetVirtualChannelOptions 方法
- SetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，SetVirtualChannelOptions 方法
- SetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，SetVirtualChannelOptions 方法
- SetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，SetVirtualChannelOptions 方法
- SetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，SetVirtualChannelOptions 方法
- SetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，SetVirtualChannelOptions 方法
- SetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，SetVirtualChannelOptions 方法
- SetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，SetVirtualChannelOptions 方法
topic_type:
- apiref
api_name:
- IMsRdpClient.SetVirtualChannelOptions
- IMsRdpClient2.SetVirtualChannelOptions
- IMsRdpClient3.SetVirtualChannelOptions
- IMsRdpClient4.SetVirtualChannelOptions
- IMsRdpClient5.SetVirtualChannelOptions
- IMsRdpClient6.SetVirtualChannelOptions
- IMsRdpClient7.SetVirtualChannelOptions
- IMsRdpClient8.SetVirtualChannelOptions
- IMsRdpClient9.SetVirtualChannelOptions
- IMsRdpClient10.SetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 804d4bde2fec9cb6273cc78f79d733f61a08772746439aa1cbb6e7b2d3c29716
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871579"
---
# <a name="imsrdpclientsetvirtualchanneloptions-method"></a>IMsRdpClient：： SetVirtualChannelOptions 方法

設定遠端桌面 ActiveX 控制項的虛擬通道選項。

請在呼叫 [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)方法之後，但在使用 [**連線**](imstscax-connect.md)方法建立連接之前呼叫這個方法。 這個方法會在使用 **CreateVirtualChannels** 建立的虛擬通道上設定其他選項。

## <a name="syntax"></a>語法


```C++
HRESULT SetVirtualChannelOptions(
  [in] BSTR ChanName,
  [in] LONG chanOptions
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ChanName* \[在\]
</dt> <dd>

呼叫 [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) 方法時所指定的虛擬通道名稱。

</dd> <dt>

*chanOptions* \[在\]
</dt> <dd>

要為 *ChanName* 參數指定的虛擬通道設定的選項。 如需可能選項的描述，請參閱 [**通道 \_ 定義**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)。 如需詳細資訊，請參閱接下來的＜備註＞一節。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

使用這個方法的範例，是藉由設定 **通道 \_ 選項 \_ 遠端 \_ 控制 \_ 持續** 旗標，將通道宣告為遠端控制持續性。 這表示當遠端控制連接到用戶端的會話或中斷連線時，就不會關閉通道。 如需詳細資訊，請參閱 [遠端控制持續性虛擬通道](remote-control-persistent-virtual-channels.md)。

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

[**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)
</dt> </dl>

 

 





