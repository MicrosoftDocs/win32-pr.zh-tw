---
title: IDXCoreAdapterList::IsAdapterPreferenceSupported
description: 判斷 OS 是否可瞭解指定的 [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) 值。
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 1678568eb17c0dd833c130e6184931c8896261e9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682542"
---
# <a name="idxcoreadapterlistisadapterpreferencesupported-method"></a>IDXCoreAdapterList：： IsAdapterPreferenceSupported 方法

## <a name="description"></a>Description

判斷目前作業系統 (作業系統) 是否瞭解指定的 [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) 值。 您可以在呼叫 [IDXCoreAdapterList：： Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md)之前呼叫 **IsAdapterPreferenceSupported** 。

## <a name="syntax"></a>語法

```cpp
bool IsAdapterPreferenceSupported(
  DXCoreAdapterPreference preference
);
```

## <a name="parameters"></a>參數

### <a name="preference"></a>preference

類型： **[DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)**

系統會檢查 [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) 值，以查看作業系統是否支援此值。

## <a name="returns"></a>傳回

類型： **bool**

`true`如果目前的作業系統瞭解排序類型，則傳回。 否則傳回 `false`。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)