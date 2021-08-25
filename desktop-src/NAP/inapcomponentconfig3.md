---
title: 'INapComponentConfig3 介面 (NapCommon .h) '
description: 提供適用于系統健全狀況驗證程式的 NAP 系統組態方法 (Shv) 設定和修改特定設定識別碼的設定資料。
ms.assetid: dbb78f7a-7c6b-4bf1-b471-374857d5dafe
keywords:
- INapComponentConfig3 介面 NAP
- INapComponentConfig3 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapComponentConfig3
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea8ab7b42589fa548439b03c04ade56db498750ccd47841b806dcb6b506d3d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803078"
---
# <a name="inapcomponentconfig3-interface"></a>INapComponentConfig3 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapComponentConfig3** 介面會為系統健康狀態驗證 (SHV 提供 NAP 系統組態方法，) 設定和修改特定設定識別碼的設定資料。

> [!Note]  
> 此介面會繼承 [**INapComponentConfig2**](inapcomponentconfig2.md) 的所有方法，因此應該改用。

 

## <a name="members"></a>成員

**INapComponentConfig3** 介面繼承自 [**INapComponentConfig2**](inapcomponentconfig2.md)。 **INapComponentConfig3** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**INapComponentConfig3** 介面具有這些方法。



| 方法                                                                                | 描述                                                                                                    |
|:--------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [**INapComponentConfig3：:D eleteAllConfig**](inapcomponentconfig3-deleteallconfig.md) | 由 Shv 所執行，以提供在安裝之後將 SHV 存放區重設為其原始狀態的方法。<br/>      |
| [**INapComponentConfig3：:D eleteConfig**](inapcomponentconfig3-deleteconfig.md)       | 由 Shv 所執行，以提供一種方法來刪除特定設定識別碼的設定資料。<br/>  |
| [**INapComponentConfig3::GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md) | 由 Shv 所執行，以提供一種方式來取得特定設定識別碼的設定資料。<br/>  |
| [**INapComponentConfig3：： >newconfig.json**](inapcomponentconfig3-newconfig.md)             | 由 Shv 所執行，以提供一種方式來建立特定設定識別碼的設定資料。<br/>  |
| [**INapComponentConfig3::SetConfigToID**](inapcomponentconfig3-setconfigtoid.md)     | 由 Shv 所執行，以提供一種方式來設定特定設定識別碼的設定資料。<br/> |



 

## <a name="remarks"></a>備註

系統健康情況代理程式 (Sha) 或隔離強制用戶端 (Qec) 不應執行此介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>NapCommon。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> <dt>

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

 





