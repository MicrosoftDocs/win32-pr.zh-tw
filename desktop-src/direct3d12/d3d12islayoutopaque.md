---
title: 'D3D12IsLayoutOpaque 函式 (D3dx12) '
description: 指出版面配置是否為不透明。
ms.assetid: 43B46A18-A725-4999-BD97-108032793A95
keywords:
- D3D12IsLayoutOpaque 函式
topic_type:
- apiref
api_name:
- D3D12IsLayoutOpaque
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971c44688e57dd1081d33a4a077a8dcadcb89abf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000221"
---
# <a name="d3d12islayoutopaque-function"></a>D3D12IsLayoutOpaque 函式

指出版面配置是否為不透明。

## <a name="syntax"></a>語法


```C++
bool inline D3D12IsLayoutOpaque(
   D3D12_TEXTURE_LAYOUT Layout
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*版面配置* 
</dt> <dd>

類型： **[ **D3D12 \_ 材質 \_ 版面** 配置](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)**

要檢查的版面配置，作為 [**D3D12 \_ 材質 \_ 版面**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)配置。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **bool**

指出配置是否不透明的 **布林** 值。 如果配置是 D3D12 \_ 材質配置 \_ \_ 未知或 D3D12 \_ 材質配置 \_ \_ 64kb \_ 未定義 \_ SWIZZLE，則為不透明的版面配置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx12。h</dt> </dl>  |
| 程式庫<br/> | <dl> <dt>D3D12 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3D12 的 Helper 函式](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





