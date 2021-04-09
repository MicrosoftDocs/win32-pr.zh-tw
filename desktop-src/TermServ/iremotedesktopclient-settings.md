---
title: IRemoteDesktopClient 設定屬性
description: 抓取遠端桌面通訊協定 (RDP) 應用程式容器用戶端的設定物件。
ms.assetid: 59999489-9ad0-4b85-9643-3b8355b817c2
ms.tgt_platform: multiple
keywords:
- Settings 屬性遠端桌面服務
- Settings 屬性遠端桌面服務，IRemoteDesktopClient 介面
- IRemoteDesktopClient 介面遠端桌面服務，Settings 屬性
topic_type:
- apiref
api_name:
- IRemoteDesktopClient.Settings
- IRemoteDesktopClient.get_Settings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e84324eaa12610d7ab898cbcb181e7712bc021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934660"
---
# <a name="iremotedesktopclientsettings-property"></a>IRemoteDesktopClient：： Settings 屬性

抓取遠端桌面通訊協定 (RDP) 應用程式容器用戶端的設定物件。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Settings(
  [out, retval] IRemoteDesktopClientSettings **Settings
);
```



## <a name="property-value"></a>屬性值

RDP 用戶端的設定物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                          |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>  |
| IID<br/>                      | IID \_ IRemoteDesktopClient 定義為 57D25668-625A-4905-BE4E-304CAA13F89C<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IRemoteDesktopClient**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
</dt> </dl>

 

