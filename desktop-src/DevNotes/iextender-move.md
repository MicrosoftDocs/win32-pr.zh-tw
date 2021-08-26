---
description: 移動 MDIForm、表單或控制項。
ms.assetid: 963e6533-f571-4043-bdd8-2596df6b5b35
title: IExtender：： Move 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IExtender.Move
api_type:
- COM
api_location:
- Ole2disp.dll
- Oleaut32.dll
ms.openlocfilehash: 13002457952490588fa9e9ad40e7f66e7d31465b74f9757a3193ccaed1e8bf7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002098"
---
# <a name="iextendermove-method"></a>IExtender：： Move 方法

移動 MDIForm、表單或控制項。

## <a name="syntax"></a>語法


```C++
void Move(
  [in] object left,
  [in] object top,
  [in] object width,
  [in] object height
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*左方* \[在\]
</dt> <dd>

表單或控制項的左邊緣。

</dd> <dt>

*頂端* \[在\]
</dt> <dd>

表單或控制項的上邊緣。

</dd> <dt>

*寬度* \[在\]
</dt> <dd>

表單或控制項的寬度。

</dd> <dt>

*高度* \[在\]
</dt> <dd>

表單或控制項的高度。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ole2disp.dll;</dt><dt>Oleaut32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IExtender**](iextender.md)
</dt> </dl>

 

 




