---
title: 'CopyRootCauseInfo 函式 (Ndattributils) '
description: 建立 RootCauseInfo 結構的複本。
ms.assetid: 6bcd1341-657a-40c1-bebd-1c0f780ae337
keywords:
- CopyRootCauseInfo 函式 NDF
topic_type:
- apiref
api_name:
- CopyRootCauseInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98bb09fd9a61da536ddd17a4067838b33d4f86ffb8ee29fb404dc861220a5166
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685828"
---
# <a name="copyrootcauseinfo-function"></a>CopyRootCauseInfo 函式

**CopyRootCauseInfo** 函數會建立一份 [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)結構的複本。

## <a name="syntax"></a>語法


```C++
HRESULT CopyRootCauseInfo(
  _Out_       RootCauseInfo *Dest,
  _In_  const RootCauseInfo *Source
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*目的地* \[擴展\]
</dt> <dd>

類型： **[ **RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\***

要更新的結構。

</dd> <dt>

*來源* \[在\]
</dt> <dd>

Type： **Const [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \***

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

[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> </dl>

 

 





