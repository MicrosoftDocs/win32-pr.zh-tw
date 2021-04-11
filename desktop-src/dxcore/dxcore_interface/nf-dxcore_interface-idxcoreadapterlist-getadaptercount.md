---
title: IDXCoreAdapterList::GetAdapterCount
description: 捕獲 DXCore 介面卡清單物件中的介面卡數目。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 067e7046d53bdd63f3c8db0c856cf5664a09f426
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186094"
---
# <a name="idxcoreadapterlistgetadaptercount-method"></a>IDXCoreAdapterList：： GetAdapterCount 方法

捕獲 DXCore 介面卡清單物件中的介面卡數目。 如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。

## <a name="syntax"></a>Syntax

```cpp
virtual uint32_t STDMETHODCALLTYPE GetAdapterCount() = 0;
```

## <a name="returns"></a>傳回

類型： **uint32_t**

傳回清單中的介面卡專案數目。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)