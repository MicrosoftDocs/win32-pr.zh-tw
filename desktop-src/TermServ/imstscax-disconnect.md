---
title: IMsTscAx 中斷連線方法
description: 中斷使用中連接。
ms.assetid: 9fcffd45-b293-4650-be8f-1b0d01d592a2
ms.tgt_platform: multiple
keywords:
- 中斷連接方法遠端桌面服務
- 中斷連接方法遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，中斷連線方法
- 中斷連接方法遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，中斷連線方法
- 中斷連接方法遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，中斷連線方法
- 中斷連接方法遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，中斷連線方法
- 中斷連接方法遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，中斷連線方法
- 中斷連接方法遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，中斷連線方法
- 中斷連接方法遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，中斷連線方法
- 中斷連接方法遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，中斷連線方法
- 中斷連接方法遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，中斷連線方法
- 中斷連接方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，中斷連線方法
topic_type:
- apiref
api_name:
- IMsTscAx.Disconnect
- IMsRdpClient.Disconnect
- IMsRdpClient2.Disconnect
- IMsRdpClient3.Disconnect
- IMsRdpClient4.Disconnect
- IMsRdpClient5.Disconnect
- IMsRdpClient6.Disconnect
- IMsRdpClient7.Disconnect
- IMsRdpClient8.Disconnect
- IMsRdpClient9.Disconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4f1545a8244209c0b4fa8267fcc8ce2a41e090
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508843"
---
# <a name="imstscaxdisconnect-method"></a>IMsTscAx：:D isconnect 方法

中斷使用中連接。

## <a name="syntax"></a>語法


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

如果在控制項未連接時呼叫此方法，則此方法會傳回錯誤值。

您也可以關閉主視窗，將控制項中斷連接。 例如，如果控制項是裝載在網頁中，就不需要在離開頁面之前呼叫這個方法。控制項的關閉會觸發中斷連接。

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

[**連接**](imstscax-connect.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





