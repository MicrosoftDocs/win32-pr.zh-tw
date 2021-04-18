---
title: IDXCoreAdapter::IsPropertySupported
description: 判斷這個 DXCore 介面卡物件和目前作業系統 (作業系統) 是否支援指定的介面卡屬性。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b960d96515d4aee85520a6def70a8f0e9349e131
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968917"
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

 `true`   如果這個 DXCore 介面卡物件和目前作業系統 (作業系統) 支援指定的介面卡屬性，則會傳回。 否則，會傳回  `false` 。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [DXCore 參考](../dxcore-reference.md)、 [DXCore 介面卡屬性 guid](../dxcore-adapter-attribute-guids.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)