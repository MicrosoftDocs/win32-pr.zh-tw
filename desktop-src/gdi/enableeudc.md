---
description: 此函式會啟用或停用 (EUDC) 的使用者自訂字元支援。
ms.assetid: 9e531d8c-6008-4189-ae25-cda707be5e2c
title: EnableEUDC 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnableEUDC
api_type:
- DllExport
api_location:
- Gdi32.dll
ms.openlocfilehash: 755ce2e0a659593b17487e86e28f5d454e48122c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972688"
---
# <a name="enableeudc-function"></a>EnableEUDC 函式

此函式會啟用或停用 (EUDC) 的使用者自訂字元支援。

## <a name="syntax"></a>語法


```C++
BOOL EnableEUDC(
  _In_ HDC BOOL fEnableEUDC
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fEnableEUDC* \[在\]
</dt> <dd>

將設定為 **TRUE** 以啟用 eudc 的布林值，若為 **FALSE** ，則停用 eudc。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回非零的值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

如果已停用 EUDC，嘗試顯示 EUDC 字元將會導致遺失或不正確的字元。

在多會話期間，此函數只會影響目前的會話。

建議您搭配 Windows XP SP2 或更新版本使用此函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 程式庫<br/>                  | <dl> <dt>Gdi32 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



 

 




