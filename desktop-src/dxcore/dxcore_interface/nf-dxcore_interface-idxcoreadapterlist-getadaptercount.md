---
title: IDXCoreAdapterList::GetAdapterCount
description: 捕獲 DXCore 介面卡清單物件中的介面卡數目。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 952120a039e4060a45f5e6e1de607fd68b50fcd7d7cd88ce5a98474f8f2dcfdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985118"
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