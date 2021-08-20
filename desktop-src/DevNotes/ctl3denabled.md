---
description: 驗證控制項是否可以使用3D 效果。
ms.assetid: fb7b892f-2580-41ac-b2ef-938da3cc1dc2
title: Ctl3dEnabled 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dEnabled
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 0d8a234736631517a0e77f5ab23f07688e3d80aa4c8b74a3b2ee51351beece90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654588"
---
# <a name="ctl3denabled-function"></a>Ctl3dEnabled 函式

驗證控制項是否可以使用3D 效果。

## <a name="syntax"></a>語法


```C++
BOOL Ctl3dEnabled(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

如果控制項可以使用3D 效果，則傳回 **TRUE** ;否則，它會傳回 **FALSE**。

## <a name="remarks"></a>備註

在 Windows 4.0 或更新版本中， **Ctl3dEnabled** 和 [**Ctl3dRegister**](ctl3dregister.md)會傳回 **FALSE**。

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
