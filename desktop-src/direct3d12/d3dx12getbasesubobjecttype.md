---
title: 'D3DX12GetBaseSubobjectType 函式 (D3dx12) '
description: 傳回子物件類型，這個物件對應至傳入之子物件類型的基類。
ms.assetid: 3744B042-094C-4EA4-8185-A018B728D843
keywords:
- D3DX12GetBaseSubobjectType 函式
topic_type:
- apiref
api_name:
- D3DX12GetBaseSubobjectType
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b39f1c61be682d55512772bef1258aecdb009a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988168"
---
# <a name="d3dx12getbasesubobjecttype-function"></a>D3DX12GetBaseSubobjectType 函式

傳回子物件類型，這個物件對應至傳入之子物件類型的基類。

## <a name="syntax"></a>語法


```C++
D3D12_PIPELINE_STATE_SUBOBJECT_TYPE inline D3DX12GetBaseSubobjectType(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE SubobjectType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SubobjectType* 
</dt> <dd>

類型： **D3D12 \_ 管線 \_ 狀態 \_ \_** 子物件類型

列舉值，指定您感興趣的子物件類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **D3D12 \_ 管線 \_ 狀態 \_ \_** 子物件類型

如果 *SubobjectType* 對應至衍生自另一個子物件資料類型的子物件資料類型，則會傳回基底子物件資料類型的子物件類型。否則，會傳回傳入的子物件類型。 例如，如果傳入 **D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型 \_ 深度 \_ STENCIL1** ，則會傳回 **D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型 \_ 深度 \_** 樣板。

## <a name="remarks"></a>備註

## <a name="requirements"></a>需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx12。h</dt> </dl>  |
| 程式庫<br/> | <dl> <dt>D3D12 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3D12 的 Helper 函式](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





