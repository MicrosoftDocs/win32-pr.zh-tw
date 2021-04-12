---
title: IMsRdpClient 全螢幕屬性
description: 判斷用戶端控制項是否處於全螢幕模式。
ms.assetid: 64fe2835-c00e-4d21-812d-dcf160147d93
ms.tgt_platform: multiple
keywords:
- 全螢幕屬性遠端桌面服務
- 全螢幕屬性遠端桌面服務、IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務、全螢幕屬性
- 全螢幕屬性遠端桌面服務、IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務、全螢幕屬性
- 全螢幕屬性遠端桌面服務、IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務、全螢幕屬性
- 全螢幕屬性遠端桌面服務、IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務、全螢幕屬性
- 全螢幕屬性遠端桌面服務、IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務、全螢幕屬性
- 全螢幕屬性遠端桌面服務、IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務、全螢幕屬性
- 全螢幕屬性遠端桌面服務、IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務、全螢幕屬性
- 全螢幕屬性遠端桌面服務、IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務、全螢幕屬性
- 全螢幕屬性遠端桌面服務、IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務、全螢幕屬性
- 全螢幕屬性遠端桌面服務、IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務、全螢幕屬性
topic_type:
- apiref
api_name:
- IMsRdpClient.FullScreen
- IMsRdpClient.get_FullScreen
- IMsRdpClient.put_FullScreen
- IMsRdpClient2.FullScreen
- IMsRdpClient2.get_FullScreen
- IMsRdpClient2.put_FullScreen
- IMsRdpClient3.FullScreen
- IMsRdpClient3.get_FullScreen
- IMsRdpClient3.put_FullScreen
- IMsRdpClient4.FullScreen
- IMsRdpClient4.get_FullScreen
- IMsRdpClient4.put_FullScreen
- IMsRdpClient5.FullScreen
- IMsRdpClient5.get_FullScreen
- IMsRdpClient5.put_FullScreen
- IMsRdpClient6.FullScreen
- IMsRdpClient6.get_FullScreen
- IMsRdpClient6.put_FullScreen
- IMsRdpClient7.FullScreen
- IMsRdpClient7.get_FullScreen
- IMsRdpClient7.put_FullScreen
- IMsRdpClient8.FullScreen
- IMsRdpClient8.get_FullScreen
- IMsRdpClient8.put_FullScreen
- IMsRdpClient9.FullScreen
- IMsRdpClient9.get_FullScreen
- IMsRdpClient9.put_FullScreen
- IMsRdpClient10.FullScreen
- IMsRdpClient10.get_FullScreen
- IMsRdpClient10.put_FullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adbc8e11d2cc4fb4a8071372777a01d81b5edad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105875"
---
# <a name="imsrdpclientfullscreen-property"></a>IMsRdpClient：：全螢幕屬性

判斷用戶端控制項是否處於全螢幕模式。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_FullScreen(
  [in]  VARIANT_BOOL fFullScreen
);

HRESULT get_FullScreen(
  [out] VARIANT_BOOL *pfFullScreen
);
```



## <a name="property-value"></a>屬性值

**True** 表示輸入全螢幕模式， **False** 則會離開全螢幕模式並返回視窗模式。

## <a name="error-codes"></a>錯誤碼

如果方法成功，則會傳回 **S \_ OK** 。 任何其他 **HRESULT** 值都表示呼叫失敗。

## <a name="remarks"></a>備註

連接控制項時，您可以設定這個屬性。

您必須先呼叫 [**IMsRdpClientNonScriptable3：:p 的 \_ ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) 方法，然後再呼叫 [**IMsTscSecuredSettings：:p 的 \_ 全像全螢幕**](imstscsecuredsettings-fullscreen.md) 方法或 **IMsRdpClient：:p 的 ui \_ 全螢幕** 方式。

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

 

 





