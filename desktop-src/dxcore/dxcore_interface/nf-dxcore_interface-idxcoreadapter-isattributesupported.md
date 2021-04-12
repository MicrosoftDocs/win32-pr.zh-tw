---
title: IDXCoreAdapter::IsAttributeSupported
description: 判斷這個 DXCore 介面卡物件是否支援指定的介面卡屬性。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 9824595326f9e81bfa21ab198a3f5b2e6eae74bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375604"
---
# <a name="idxcoreadapterisattributesupported-method"></a>IDXCoreAdapter：： IsAttributeSupported 方法

判斷這個 DXCore 介面卡物件是否支援指定的介面卡屬性。

## <a name="syntax"></a>語法

```cpp
virtual bool STDMETHODCALLTYPE IsAttributeSupported( 
  REFGUID attributeGUID) = 0;
```

## <a name="parameters"></a>參數

### <a name="attributeguid"></a>attributeGUID

類型： **REFGUID**

介面卡屬性 GUID 的參考。 如需屬性 Guid 清單，請參閱 [DXCore adapter 屬性 guid](../dxcore-adapter-attribute-guids.md)。

## <a name="returns"></a>傳回

類型： **bool**

 `true`   如果這個 DXCore 介面卡物件支援指定的介面卡屬性，則傳回。 否則，會傳回  `false` 。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [DXCore 參考](../dxcore-reference.md)、 [DXCore 介面卡屬性 guid](../dxcore-adapter-attribute-guids.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)