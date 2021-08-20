---
title: IMsTscAx ConnectingText 屬性
description: 指定控制項連接時，顯示在控制項中央的文字。
ms.assetid: 9bc82074-988f-491b-80e3-00c3f7ba437a
ms.tgt_platform: multiple
keywords:
- ConnectingText 屬性遠端桌面服務
- ConnectingText 屬性遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，ConnectingText 屬性
- ConnectingText 屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，ConnectingText 屬性
- ConnectingText 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，ConnectingText 屬性
- ConnectingText 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，ConnectingText 屬性
- ConnectingText 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，ConnectingText 屬性
- ConnectingText 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，ConnectingText 屬性
- ConnectingText 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，ConnectingText 屬性
- ConnectingText 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，ConnectingText 屬性
- ConnectingText 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，ConnectingText 屬性
- ConnectingText 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，ConnectingText 屬性
topic_type:
- apiref
api_name:
- IMsTscAx.ConnectingText
- IMsTscAx.get_ConnectingText
- IMsTscAx.put_ConnectingText
- IMsRdpClient.ConnectingText
- IMsRdpClient.get_ConnectingText
- IMsRdpClient.put_ConnectingText
- IMsRdpClient2.ConnectingText
- IMsRdpClient2.get_ConnectingText
- IMsRdpClient2.put_ConnectingText
- IMsRdpClient3.ConnectingText
- IMsRdpClient3.get_ConnectingText
- IMsRdpClient3.put_ConnectingText
- IMsRdpClient4.ConnectingText
- IMsRdpClient4.get_ConnectingText
- IMsRdpClient4.put_ConnectingText
- IMsRdpClient5.ConnectingText
- IMsRdpClient5.get_ConnectingText
- IMsRdpClient5.put_ConnectingText
- IMsRdpClient6.ConnectingText
- IMsRdpClient6.get_ConnectingText
- IMsRdpClient6.put_ConnectingText
- IMsRdpClient7.ConnectingText
- IMsRdpClient7.get_ConnectingText
- IMsRdpClient7.put_ConnectingText
- IMsRdpClient8.ConnectingText
- IMsRdpClient8.get_ConnectingText
- IMsRdpClient8.put_ConnectingText
- IMsRdpClient9.ConnectingText
- IMsRdpClient9.get_ConnectingText
- IMsRdpClient9.put_ConnectingText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7342e47658e77d9fb29ef03ab1995e5263c78a8e31d2f020852e5fa10864a031
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129670"
---
# <a name="imstscaxconnectingtext-property"></a>IMsTscAx：： ConnectingText 屬性

指定控制項連接時，顯示在控制項中央的文字。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ConnectingText(
  [in]  BSTR newVal
);

HRESULT get_ConnectingText(
  [out] BSTR *pConnectingText
);
```



## <a name="property-value"></a>屬性值

新的顯示文字。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

如果發生錯誤，則傳回非零的 **HRESULT** 。

## <a name="remarks"></a>備註

連接文字的範例是「正在連接到伺服器 ...」。

設定 **ConnectingText** 屬性是選擇性的。 如果未設定，則在建立連接之前，控制項會顯示空白。

只有當控制項不是處於連接狀態時，才能設定這個屬性。 如果在連接控制項時呼叫它，它會傳回 **E \_ FAIL** 。 您可以藉由回應 [**IMsTscAxEvents**](imstscaxevents-interface.md) 中的連接事件，或檢查 [**連接**](imstscax-connected.md) 的屬性來檢查控制項是否已連接。

**Get \_ ConnectingText** 屬性方法會配置 *pConnectingText* 參數所指向之緩衝區所需的記憶體。 呼叫 C/c + + 應用程式時，必須透過呼叫 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 函式來釋放記憶體。 Visual Basic 和腳本用戶端都不需要這麼做。

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

 

