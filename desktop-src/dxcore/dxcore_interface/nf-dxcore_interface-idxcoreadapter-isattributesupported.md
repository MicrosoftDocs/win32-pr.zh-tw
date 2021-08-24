---
title: IDXCoreAdapter::IsAttributeSupported
description: 判斷這個 DXCore 介面卡物件是否支援指定的介面卡屬性。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 9dda05ca9dc1d3b7a7a84792c7ac122bb64144d5fdba3ad630be1a3f4d9ddf24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787078"
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

`true`如果這個 DXCore 介面卡物件支援指定的介面卡屬性，則傳回。 否則傳回 `false`。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [DXCore 參考](../dxcore-reference.md)、 [DXCore 介面卡屬性 guid](../dxcore-adapter-attribute-guids.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)