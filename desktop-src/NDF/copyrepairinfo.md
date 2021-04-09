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
ms.openlocfilehash: 7a24d15ec5a8a69b3c8c40700273ebcb6f32bcfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934157"
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

類型： **[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _

要更新的結構。

</dd> <dt>

_Source * \[ in\]
</dt> <dd>

類型： **Const [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _

要複製的現有結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： _ *HRESULT**

可能的傳回值包括（但不限於）下列各項。



| 傳回碼                                                                                   | Description                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業成功。<br/>                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 未正確提供一或多個參數。<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 沒有足夠的記憶體可完成此作業。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>Ndattributils。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> </dl>

 

 





