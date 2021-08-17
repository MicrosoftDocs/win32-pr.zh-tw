---
title: '隱私權類型 (Wininet. h) '
description: 指定隱私權設定適用于第一方或協力廠商 cookie。
ms.assetid: 7d0846d4-fd81-4af9-b7e6-05c4c1438770
topic_type:
- apiref
api_name:
- PRIVACY_TYPE_FIRST_PARTY
- PRIVACY_TYPE_THIRD_PARTY
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af6f29461f57a2209fde00b30bce7914c207958f27e28062e2c3bd3d94d442e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743725"
---
# <a name="privacy-type"></a>隱私權類型

指定隱私權設定適用于第一方或協力廠商 cookie。

<dl> <dt>

<span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**隱私權 \_ 類型 \_ 第一 \_ 方**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



是指第一方 cookie 的隱私權設定。


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**隱私權 \_ 類型 \_ 第三 \_ 方**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



指的是協力廠商 cookie 的隱私權設定。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

Cookie 會分類為第一方和協力廠商。 第一方 cookie 是源自主機網域的 cookie。 如果 https://www.blueyonderairlines.com 在 Microsoft Internet Explorer 網址列中找到 ""，則 "www.blueyonderairlines.com" 是主機網域。 造訪此頁面時，如果從 "www.blueyonderairlines.com" 以外的網域設定 cookie （例如 "www.fourthcoffee.com"），則會將此 cookie 視為協力廠商 cookie。

> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 若為伺服器執行或服務，請使用[Microsoft Windows HTTP 服務 (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Wininet</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PrivacyGetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[**PrivacySetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

