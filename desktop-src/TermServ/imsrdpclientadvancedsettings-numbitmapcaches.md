---
title: IMsRdpClientAdvancedSettings NumBitmapCaches 屬性
description: 不支援這個屬性。 |IMsRdpClientAdvancedSettings NumBitmapCaches 屬性
ms.assetid: a413b2c0-7661-415d-bc38-e8fd55006e8c
ms.tgt_platform: multiple
keywords:
- NumBitmapCaches 屬性遠端桌面服務
- NumBitmapCaches 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，NumBitmapCaches 屬性
- NumBitmapCaches 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，NumBitmapCaches 屬性
- NumBitmapCaches 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，NumBitmapCaches 屬性
- NumBitmapCaches 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，NumBitmapCaches 屬性
- NumBitmapCaches 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，NumBitmapCaches 屬性
- NumBitmapCaches 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，NumBitmapCaches 屬性
- NumBitmapCaches 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，NumBitmapCaches 屬性
- NumBitmapCaches 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，NumBitmapCaches 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.NumBitmapCaches
- IMsRdpClientAdvancedSettings.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings2.NumBitmapCaches
- IMsRdpClientAdvancedSettings2.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings2.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings3.NumBitmapCaches
- IMsRdpClientAdvancedSettings3.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings3.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings4.NumBitmapCaches
- IMsRdpClientAdvancedSettings4.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings4.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings5.NumBitmapCaches
- IMsRdpClientAdvancedSettings5.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings5.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings6.NumBitmapCaches
- IMsRdpClientAdvancedSettings6.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings6.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings7.NumBitmapCaches
- IMsRdpClientAdvancedSettings7.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings7.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings8.NumBitmapCaches
- IMsRdpClientAdvancedSettings8.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings8.put_NumBitmapCaches
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ae60423287da041e3f84b28d8d51388e9a4050b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106976669"
---
# <a name="imsrdpclientadvancedsettingsnumbitmapcaches-property"></a>IMsRdpClientAdvancedSettings：： NumBitmapCaches 屬性

不支援這個屬性。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_NumBitmapCaches(
  [in]  LONG numBitmapCaches
);

HRESULT get_NumBitmapCaches(
  [out] LONG *pnumBitmapCaches
);
```



## <a name="property-value"></a>屬性值

新的快取數目。 預設值為3，這會產生最佳效能。

## <a name="error-codes"></a>錯誤碼

傳回 **\_ FALSE**。

## <a name="remarks"></a>備註

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                       |
| 用戶端支援結束<br/>    | 都不支援<br/>                                                                       |
| 伺服器支援結束<br/>    | 都不支援<br/>                                                                       |
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

 

 





