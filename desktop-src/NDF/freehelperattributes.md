---
title: 'FreeHelperAttributes 函式 (Ndattributils) '
description: 將內部配置的記憶體解除配置至 HELPER \_ 屬性結構的陣列。
ms.assetid: d973bdb9-c1d1-4cea-bcc6-98671349413f
keywords:
- FreeHelperAttributes 函式 NDF
topic_type:
- apiref
api_name:
- FreeHelperAttributes
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb16ad2d7f505a90d806e3f6a155f2c20affce2c71267316c2278e2320c371b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802428"
---
# <a name="freehelperattributes-function"></a>FreeHelperAttributes 函式

**FreeHelperAttributes** 函式會將內部配置的記憶體解除配置至 [**HELPER \_ 屬性**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)結構的陣列。 此函數會呼叫 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) 來解除配置記憶體。

## <a name="syntax"></a>語法


```C++
VOID FreeHelperAttributes(
  _In_ HELPER_ATTRIBUTE *pInfo,
       ULONG            HelperAttributeCount,
       BOOL             bFreePointer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pInfo* \[在\]
</dt> <dd>

類型： **[ **HELPER \_ 屬性**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\***

結構的陣列。 將釋放這些結構所指向的配置記憶體。

</dd> <dt>

*HelperAttributeCount* 
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

[**HELPER \_ 屬性**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

