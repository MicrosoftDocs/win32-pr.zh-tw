---
title: 'IMsTscAx 伺服器屬性 (Asptlb .h) '
description: 指定目前控制項所連接的伺服器名稱。
ms.assetid: 81118ddd-2662-47f5-8e9d-9c2a5056820b
ms.tgt_platform: multiple
keywords:
- 伺服器屬性遠端桌面服務
- 伺服器屬性遠端桌面服務、IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，伺服器屬性
- 伺服器屬性遠端桌面服務、IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，伺服器屬性
- 伺服器屬性遠端桌面服務、IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，伺服器屬性
- 伺服器屬性遠端桌面服務、IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，伺服器屬性
- 伺服器屬性遠端桌面服務、IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，伺服器屬性
- 伺服器屬性遠端桌面服務、IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，伺服器屬性
- 伺服器屬性遠端桌面服務、IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，伺服器屬性
- 伺服器屬性遠端桌面服務、IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，伺服器屬性
- 伺服器屬性遠端桌面服務、IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，伺服器屬性
- 伺服器屬性遠端桌面服務、IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，伺服器屬性
topic_type:
- apiref
api_name:
- IMsTscAx.Server
- IMsTscAx.get_Server
- IMsTscAx.put_Server
- IMsRdpClient.Server
- IMsRdpClient.get_Server
- IMsRdpClient.put_Server
- IMsRdpClient2.Server
- IMsRdpClient2.get_Server
- IMsRdpClient2.put_Server
- IMsRdpClient3.Server
- IMsRdpClient3.get_Server
- IMsRdpClient3.put_Server
- IMsRdpClient4.Server
- IMsRdpClient4.get_Server
- IMsRdpClient4.put_Server
- IMsRdpClient5.Server
- IMsRdpClient5.get_Server
- IMsRdpClient5.put_Server
- IMsRdpClient6.Server
- IMsRdpClient6.get_Server
- IMsRdpClient6.put_Server
- IMsRdpClient7.Server
- IMsRdpClient7.get_Server
- IMsRdpClient7.put_Server
- IMsRdpClient8.Server
- IMsRdpClient8.get_Server
- IMsRdpClient8.put_Server
- IMsRdpClient9.Server
- IMsRdpClient9.get_Server
- IMsRdpClient9.put_Server
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8ce72d7cc26dc3fd7b60b7f1d4f26d2737980dfde88a1b31c79a59fb4335f96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770998"
---
# <a name="imstscaxserver-property"></a>IMsTscAx：： Server 屬性

指定目前控制項所連接的伺服器名稱。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Server(
  [in]  BSTR newVal
);

HRESULT get_Server(
  [out] BSTR *pServer
);
```



## <a name="property-value"></a>屬性值

新的伺服器名稱。 此參數可以是 DNS 名稱或 IP 位址。

## <a name="error-codes"></a>錯誤碼

如果方法成功，則會傳回 **S \_ OK** 。 任何其他 **HRESULT** 值都表示呼叫失敗。

## <a name="remarks"></a>備註

在呼叫 [**連線**](imstscax-connect.md)方法之前，必須先設定這個屬性。 它是唯一必須在連接之前設定的屬性。

只有當控制項不是處於連接狀態時，才能設定這個屬性。 如果在連接控制項時呼叫這個屬性，則這個屬性會傳回 **E \_ FAIL** 。 您可以使用 [**連接**](imstscax-connected.md) 的屬性來檢查連接的狀態。

這個方法會配置 *pServer* 參數所指向之緩衝區所需的記憶體。 呼叫 C/c + + 應用程式時，必須透過呼叫 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 函式來釋放記憶體。 Visual Basic 和腳本用戶端都不需要這麼做。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 標頭<br/>                   | <dl> <dt>Asptlb。h</dt> </dl>    |
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

 

