---
title: IDXCoreAdapter::IsValid
description: 判斷這個 DXCore 介面卡物件是否仍然有效。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6b8a0ccadb46f20db9c5f2a23ac8709b391254ee453f05424dadee309f33fc40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842538"
---
# <a name="idxcoreadapterisvalid-method"></a>IDXCoreAdapter：： IsValid 方法

判斷這個 DXCore 介面卡物件是否仍然有效。 如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。

## <a name="syntax"></a>Syntax

```cpp
virtual bool STDMETHODCALLTYPE IsValid() = 0;
```

## <a name="returns"></a>傳回

類型： **bool**

`true`如果這個 DXCore 介面卡物件仍然有效，則會傳回。 否則傳回 `false`。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)