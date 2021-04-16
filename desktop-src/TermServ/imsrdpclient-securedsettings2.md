---
title: IMsRdpClient SecuredSettings2 屬性
description: 捕獲 IMsRdpClientSecuredSettings 介面的指標。 這個介面可以用來設定用戶端控制項的安全設定。
ms.assetid: f570a3f6-70ae-45fd-ba20-75c9f4d2f5ca
ms.tgt_platform: multiple
keywords:
- SecuredSettings2 屬性遠端桌面服務
- SecuredSettings2 屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，SecuredSettings2 屬性
- SecuredSettings2 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，SecuredSettings2 屬性
- SecuredSettings2 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，SecuredSettings2 屬性
- SecuredSettings2 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，SecuredSettings2 屬性
- SecuredSettings2 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，SecuredSettings2 屬性
- SecuredSettings2 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，SecuredSettings2 屬性
- SecuredSettings2 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，SecuredSettings2 屬性
- SecuredSettings2 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，SecuredSettings2 屬性
- SecuredSettings2 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，SecuredSettings2 屬性
- SecuredSettings2 屬性遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，SecuredSettings2 屬性
topic_type:
- apiref
api_name:
- IMsRdpClient.SecuredSettings2
- IMsRdpClient.get_SecuredSettings2
- IMsRdpClient2.SecuredSettings2
- IMsRdpClient2.get_SecuredSettings2
- IMsRdpClient3.SecuredSettings2
- IMsRdpClient3.get_SecuredSettings2
- IMsRdpClient4.SecuredSettings2
- IMsRdpClient4.get_SecuredSettings2
- IMsRdpClient5.SecuredSettings2
- IMsRdpClient5.get_SecuredSettings2
- IMsRdpClient6.SecuredSettings2
- IMsRdpClient6.get_SecuredSettings2
- IMsRdpClient7.SecuredSettings2
- IMsRdpClient7.get_SecuredSettings2
- IMsRdpClient8.SecuredSettings2
- IMsRdpClient8.get_SecuredSettings2
- IMsRdpClient9.SecuredSettings2
- IMsRdpClient9.get_SecuredSettings2
- IMsRdpClient10.SecuredSettings2
- IMsRdpClient10.get_SecuredSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39e26d9d7a7b2ac776166c251e5a2ab9923297f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508300"
---
# <a name="imsrdpclientsecuredsettings2-property"></a>IMsRdpClient：： SecuredSettings2 屬性

捕獲 [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) 介面的指標。 這個介面可以用來設定用戶端控制項的安全設定。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_SecuredSettings2(
  [out] IMsRdpClientSecuredSettings **ppSecuredSettings
);
```



## <a name="property-value"></a>屬性值

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)介面指標。

## <a name="error-codes"></a>錯誤碼

如果方法成功，則會傳回 **S \_ OK** 。 任何其他 **HRESULT** 值都表示呼叫失敗。

## <a name="remarks"></a>備註

如需詳細資訊，請參閱 [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) 介面，並 [提供 RDP 用戶端安全性](providing-for-rdp-client-security.md)。

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
</dt> </dl>

 

 





