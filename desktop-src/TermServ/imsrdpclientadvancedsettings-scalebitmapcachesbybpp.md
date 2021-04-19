---
title: IMsRdpClientAdvancedSettings ScaleBitmapCachesByBPP 屬性
description: 不支援這個屬性。 |IMsRdpClientAdvancedSettings ScaleBitmapCachesByBPP 屬性
ms.assetid: 1da3d634-6322-4546-92cf-5607dc74d400
ms.tgt_platform: multiple
keywords:
- ScaleBitmapCachesByBPP 屬性遠端桌面服務
- ScaleBitmapCachesByBPP 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，ScaleBitmapCachesByBPP 屬性
- ScaleBitmapCachesByBPP 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，ScaleBitmapCachesByBPP 屬性
- ScaleBitmapCachesByBPP 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，ScaleBitmapCachesByBPP 屬性
- ScaleBitmapCachesByBPP 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，ScaleBitmapCachesByBPP 屬性
- ScaleBitmapCachesByBPP 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，ScaleBitmapCachesByBPP 屬性
- ScaleBitmapCachesByBPP 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，ScaleBitmapCachesByBPP 屬性
- ScaleBitmapCachesByBPP 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，ScaleBitmapCachesByBPP 屬性
- ScaleBitmapCachesByBPP 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，ScaleBitmapCachesByBPP 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings.get_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings.put_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings2.ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings2.get_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings2.put_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings3.ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings3.get_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings3.put_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings4.ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings4.get_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings4.put_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings5.ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings5.get_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings5.put_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings6.ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings6.get_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings6.put_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings7.ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings7.get_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings7.put_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings8.ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings8.get_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings8.put_ScaleBitmapCachesByBPP
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47e7072d83bf3d9e71a888b5137be4ddcf93f826
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106976678"
---
# <a name="imsrdpclientadvancedsettingsscalebitmapcachesbybpp-property"></a>IMsRdpClientAdvancedSettings：： ScaleBitmapCachesByBPP 屬性

不支援這個屬性。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ScaleBitmapCachesByBPP(
  [in]  LONG bScale
);

HRESULT get_ScaleBitmapCachesByBPP(
  [out] LONG *pbScale
);
```



## <a name="property-value"></a>屬性值

將此參數設定為0，以停用此功能或非零值以啟用此功能。

## <a name="error-codes"></a>錯誤碼

傳回 **\_ FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                       |
| 用戶端支援結束<br/>    | 都不支援<br/>                                                                       |
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

 

 





