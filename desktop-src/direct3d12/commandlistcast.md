---
title: 'CommandListCast 函式 (D3dx12) '
description: 這個函式範本會將任何命令清單的常數指標轉換成 ID3D12CommandList 的 const 指標。
ms.assetid: 63719AA1-2119-456C-9D23-13933D38AFA9
keywords:
- CommandListCast 函式
topic_type:
- apiref
api_name:
- CommandListCast
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a740258f74975fecac3e1a4df2412f1fae92f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985907"
---
# <a name="commandlistcast-function"></a>CommandListCast 函式

這個函式範本會將任何命令清單的常數指標轉換成 ID3D12CommandList 的 const 指標。

這項轉換適用于將強型別命令清單指標傳遞至 [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)。

## <a name="syntax"></a>語法


```C++
ID3D12CommandList * const * inline CommandListCast(
   t_CommandListType * const * pp
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Pp* 
</dt> <dd>

類型： **t \_ CommandListType \* const \***

要轉換的強型別命令清單。

範本引數 **t \_ CommandListType** 指定任何強型別命令清單物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **ID3D12CommandList \* const \***

強型別命令清單重新解譯為 [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)。

## <a name="remarks"></a>備註

CommandListCast 會執行 **重新解譯 \_ 轉換**。 只要遵守命令清單的 const 性質，轉換就有效。

CommandListCast 函式定義如下：


```C++
template <typename t_CommandListType>
inline ID3D12CommandList * const * CommandListCast(t_CommandListType * const * pp)
{
    return reinterpret_cast<ID3D12CommandList * const *>(pp);
}
          
```



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

 

 





