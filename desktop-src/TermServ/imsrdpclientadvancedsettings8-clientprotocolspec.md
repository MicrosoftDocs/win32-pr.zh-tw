---
title: IMsRdpClientAdvancedSettings8 ClientProtocolSpec 屬性
description: 指定用戶端與伺服器之間使用的遠端桌面通訊協定。
ms.assetid: DD607D54-CAEA-43EE-94EB-F983AEA0CC1E
ms.tgt_platform: multiple
keywords:
- ClientProtocolSpec 屬性遠端桌面服務
- ClientProtocolSpec 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，ClientProtocolSpec 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings8.ClientProtocolSpec
- IMsRdpClientAdvancedSettings8.get_ClientProtocolSpec
- IMsRdpClientAdvancedSettings8.put_ClientProtocolSpec
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7e0cc7b45e457a2e0300e5e59ac1780a4ac4cd9ef023f10b6a73986a960574
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130129"
---
# <a name="imsrdpclientadvancedsettings8clientprotocolspec-property"></a>IMsRdpClientAdvancedSettings8：： ClientProtocolSpec 屬性

指定用戶端與伺服器之間使用的遠端桌面通訊協定。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ClientProtocolSpec(
  [in]  ClientSpec ClientMode
);

HRESULT get_ClientProtocolSpec(
  [out] ClientSpec *pClientMode
);
```



## <a name="property-value"></a>屬性值

[**ClientSpec**](clientspec.md)列舉的值，指定用戶端與伺服器之間使用的遠端桌面通訊協定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ClientSpec**](clientspec.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> </dl>

 

 





