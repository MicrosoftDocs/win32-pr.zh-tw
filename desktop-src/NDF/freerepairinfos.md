---
title: 'FreeRepairInfos 函式 (Ndattributils) '
description: 將內部配置的記憶體解除配置至 RepairInfo 結構的陣列。
ms.assetid: c40f9d10-8d9e-4c79-ac0b-fa88608888f1
keywords:
- FreeRepairInfos 函式 NDF
topic_type:
- apiref
api_name:
- FreeRepairInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 745f6cd9a7fd484db943fc91c5c9dadf440b3635f31cdb539b356358c22362a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798603"
---
# <a name="freerepairinfos-function"></a>FreeRepairInfos 函式

**FreeRepairInfos** 函式會將內部配置的記憶體解除配置至 [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)結構的陣列。 此函數會呼叫 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) 來解除配置記憶體。

## <a name="syntax"></a>語法


```C++
VOID FreeRepairInfos(
  _In_ RepairInfo *pInfo,
       ULONG      RepairCount,
       BOOL       bFreePointer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pInfo* \[在\]
</dt> <dd>

類型： **[ **RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\***

結構的陣列。 將釋放這些結構所指向的配置記憶體。

</dd> <dt>

*RepairCount* 
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

[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

