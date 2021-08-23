---
title: 'FreeRootCauseInfos 函式 (Ndattributils) '
description: 將內部配置的記憶體解除配置至 RootCauseInfo 結構的陣列。
ms.assetid: b45fa432-0db4-470b-80ce-ae25c33f88d6
keywords:
- FreeRootCauseInfos 函式 NDF
topic_type:
- apiref
api_name:
- FreeRootCauseInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9cbd0386af86ebe5e1fdc5e6350cebfb305f44544f8822e0f2bde4d46cb55f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065238"
---
# <a name="freerootcauseinfos-function"></a>FreeRootCauseInfos 函式

**FreeRootCauseInfos** 函式會將內部配置的記憶體解除配置至 [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)結構的陣列。 此函數會呼叫 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) 來解除配置記憶體。

## <a name="syntax"></a>語法


```C++
VOID FreeRootCauseInfos(
  _In_ RootCauseInfo *pInfo,
       ULONG         RootCauseCount,
       BOOL          bFreePointer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pInfo* \[在\]
</dt> <dd>

類型： **[ **RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\***

結構的陣列。 將釋放這些結構所指向的配置記憶體。

</dd> <dt>

*RootCauseCount* 
</dt> <dd>

類型： **ULONG**

*PInfo* 所指向之陣列中的結構數目。

</dd> <dt>

*bFreePointer* 
</dt> <dd>

類型： **BOOL**

如果也應該刪除結構的陣列，則為 True;否則為 false。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>Ndattributils。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

