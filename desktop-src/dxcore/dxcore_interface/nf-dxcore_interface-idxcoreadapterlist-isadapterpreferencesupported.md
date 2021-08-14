---
title: IDXCoreAdapterList::IsAdapterPreferenceSupported
description: 判斷 OS 是否可瞭解指定的 [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) 值。
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: f8a42040ecd6c5667a3d33fb506fd97cfdfe53e8950c2e42b6068bbed6c19467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118502579"
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