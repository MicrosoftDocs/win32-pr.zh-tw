---
description: D3DXMATRIXA16 結構 (D3DX10Math .h) -包含方法和運算子多載的4x4、16位元組對齊矩陣。
ms.assetid: d9e9c1cc-7555-4011-a4b4-8cce20404841
title: 'D3DXMATRIXA16 結構 (D3DX10Math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATRIXA16
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 4953b51cdd09cdbcac4855bd423ce37dda5b979e06153589b5b2ded21004b3ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853398"
---
# <a name="d3dxmatrixa16-structure-d3dx10mathh"></a>D3DXMATRIXA16 結構 (D3DX10Math .h) 

4x4、16位元組對齊的矩陣，其中包含方法和運算子多載。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
```



## <a name="members"></a>成員

<dl> <dt>

**\_Ij**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

矩陣的 (i，j) 元件，其中 i 是資料列編號，而 j 是資料行編號。 例如， \_ 34 表示與 \[ ₃₄相同 \] ，第三個數據列和第四個數據行中的元件。

</dd> </dl>

## <a name="remarks"></a>備註

D3DX 數學函式使用時，16位元組對齊的矩陣已經過優化，以改善 Intel Pentium 4 處理器的效能。 矩陣的對齊方式與它們的建立位置無關：在程式堆疊上、堆積或全域範圍中。 您可以使用 \_ \_ declspec (對齊 (16) ) 來完成對齊，這項功能僅適用于 Visual C++ .net，而且只有在安裝處理器套件時才會使用 Visual C++ 6.0。 可惜的是，沒有任何方法可以偵測處理器套件，因此預設只會根據 Visual C++ .NET 來開啟位元組對齊。

向量和四元數在 D3DX 中不是位元組對齊。 搭配使用向量和四元數與 D3DX 數學函式時，請使用 \_ declspec (對齊 (16) ) 來產生位元組對齊的向量和四元數，因為它們的執行效能大幅提升。 Declspec 的定義 \_ 如下所示。


```
#define D3DX_ALIGN16 __declspec(align(16))
```



其他編譯器會將 **D3DXMATRIXA16** 解讀為 [**D3DXMATRIX**](d3d10-d3dxmatrix.md)。 在未實際對齊矩陣的編譯器上使用此結構可能會造成問題，因為它不會公開會忽略對齊的 bug。 例如，如果 **D3DXMATRIXA16** 物件位於結構或類別內，則可能會使用緊密封裝完成 [memcpy](https://msdn2.microsoft.com/library/dswaw1wk(vs.71).aspx) ， (忽略16位元組界限) 。 如果編譯器在一段時間加入矩陣時，這會造成組建中斷。

### <a name="d3dxmatrixa16-extensions"></a>D3DXMATRIXA16 延伸模組

**D3DXMATRIXA16** 具有下列 c + + 擴充功能。


```
typedef struct _D3DXMATRIXA16 : public D3DXMATRIX
{
    _D3DXMATRIXA16();
    _D3DXMATRIXA16( CONST FLOAT * f);
    _D3DXMATRIXA16( CONST D3DMATRIX& m);
    _D3DXMATRIXA16( FLOAT _11, FLOAT _12, FLOAT _13, FLOAT _14,
                    FLOAT _21, FLOAT _22, FLOAT _23, FLOAT _24,
                    FLOAT _31, FLOAT _32, FLOAT _33, FLOAT _34,
                    FLOAT _41, FLOAT _42, FLOAT _43, FLOAT _44 );
    void* operator new(size_t s);
    void* operator new[](size_t s);

    // The two operators below are not virtual operators. If you cast
    //   to D3DXMATRIX, do not delete using them
    void operator delete(void* p);
    void operator delete[](void* p);

    struct _D3DXMATRIXA16& operator=(CONST D3DXMATRIX& rhs);
} _D3DXMATRIXA16;

typedef D3DX_ALIGN16 _D3DXMATRIXA16 D3DXMATRIXA16, *LPD3DXMATRIXA16;
        
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
