---
title: IMsRdpClientAdvancedSettings CachePersistenceActive 屬性
description: 指定是否應該使用持續性點陣圖快取。 持續性快取可以改善效能，但需要額外的磁碟空間。
ms.assetid: 5eb986c4-98dd-426f-8d55-d3a9a526e1b2
ms.tgt_platform: multiple
keywords:
- CachePersistenceActive 屬性遠端桌面服務
- CachePersistenceActive 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，CachePersistenceActive 屬性
- CachePersistenceActive 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，CachePersistenceActive 屬性
- CachePersistenceActive 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，CachePersistenceActive 屬性
- CachePersistenceActive 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，CachePersistenceActive 屬性
- CachePersistenceActive 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，CachePersistenceActive 屬性
- CachePersistenceActive 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，CachePersistenceActive 屬性
- CachePersistenceActive 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，CachePersistenceActive 屬性
- CachePersistenceActive 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，CachePersistenceActive 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.CachePersistenceActive
- IMsRdpClientAdvancedSettings.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings2.CachePersistenceActive
- IMsRdpClientAdvancedSettings2.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings2.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings3.CachePersistenceActive
- IMsRdpClientAdvancedSettings3.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings3.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings4.CachePersistenceActive
- IMsRdpClientAdvancedSettings4.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings4.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings5.CachePersistenceActive
- IMsRdpClientAdvancedSettings5.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings5.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings6.CachePersistenceActive
- IMsRdpClientAdvancedSettings6.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings6.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings7.CachePersistenceActive
- IMsRdpClientAdvancedSettings7.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings7.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings8.CachePersistenceActive
- IMsRdpClientAdvancedSettings8.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings8.put_CachePersistenceActive
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb34e90cc028e95c750a444d53f42c9c0ab77400
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965947"
---
# <a name="imsrdpclientadvancedsettingscachepersistenceactive-property"></a>IMsRdpClientAdvancedSettings：： CachePersistenceActive 屬性

指定是否應該使用持續性點陣圖快取。 持續性快取可以改善效能，但需要額外的磁碟空間。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_CachePersistenceActive(
  [in]  LONG cachePersistenceActive
);

HRESULT get_CachePersistenceActive(
  [out] LONG *pcachePersistenceActive
);
```



## <a name="property-value"></a>屬性值

將此參數設定為0，以停用此功能或非零值以啟用此功能。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

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

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





