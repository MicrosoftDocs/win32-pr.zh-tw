---
title: IMsTscSecuredSettings 全螢幕屬性
description: 指定用戶端控制項的全螢幕狀態。
ms.assetid: f65c2fa3-b2d0-4e64-bf1e-08394c91eda8
ms.tgt_platform: multiple
keywords:
- 全螢幕屬性遠端桌面服務
- 全螢幕屬性遠端桌面服務、IMsTscSecuredSettings 介面
- IMsTscSecuredSettings 介面遠端桌面服務、全螢幕屬性
- 全螢幕屬性遠端桌面服務、IMsRdpClientSecuredSettings 介面
- IMsRdpClientSecuredSettings 介面遠端桌面服務、全螢幕屬性
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.Fullscreen
- IMsTscSecuredSettings.get_Fullscreen
- IMsTscSecuredSettings.put_Fullscreen
- IMsRdpClientSecuredSettings.Fullscreen
- IMsRdpClientSecuredSettings.get_Fullscreen
- IMsRdpClientSecuredSettings.put_Fullscreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c3b3208edf3476fcd110d7729d97d9817cb929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965522"
---
# <a name="imstscsecuredsettingsfullscreen-property"></a>IMsTscSecuredSettings：：全螢幕屬性

指定用戶端控制項的全螢幕狀態。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Fullscreen(
  [in]  BOOL fFullScreen
);

HRESULT get_Fullscreen(
  [out] BOOL *pfFullScreen
);
```



## <a name="property-value"></a>屬性值

如果控制項應使用全螢幕模式，請將此參數設定為 **TRUE** ，否則為 **FALSE** 。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

如需此方法的詳細資訊，請參閱 [提供 RDP 用戶端安全性](providing-for-rdp-client-security.md)。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

請注意，雖然使用此屬性只限于允許的 Internet Explorer URL 安全性區域，但是在建立連線之後，使用者隨時都可以在建立連線之後變更為全 [螢幕模式 (](terminal-services-shortcut-keys.md) CTRL + ALT + BREAK) 。

建立用戶端連接時，可以呼叫這個方法。

您必須先呼叫 [**IMsRdpClientNonScriptable3：:p 的 \_ ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) 方法，然後再呼叫 **IMsTscSecuredSettings：:p 的 \_ 全像全螢幕** 方法或 [**IMsRdpClient：:p 的 ui \_ 全螢幕**](imsrdpclient-fullscreen.md) 方式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsTscSecuredSettings 定義為 c9d65442-a0f9-45b2-8f73-d61d2db8cbb6<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





