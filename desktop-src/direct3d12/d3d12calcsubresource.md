---
title: 'D3D12CalcSubresource 函式 (D3dx12) '
description: 計算材質的 subresource 索引。
ms.assetid: 5C63A315-E21E-498B-A832-6BA2D17FF9A7
keywords:
- D3D12CalcSubresource 函式
topic_type:
- apiref
api_name:
- D3D12CalcSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e872d13ba5221ad50003d789b87f65fc64821dd0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986076"
---
# <a name="d3d12calcsubresource-function"></a>D3D12CalcSubresource 函式

計算材質的 subresource 索引。

## <a name="syntax"></a>語法


```C++
UINT inline D3D12CalcSubresource(
   UINT MipSlice,
   UINT ArraySlice,
   UINT PlaneSlice,
   UINT MipLevels,
   UINT ArraySize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*MipSlice* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

要定址的 mipmap 層級之以零為基底的索引;0表示第一個最詳細的 mipmap 層級。

</dd> <dt>

*ArraySlice* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

要定址的陣列層級之以零為基底的索引;針對 volume (3D) 材質，一律使用0。

</dd> <dt>

*PlaneSlice* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

要定址之平面層級的以零為基底的索引。

</dd> <dt>

*MipLevels* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

資源中的 mipmap 層級數目。

</dd> <dt>

[陣列大小] 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

陣列中的項目數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

等於 MipSlice + (ArraySlice \* MipLevels) 的索引。

## <a name="remarks"></a>備註

緩衝區是非結構化的資源，因此定義為包含單一 subresource。 採用緩衝區的 Api 不需要 subresource 索引。 另一方面，材質高度結構化。 每個材質物件都可以包含一或多個子資源，視陣列大小和 mipmap 層級數目而定。

針對 volume (3D) 材質，指定 mipmap 層級的所有配量都是單一 subresource 索引。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx12。h</dt> </dl>  |
| 程式庫<br/> | <dl> <dt>D3D12 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3D12 的 Helper 函式](helper-functions-for-d3d12.md)
</dt> <dt>

[子資源](subresources.md)
</dt> </dl>

 

