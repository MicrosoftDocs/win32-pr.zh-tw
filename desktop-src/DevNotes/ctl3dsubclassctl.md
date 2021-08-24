---
description: 子類別化個別控制項，除非控制項出現在對話方塊中。
ms.assetid: 07a2bce1-4c69-4f8d-bb24-b17351f5e771
title: Ctl3dSubclassCtl 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: f1d25bdc189ad80f1976ee76cc7f9909d099f34c8a88b83771ebf3f297c78934
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654478"
---
# <a name="ctl3dsubclassctl-function"></a>Ctl3dSubclassCtl 函式

子類別化個別控制項，除非控制項出現在對話方塊中。

## <a name="syntax"></a>語法


```C++
BOOL Ctl3dSubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* 
</dt> <dd>

控制項視窗的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功將控制項子類別化，則傳回 **TRUE** ;否則，它會傳回 **FALSE**。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Ctl3dUnsubclassCtl**](ctl3dunsubclassctl.md)
</dt> </dl>

 

 
