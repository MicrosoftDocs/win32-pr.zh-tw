---
title: IMsRdpClientAdvancedSettings BitmapVirtualCache16BppSize 屬性
description: 指定持續性點陣圖快取檔案的大小（以 mb 為單位），以用於每圖元15和16位的高色彩設定。
ms.assetid: f2558c88-d60f-4be3-9941-8e0e18bbb778
ms.tgt_platform: multiple
keywords:
- BitmapVirtualCache16BppSize 屬性遠端桌面服務
- BitmapVirtualCache16BppSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，BitmapVirtualCache16BppSize 屬性
- BitmapVirtualCache16BppSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，BitmapVirtualCache16BppSize 屬性
- BitmapVirtualCache16BppSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，BitmapVirtualCache16BppSize 屬性
- BitmapVirtualCache16BppSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，BitmapVirtualCache16BppSize 屬性
- BitmapVirtualCache16BppSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，BitmapVirtualCache16BppSize 屬性
- BitmapVirtualCache16BppSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，BitmapVirtualCache16BppSize 屬性
- BitmapVirtualCache16BppSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，BitmapVirtualCache16BppSize 屬性
- BitmapVirtualCache16BppSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，BitmapVirtualCache16BppSize 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings2.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings2.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings2.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings3.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings3.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings3.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings4.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings4.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings4.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings5.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCache16BppSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bac538097ac7b31a30c9ed6fe4e5505c89c3e0701d1476edc19efcbc4420520d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353410"
---
# <a name="imsrdpclientadvancedsettingsbitmapvirtualcache16bppsize-property"></a>IMsRdpClientAdvancedSettings：： BitmapVirtualCache16BppSize 屬性

指定持續性點陣圖快取檔案的大小（以 mb 為單位），以用於每圖元15和16位的高色彩設定。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_BitmapVirtualCache16BppSize(
  [in]  LONG bitmapVirtualCache16BppSize
);

HRESULT get_BitmapVirtualCache16BppSize(
  [out] LONG *pbitmapVirtualCache16BppSize
);
```



## <a name="property-value"></a>屬性值

新的快取大小。 有效值為1到32（含），預設值為20。 請注意，所有虛擬快取檔案的大小上限為 128 MB。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

相關屬性包含 **BitmapVirtualCacheSize** 和 **BitmapVirtualCache24BppSize** 屬性。

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

 

 





