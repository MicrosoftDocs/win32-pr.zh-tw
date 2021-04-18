---
title: IMsRdpClientAdvancedSettings TransportType 屬性
description: 指定用戶端所使用的傳輸類型。
ms.assetid: 752f5fbc-eb5a-48eb-8750-fc25c8a2f024
ms.tgt_platform: multiple
keywords:
- TransportType 屬性遠端桌面服務
- TransportType 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，TransportType 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.TransportType
- IMsRdpClientAdvancedSettings.get_TransportType
- IMsRdpClientAdvancedSettings.put_TransportType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0664e0c792725dc112baf786d63c5175eb450dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968739"
---
# <a name="imsrdpclientadvancedsettingstransporttype-property"></a>IMsRdpClientAdvancedSettings：： TransportType 屬性

指定用戶端所使用的傳輸類型。 遠端桌面 ActiveX 控制項不會使用這個屬性。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_TransportType(
  [in]  LONG transportType
);

HRESULT get_TransportType(
  [out] LONG *ptransportType
);
```



## <a name="property-value"></a>屬性值

設定傳輸類型。 這個方法可能會成功，但是遠端桌面 ActiveX 控制項絕不會使用設定的值。

## <a name="remarks"></a>備註

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                        |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                  |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





