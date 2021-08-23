---
title: IMsTscAx 連線方法
description: 使用目前在控制項上設定的屬性起始連接。
ms.assetid: 9bcbdc13-6c66-4737-82a4-98329f173743
ms.tgt_platform: multiple
keywords:
- 連線方法遠端桌面服務
- 連線方法遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，連線方法
- 連線方法遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，連線方法
- 連線方法遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，連線方法
- 連線方法遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，連線方法
- 連線方法遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，連線方法
- 連線方法遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，連線方法
- 連線方法遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，連線方法
- 連線方法遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，連線方法
- 連線方法遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，連線方法
- 連線方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，連線方法
topic_type:
- apiref
api_name:
- IMsTscAx.Connect
- IMsRdpClient.Connect
- IMsRdpClient2.Connect
- IMsRdpClient3.Connect
- IMsRdpClient4.Connect
- IMsRdpClient5.Connect
- IMsRdpClient6.Connect
- IMsRdpClient7.Connect
- IMsRdpClient8.Connect
- IMsRdpClient9.Connect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4372b19c9dba51714c6927d5e54468e143033689bfd9c74db78bbff8812e45ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513108"
---
# <a name="imstscaxconnect-method"></a>IMsTscAx：：連線方法

使用目前在控制項上設定的屬性起始連接。

## <a name="syntax"></a>語法


```C++
HRESULT Connect();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

唯一必要的屬性是伺服器名稱。 請參閱 [**伺服器**](imstscax-server.md) 屬性。

控制項會以非同步方式連接，因此從連線呼叫傳回時，只會指出已成功初始化連接，而不是已完成。 您應該回應 [**IMsTscAxEvents**](imstscaxevents-interface.md) 介面上的事件，以判斷控制項何時成功連接 (或已中斷連線。 ) 

如果控制項已經連接或處於連接狀態，則這個方法會傳回 **E \_ FAIL** 。

呼叫 **連線** 之後，就無法再設定大部分的控制項屬性，直到控制項回到中斷連接狀態為止。

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

[**中斷連線**](imstscax-disconnect.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





