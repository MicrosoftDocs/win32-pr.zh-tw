---
description: 初始化 Aux \_ klib 程式庫。
ms.assetid: 516bb359-d3a3-415b-90af-09e544366a12
title: 'AuxKlibInitialize function (Aux \_ klib .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibInitialize
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: f35d2d17d581d17a6d89a7bc10d185a67a5fb0b695a29492922f5950241f2ab7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654878"
---
# <a name="auxklibinitialize-function"></a>AuxKlibInitialize 函式

初始化 Aux \_ klib 程式庫。 必須先呼叫此函式，才能呼叫程式庫中的任何其他函式。

## <a name="syntax"></a>語法


```C++
NTSTATUS _stdcall AuxKlibInitialize(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「狀態 \_ 成功」。

如果函式失敗，則傳回值可以是在 WDK 中定義的其中一個狀態碼，也就是在 WDK 中可用。

## <a name="remarks"></a>備註

您可以從 [這裡](https://www.microsoft.com/?ref=go)下載可執行此 API 的物件程式庫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|------------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows輔助 API 程式庫1.0 版或更新版本<br/>                            |
| 標頭<br/>          | <dl> <dt>Aux \_ klib。h</dt> </dl>   |
| 程式庫<br/>         | <dl> <dt>Aux \_ klib .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AuxKlibQueryModuleInformation**](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




