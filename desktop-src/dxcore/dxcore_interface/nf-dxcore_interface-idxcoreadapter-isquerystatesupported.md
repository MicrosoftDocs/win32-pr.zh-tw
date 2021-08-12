---
title: IDXCoreAdapter::IsQueryStateSupported
description: 判斷這個 DXCore 介面卡物件和目前作業系統 (作業系統) 是否支援查詢指定介面卡狀態的值。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 8ae77c308cb251982947d91e23eaef8f6d828c1233df442cb013bf9737e3c57d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279219"
---
# <a name="idxcoreadapterisquerystatesupported-method"></a>IDXCoreAdapter：： IsQueryStateSupported 方法

判斷這個 DXCore 介面卡物件和目前作業系統 (作業系統) 是否支援查詢指定介面卡狀態的值。

## <a name="syntax"></a>語法

```cpp
virtual bool STDMETHODCALLTYPE IsQueryStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a>參數

### <a name="state"></a>狀態

類型： **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

您所查詢的狀態專案的支援類型。 如需每個介面卡狀態種類的詳細資訊，請參閱 [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) 中的表格。

## <a name="returns"></a>傳回

類型： **bool**

`true`如果這個 DXCore 介面卡物件和目前作業系統 (作業系統) 支援查詢指定的介面卡狀態，則會傳回。 否則傳回 `false`。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [DXCore 參考](../dxcore-reference.md)、 [DXCore 介面卡屬性 guid](../dxcore-adapter-attribute-guids.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)