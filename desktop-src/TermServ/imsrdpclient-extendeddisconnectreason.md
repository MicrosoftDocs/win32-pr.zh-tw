---
title: IMsRdpClient ExtendedDisconnectReason 屬性
description: 包含控制項中斷連接原因的延伸資訊。
ms.assetid: 5729992f-6695-44c0-8cf0-0d6b4cbddb62
ms.tgt_platform: multiple
keywords:
- ExtendedDisconnectReason 屬性遠端桌面服務
- ExtendedDisconnectReason 屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，ExtendedDisconnectReason 屬性
- ExtendedDisconnectReason 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，ExtendedDisconnectReason 屬性
- ExtendedDisconnectReason 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，ExtendedDisconnectReason 屬性
- ExtendedDisconnectReason 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，ExtendedDisconnectReason 屬性
- ExtendedDisconnectReason 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，ExtendedDisconnectReason 屬性
- ExtendedDisconnectReason 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，ExtendedDisconnectReason 屬性
- ExtendedDisconnectReason 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，ExtendedDisconnectReason 屬性
- ExtendedDisconnectReason 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，ExtendedDisconnectReason 屬性
- ExtendedDisconnectReason 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，ExtendedDisconnectReason 屬性
- ExtendedDisconnectReason 屬性遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，ExtendedDisconnectReason 屬性
topic_type:
- apiref
api_name:
- IMsRdpClient.ExtendedDisconnectReason
- IMsRdpClient.get_ExtendedDisconnectReason
- IMsRdpClient2.ExtendedDisconnectReason
- IMsRdpClient2.get_ExtendedDisconnectReason
- IMsRdpClient3.ExtendedDisconnectReason
- IMsRdpClient3.get_ExtendedDisconnectReason
- IMsRdpClient4.ExtendedDisconnectReason
- IMsRdpClient4.get_ExtendedDisconnectReason
- IMsRdpClient5.ExtendedDisconnectReason
- IMsRdpClient5.get_ExtendedDisconnectReason
- IMsRdpClient6.ExtendedDisconnectReason
- IMsRdpClient6.get_ExtendedDisconnectReason
- IMsRdpClient7.ExtendedDisconnectReason
- IMsRdpClient7.get_ExtendedDisconnectReason
- IMsRdpClient8.ExtendedDisconnectReason
- IMsRdpClient8.get_ExtendedDisconnectReason
- IMsRdpClient9.ExtendedDisconnectReason
- IMsRdpClient9.get_ExtendedDisconnectReason
- IMsRdpClient10.ExtendedDisconnectReason
- IMsRdpClient10.get_ExtendedDisconnectReason
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94c2612b231e24aaec855b6ebd1f9a0498b63c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509283"
---
# <a name="imsrdpclientextendeddisconnectreason-property"></a>IMsRdpClient：： ExtendedDisconnectReason 屬性

包含控制項中斷連接原因的延伸資訊。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_ExtendedDisconnectReason(
  [out] ExtendedDisconnectReasonCode *pExtendedDisconnectReason
);
```



## <a name="property-value"></a>屬性值

[**ExtendedDisconnectReasonCode**](extendeddisconnectreasoncode.md)值的指標，指出用戶端中斷連接的原因。

## <a name="error-codes"></a>錯誤碼

如果方法成功，則會傳回 **S \_ OK** 。 任何其他 **HRESULT** 值都表示呼叫失敗。

## <a name="remarks"></a>備註

通常會在 [**IMsTscAxEvents：： OnDisconnected**](imstscaxevents-ondisconnected.md) 事件處理常式中呼叫這個方法，以取得有關中斷連接事件的其他資訊。

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

[**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





