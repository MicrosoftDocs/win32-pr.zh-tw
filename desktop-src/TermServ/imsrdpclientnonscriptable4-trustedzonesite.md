---
title: IMsRdpClientNonScriptable4 TrustedZoneSite 屬性
description: 指定使用者啟動連線的網站是否位於使用者用戶端電腦的 [信任的網站] 清單中。
ms.assetid: cb7efacc-b13b-494c-ab02-35c4f914744c
ms.tgt_platform: multiple
keywords:
- TrustedZoneSite 屬性遠端桌面服務
- TrustedZoneSite 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，TrustedZoneSite 屬性
- TrustedZoneSite 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，TrustedZoneSite 屬性
- TrustedZoneSite 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、TrustedZoneSite 屬性
- TrustedZoneSite 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、TrustedZoneSite 屬性
- TrustedZoneSite 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、TrustedZoneSite 屬性
- TrustedZoneSite 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、TrustedZoneSite 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.TrustedZoneSite
- IMsRdpClientNonScriptable4.get_TrustedZoneSite
- IMsRdpClientNonScriptable4.put_TrustedZoneSite
- IMsRdpClientNonScriptable5.TrustedZoneSite
- IMsRdpClientNonScriptable5.get_TrustedZoneSite
- IMsRdpClientNonScriptable5.put_TrustedZoneSite
- MsRdpClient6.TrustedZoneSite
- MsRdpClient7.TrustedZoneSite
- MsRdpClient8.TrustedZoneSite
- MsRdpClient9.TrustedZoneSite
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d791b5eff3346f61f999ea1f4f78bc41a5acea0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384893"
---
# <a name="imsrdpclientnonscriptable4trustedzonesite-property"></a>IMsRdpClientNonScriptable4：： TrustedZoneSite 屬性

指定使用者啟動連線的網站是否位於使用者用戶端電腦的 [信任的網站] 清單中。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_TrustedZoneSite(
  [in]  VARIANT_BOOL fIsTrustedZone
);

HRESULT get_TrustedZoneSite(
  [out] VARIANT_BOOL *pfIsTrustedZone
);
```



## <a name="property-value"></a>屬性值

設定 TrustedZoneSite 屬性。 這個方法不會影響使用者啟動連線的網站是否位於用戶端電腦的 [信任的網站] 清單中。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 定義為 f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





