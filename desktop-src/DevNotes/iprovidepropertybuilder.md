---
description: 在實 IProvidePropertyBuilder 介面時，會允許物件指定屬性的屬性產生器物件。
ms.assetid: 26557622-4a97-4db0-85ed-3f77fcb769a0
title: IProvidePropertyBuilder 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder:IUnknown
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: b93d05c3c64686b21f19ffe6262ddfd68812dd80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990518"
---
# <a name="iprovidepropertybuilder-interface"></a>IProvidePropertyBuilder 介面

在實 **IProvidePropertyBuilder** 介面時，會允許物件指定屬性的屬性產生器物件。 在 \[ \] 按下按鈕時，會在 Microsoft Visual Studio 的屬性瀏覽器上 (...) 的省略號按鈕叫用產生器，並透過 [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md) 叫用。 若要為指定的屬性提供建立器，請針對 [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md)的目前屬性，傳回應叫用的屬性產生器 GUID。 產生器通常會透過強制回應對話方塊來實行。

這個介面的版本是1.0。 方法呼叫會在動態指派的端點上收到 (如 MSMQ 二進位檔案中的端點對應) 所述，並使用 UUID (全域唯一識別碼) "33C0C1D8-33CF-11d3-BFF2-00C04F990235"。

## <a name="members"></a>成員

**IProvidePropertyBuilder： iunknown** 介面繼承自 [**iunknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IProvidePropertyBuilder** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IProvidePropertyBuilder： IUnknown** 介面具有這些方法。



| 方法                                                                       | 描述                                                                                  |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md)             | 通知物件應針對指定的屬性顯示其產生器。<br/> |
| [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md) | 檢查產生器是否應該與特定屬性相關聯。<br/>         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



 

 
