---
title: IMsRdpClientAdvancedSettings SasSequence 屬性
description: 指定用戶端將用來存取伺服器上登入畫面 (SAS) 的安全存取順序。
ms.assetid: ec1dc7b1-2bf1-447b-a768-08f28982a995
ms.tgt_platform: multiple
keywords:
- SasSequence 屬性遠端桌面服務
- SasSequence 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，SasSequence 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.SasSequence
- IMsRdpClientAdvancedSettings.get_SasSequence
- IMsRdpClientAdvancedSettings.put_SasSequence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cf38a4e1f048e67613b92b3629aa96cca281b1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464320"
---
# <a name="imsrdpclientadvancedsettingssassequence-property"></a>IMsRdpClientAdvancedSettings：： SasSequence 屬性

指定用戶端將用來存取伺服器上登入畫面 (SAS) 的安全存取順序。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SasSequence(
  [in]  LONG sasSequence
);

HRESULT get_SasSequence(
  [out] LONG *psasSequence
);
```



## <a name="property-value"></a>屬性值

包含 SAS 指標的 **長** 數值。 唯一支援的值是0xaa03，表示標準 CTRL + ALT + DELETE 序列。

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

 

 





