---
title: IDXCoreAdapterList::IsStale
description: 判斷此系統的變更是否造成此 DXCore 介面卡清單物件過期。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: a40a590a76773592d5442993c75149b2349880f7681d625e777d363062f5c4be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118502569"
---
# <a name="idxcoreadapterlistisstale-method"></a>IDXCoreAdapterList：： IsStale 方法

判斷此系統的變更是否造成此 DXCore 介面卡清單物件過期。 如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。

## <a name="syntax"></a>Syntax

```cpp
virtual bool STDMETHODCALLTYPE IsStale() = 0;
```

## <a name="returns"></a>傳回

類型： **bool**

`true`如果產生清單，則會傳回系統狀況的變更，使此介面卡清單變成過時。 否則傳回 `false`。

## <a name="remarks"></a>備註

您可以輪詢 **IsStale** ，以判斷變更的系統條件是否會導致此清單變成過期。 如果 **IsStale** 傳回 `true` 一次，則會傳回 `true` DXCore 介面卡清單物件的剩餘存留期。 即使系統條件返回符合清單的狀態，也會將過時的清單物件視為過時， (相同的條件會立即取得，就像是首次產生清單一樣) 。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)