---
description: 設定指定動畫播放軌的混合事件索引鍵。
ms.assetid: 2023d566-1de5-465a-ad6f-04a78ac01c33
title: 'ID3DXAnimationController：： KeyPriorityBlend 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31778da9b26ddd79b5f05c69c822ed62a5b5281e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322680"
---
# <a name="id3dxanimationcontrollerkeypriorityblend-method"></a>ID3DXAnimationController：： KeyPriorityBlend 方法

設定指定動畫播放軌的混合事件索引鍵。

## <a name="syntax"></a>語法


```C++
D3DXEVENTHANDLE KeyPriorityBlend(
  [in] FLOAT               NewBlendWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NewBlendWeight* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

介於0和1之間的數位，用來結合追蹤。

</dd> <dt>

*StartTime* \[在\]
</dt> <dd>

類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**

開始 blend 的全球時間。

</dd> <dt>

*持續時間* \[在\]
</dt> <dd>

類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**

Blend 的全球時間持續時間。

</dd> <dt>

*轉換* \[在\]
</dt> <dd>

類型： **[ **D3DXTRANSITION \_ 類型**](./d3dxtransition-type.md)**

指定用於 blend 期間的轉換類型。 請參閱 [**D3DXTRANSITION \_ 類型**](./d3dxtransition-type.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

優先權 blend 事件的事件控制碼。 如果有一或多個輸入參數無效，或沒有可用的事件，則會傳回 **Null** 。

## <a name="remarks"></a>備註

動畫控制器會以三個階段來混合：低優先順序的軌跡先混合，高優先順序的軌跡則是混合的第二個，然後兩者的結果都是混合的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**SetPriorityBlend**](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 
