---
title: IMsRdpClientSecuredSettings AudioRedirectionMode 屬性
description: 指定音訊重新導向設定，指定是否要在遠端桌面工作階段主機 (RD 工作階段主機) 伺服器上，重新導向聲音或播放音效。
ms.assetid: 6aa63a50-a714-4a9b-a4ec-c0551920467a
ms.tgt_platform: multiple
keywords:
- AudioRedirectionMode 屬性遠端桌面服務
- AudioRedirectionMode 屬性遠端桌面服務，IMsRdpClientSecuredSettings 介面
- IMsRdpClientSecuredSettings 介面遠端桌面服務，AudioRedirectionMode 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.AudioRedirectionMode
- IMsRdpClientSecuredSettings.get_AudioRedirectionMode
- IMsRdpClientSecuredSettings.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 858342811ec97def95031ebed0605b5a81cf80fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509469"
---
# <a name="imsrdpclientsecuredsettingsaudioredirectionmode-property"></a>IMsRdpClientSecuredSettings：： AudioRedirectionMode 屬性

指定音訊重新導向設定，指定是否要在遠端桌面工作階段主機 (RD 工作階段主機) 伺服器上，重新導向聲音或播放音效。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AudioRedirectionMode(
  [in]  LONG audioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] LONG *paudioRedirectionMode
);
```



## <a name="property-value"></a>屬性值

新的設定。 此參數可以是下列其中一個值。

<dt>

0
</dt> <dd>

將聲音重新導向至用戶端。 這是預設值。

</dd> <dt>

1
</dt> <dd>

在遠端電腦上播放音效。

</dd> <dt>

2
</dt> <dd>

停用音效重新導向;不要在伺服器上播放聲音。

</dd> </dl>

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

連接控制項時無法設定這些屬性。

如需詳細資訊，請參閱 [提供 RDP 用戶端安全性](providing-for-rdp-client-security.md) 。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                 |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ IMsRdpClientSecuredSettings 定義為605befcf-39c1-45cc-a811-068fb7be346d<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





