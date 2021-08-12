---
title: 'CopyRepairInfo 函式 (Ndattributils) '
description: 建立 RepairInfo 結構的複本。
ms.assetid: a1147ce6-9a90-4a46-8fe4-da3353391a13
keywords:
- CopyRepairInfo 函式 NDF
topic_type:
- apiref
api_name:
- CopyRepairInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e40a054df2b16684840f22295f0c26de6029ef150a97ca8839c98d94713ab030
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620433"
---
# <a name="copyrepairinfo-function"></a>CopyRepairInfo 函式

**CopyRepairInfo** 函數會建立一份 [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)結構的複本。

## <a name="syntax"></a>語法


```C++
HRESULT CopyRepairInfo(
  _Out_       RepairInfo *Dest,
  _In_  const RepairInfo *Source
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*目的地* \[擴展\]
</dt> <dd>

類型： **[ **RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\***

要更新的結構。

</dd> <dt>

*來源* \[在\]
</dt> <dd>

Type： **Const [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \***

要複製的現有結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

可能的傳回值包括（但不限於）下列各項。



| 傳回碼                                                                                   | 描述                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業成功。<br/>                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 未正確提供一或多個參數。<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 沒有足夠的記憶體可完成此作業。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>Ndattributils。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> </dl>

 

 





