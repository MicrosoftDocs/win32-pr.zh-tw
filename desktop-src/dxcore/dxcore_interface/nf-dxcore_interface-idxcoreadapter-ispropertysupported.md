---
title: IDXCoreAdapter::IsPropertySupported
description: 判斷這個 DXCore 介面卡物件和目前作業系統 (作業系統) 是否支援指定的介面卡屬性。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ddee6bea5af8fb64dfa2bfc15392e92239e7326b34cbd93cbd112559a6027912
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279229"
---
# <a name="idxcoreadapterispropertysupported-method"></a>IDXCoreAdapter：： IsPropertySupported 方法

判斷這個 DXCore 介面卡物件和目前作業系統 (作業系統) 是否支援指定的介面卡屬性。

## <a name="syntax"></a>語法

```cpp
virtual bool STDMETHODCALLTYPE IsPropertySupported( 
  DXCoreAdapterProperty property) = 0;
```

## <a name="parameters"></a>參數

### <a name="property"></a>屬性

類型： **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

您要查詢之支援的屬性類型。 如需每個介面卡屬性的詳細資訊，請參閱 [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) 中的表格。

## <a name="returns"></a>傳回

類型： **bool**

`true`如果這個 DXCore 介面卡物件和目前作業系統 (作業系統) 支援指定的介面卡屬性，則會傳回。 否則傳回 `false`。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [DXCore 參考](../dxcore-reference.md)、 [DXCore 介面卡屬性 guid](../dxcore-adapter-attribute-guids.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)