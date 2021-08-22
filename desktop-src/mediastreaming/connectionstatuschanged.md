---
title: ConnectionStatusChanged 事件
description: 發生于裝置的網路連接狀態變更時。
ms.assetid: d1f04fa5-895e-4e86-9643-e880388dcded
keywords:
- ConnectionStatusChanged 事件媒體串流 API
topic_type:
- apiref
api_name:
- ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ccc19c71b56977a77ac5ec05448ea72eaff79d9e96b42f4f297d7046079f571
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060428"
---
# <a name="connectionstatuschanged-event"></a>ConnectionStatusChanged 事件

發生于裝置的網路連接狀態變更時。

## <a name="syntax"></a>語法


```C++
void ConnectionStatusChanged();
```



## <a name="parameters"></a>參數

此事件沒有任何參數。

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

若要處理此事件的通知，請使用 [**add \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md)方法來註冊 [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))事件處理常式函式。 若要取消註冊事件處理常式，請使用 [**remove \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) 方法。

 

 