---
title: MsimtfIsWindowFiltered 函式
description: MsimtfIsWindowFiltered 函式會測試指定的視窗是否由 AIMM (Active Input Method Manager) 篩選。
ms.assetid: 1f5e98f1-3626-4aa5-b2da-b6bc48d02184
keywords:
- MsimtfIsWindowFiltered 函式文字服務架構
topic_type:
- apiref
api_name:
- MsimtfIsWindowFiltered
api_location:
- msimtf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06f3841ed5c0436d991d02291c1e395f42d6b31b66f442a3caac0b2062fc27db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476748"
---
# <a name="msimtfiswindowfiltered-function"></a>MsimtfIsWindowFiltered 函式

**MsimtfIsWindowFiltered** 函式會測試指定的視窗是否由 AIMM (Active Input Method Manager) 篩選。

## <a name="syntax"></a>語法


```C++
BOOL CALLBACK MsimtfIsWindowFiltered(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* \[在\]
</dt> <dd>

要測試的視窗控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值



| 傳回碼                                                                          | 描述                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**真**</dt> </dl>  | 如果使用 Active Input Method Manager 篩選此視窗。<br/>     |
| <dl> <dt>**假**</dt> </dl> | 如果這個視窗不是由作用中的輸入方法管理員進行篩選。<br/> |



 

## <a name="remarks"></a>備註

您可以使用 IActiveIMMApp：： FilterClientWindows 來篩選視窗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Msimtf.dll</dt> </dl> |



 

 





