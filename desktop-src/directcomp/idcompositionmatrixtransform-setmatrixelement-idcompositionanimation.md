---
title: IDCompositionMatrixTransform SetMatrixElement (int，int，IDCompositionAnimation ) 方法
description: 將這個2D 轉換之矩陣的某個元素值繪製成動畫。
ms.assetid: 16A9E136-5F0C-4F34-A127-BF06C4530499
keywords:
- SetMatrixElement 方法 DirectComposition
- SetMatrixElement 方法 DirectComposition、IDCompositionMatrixTransform 介面
- IDCompositionMatrixTransform 介面 DirectComposition，SetMatrixElement 方法
topic_type:
- apiref
api_name:
- IDCompositionMatrixTransform.SetMatrixElement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b4bf2a43e762b85b8b8cfd0c15468b3dc438221
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376181"
---
# <a name="idcompositionmatrixtransformsetmatrixelementint-int-idcompositionanimation-method"></a>IDCompositionMatrixTransform：： SetMatrixElement (int，int，IDCompositionAnimation \*) 方法

將這個2D 轉換之矩陣的某個元素值繪製成動畫。

## <a name="syntax"></a>語法


```C++
HRESULT SetMatrixElement(
  [in] int                    row,
  [in] int                    column,
  [in] IDCompositionAnimation *animation
);
```



## <a name="parameters"></a>參數

<dl> <dt>

資料 *列* \[在\]
</dt> <dd>

要變更之元素的資料列索引。 此值必須介於0和2（含）之間。

</dd> <dt>

資料 *行* \[在\]
</dt> <dd>

要變更之元素的資料行索引。 此值必須介於0和1（含）之間。

</dd> <dt>

*動畫* \[在\]
</dt> <dd>

表示指定專案的值如何隨著時間而改變的動畫。 此參數不得為 Null。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回 S \_ OK。 否則，它會傳回 **HRESULT** 錯誤碼。 如需錯誤碼清單，請參閱 [DirectComposition 錯誤碼](directcomposition-error-codes.md) 。

## <a name="remarks"></a>備註

這個方法會複製指定的動畫。 如果在呼叫這個方法之後變更了 *動畫* 參數所參考的物件，除非再次呼叫這個方法，否則變更不會影響元素。 如果專案先前是以動畫顯示，呼叫這個方法會以新動畫取代先前的動畫。

如果 *動畫* 是不正確指標，或與受影響的轉換不是由相同的 [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) 介面所建立，則這個方法會失敗。 介面不能是自訂的實值;只有 Microsoft DirectComposition 建立的介面可以搭配此方法使用。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> </dl>

 

 