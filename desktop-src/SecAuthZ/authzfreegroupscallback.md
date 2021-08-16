---
description: 釋放 AuthzComputeGroupsCallback 函式所配置記憶體的應用程式定義函數。 AuthzFreeGroupsCallback 是應用程式定義函數名稱的預留位置。
ms.assetid: 5563311c-2bd1-4e96-ba0a-5a4225050f77
title: AuthzFreeGroupsCallback 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 3cce78e261892fede79fb8fc76bc5b0d009342db3e0bf672be2854cb8492bcec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783762"
---
# <a name="authzfreegroupscallback-callback-function"></a>AuthzFreeGroupsCallback 回呼函式

**AuthzFreeGroupsCallback** 函式是應用程式定義的函式，可釋出由 [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md)函數配置的記憶體。 **AuthzFreeGroupsCallback** 是應用程式定義函數名稱的預留位置。

## <a name="syntax"></a>語法


```C++
void CALLBACK AuthzFreeGroupsCallback(
  _In_ PSID_AND_ATTRIBUTES pSidAttrArray
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSidAttrArray* \[在\]
</dt> <dd>

[**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md)所配置之記憶體的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個回呼函式不會傳回值。

## <a name="remarks"></a>備註

使用邏輯運算子時，屬性變數的格式必須是運算式;否則會評估為 unknown。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                   |
| 可轉散發套件<br/>          | WindowsWindows XP 上的 Server 2003 管理工具套件<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[基本存取控制功能](authorization-functions.md)
</dt> <dt>

[**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md)
</dt> </dl>

 

 




