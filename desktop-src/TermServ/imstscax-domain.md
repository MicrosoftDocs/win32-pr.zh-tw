---
title: IMsTscAx 網域屬性
description: 指定目前使用者登入的網域。
ms.assetid: 5d9a2048-5f5d-43ca-a8b8-400dac7d7472
ms.tgt_platform: multiple
keywords:
- 網域屬性遠端桌面服務
- 網域屬性遠端桌面服務、IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，網域屬性
- 網域屬性遠端桌面服務、IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，網域屬性
- 網域屬性遠端桌面服務、IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，網域屬性
- 網域屬性遠端桌面服務、IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，網域屬性
- 網域屬性遠端桌面服務、IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，網域屬性
- 網域屬性遠端桌面服務、IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，網域屬性
- 網域屬性遠端桌面服務、IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，網域屬性
- 網域屬性遠端桌面服務、IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，網域屬性
- 網域屬性遠端桌面服務、IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，網域屬性
- 網域屬性遠端桌面服務、IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，網域屬性
topic_type:
- apiref
api_name:
- IMsTscAx.Domain
- IMsTscAx.get_Domain
- IMsTscAx.put_Domain
- IMsRdpClient.Domain
- IMsRdpClient.get_Domain
- IMsRdpClient.put_Domain
- IMsRdpClient2.Domain
- IMsRdpClient2.get_Domain
- IMsRdpClient2.put_Domain
- IMsRdpClient3.Domain
- IMsRdpClient3.get_Domain
- IMsRdpClient3.put_Domain
- IMsRdpClient4.Domain
- IMsRdpClient4.get_Domain
- IMsRdpClient4.put_Domain
- IMsRdpClient5.Domain
- IMsRdpClient5.get_Domain
- IMsRdpClient5.put_Domain
- IMsRdpClient6.Domain
- IMsRdpClient6.get_Domain
- IMsRdpClient6.put_Domain
- IMsRdpClient7.Domain
- IMsRdpClient7.get_Domain
- IMsRdpClient7.put_Domain
- IMsRdpClient8.Domain
- IMsRdpClient8.get_Domain
- IMsRdpClient8.put_Domain
- IMsRdpClient9.Domain
- IMsRdpClient9.get_Domain
- IMsRdpClient9.put_Domain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faf95c02de10fe8db38a53b75d4d20cf796020f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934971"
---
# <a name="imstscaxdomain-property"></a>IMsTscAx：:D omain 屬性

指定目前使用者登入的網域。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Domain(
  [in]  BSTR newVal
);

HRESULT get_Domain(
  [out] BSTR *pDomain
);
```



## <a name="property-value"></a>屬性值

新的功能變數名稱。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

設定 **網域** 屬性是選擇性的。 如果未設定，則使用者可以在連接期間出現 [Windows 登入] 對話方塊時選擇網域。

**Get \_ 網域** 方法會配置 *pDomain* 參數所指向之緩衝區所需的記憶體。 呼叫 C/c + + 應用程式時，必須透過呼叫 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 函式來釋放記憶體。 Visual Basic 和腳本用戶端都不需要這麼做。

只有當控制項不是處於連接狀態時，才能設定這個屬性。 如果在連接控制項時呼叫它，它會傳回 **E \_ FAIL** 。 您可以藉由回應 [**IMsTscAxEvents**](imstscaxevents-interface.md) 中的連接事件，或檢查 [**連接**](imstscax-connected.md) 的屬性來檢查控制項是否已連接。

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

[**連線**](imstscax-connected.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

