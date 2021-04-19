---
description: 從 DLL 進入點呼叫之函式的指標。
ms.assetid: 30196657-38ab-42ca-b673-b0894999e566
title: 'LPFNInitRoutine 函式指標 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNInitRoutine
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: 375660399180196e2434030ea7551733affc4062
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995282"
---
# <a name="lpfninitroutine-function-pointer"></a>LPFNInitRoutine 函式指標

從 DLL 進入點呼叫之函式的指標。

## <a name="syntax"></a>語法


```C++
typedef void ( CALLBACK *LPFNInitRoutine)(
         BOOL  bLoading,
   const CLSID *rclsid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bLoading* 
</dt> <dd>

載入 DLL 時 **為 TRUE** ，卸載 dll 時為 **FALSE** 。

</dd> <dt>

*rclsid* 
</dt> <dd>

物件之 CLISD 的指標，在 [**CFactoryTemplate：： m \_ ClsID**](cfactorytemplate-m-clsid.md) 成員變數中指定。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個函式指標不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Combase (包含： .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CFactoryTemplate 類別**](cfactorytemplate.md)
</dt> </dl>

 

 




