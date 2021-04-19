---
title: 'CD3DX12_SHADER_BYTECODE 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 著色器位元組程式碼 \_ 結構。
ms.assetid: 09CEFCCE-C499-493D-ACDE-806E09995315
keywords:
- CD3DX12_SHADER_BYTECODE 結構
topic_type:
- apiref
api_name:
- CD3DX12_SHADER_BYTECODE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227c18913492d6533b08f49f5761fab1b93e97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106979870"
---
# <a name="cd3dx12_shader_bytecode-structure"></a>CD3DX12 \_ 著色器 \_ 位元組位元組結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 著色器 \_ 位元組**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) 程式碼結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_SHADER_BYTECODE  : public D3D12_SHADER_BYTECODE{
   CD3DX12_SHADER_BYTECODE();
   explicit CD3DX12_SHADER_BYTECODE(const D3D12_SHADER_BYTECODE &o);
   CD3DX12_SHADER_BYTECODE(ID3DBlob* pShaderBlob);
   CD3DX12_SHADER_BYTECODE(const void* _pShaderBytecode, SIZE_T bytecodeLength);
   operator const D3D12_SHADER_BYTECODE&() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 著色器 \_ 位元組 ()**
</dt> <dd>

建立 CD3DX12 著色器位元組程式碼的新、未初始化的實例 \_ \_ 。

</dd> <dt>

**明確的 CD3DX12 \_ 著色器 \_ 位元組 (const D3D12 \_ 著色器 \_ 位元組 &o)**
</dt> <dd>

建立 CD3DX12 著色器位元組程式碼的新實例 \_ \_ ，並以另一個 [**D3D12 \_ 著色器 \_ 位元組**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) 程式碼結構的內容進行初始化。

</dd> <dt>

**CD3DX12 \_ 著色器 \_ 位元組 (ID3DBlob \* pShaderBlob)**
</dt> <dd>

建立 CD3DX12 \_ 著色器位元組程式碼的新實例 \_ ，並初始化下列參數：

[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) \*pShaderBlob

</dd> <dt>

**CD3DX12 \_ 著色器 \_ 位元組空間 (const void \* \_ PShaderBytecode，SIZE \_ T bytecodeLength)**
</dt> <dd>

建立 CD3DX12 \_ 著色器位元組程式碼的新實例 \_ ，並初始化下列參數：

void \* \_ pShaderBytecode

大小 \_ T bytecodeLength

</dd> <dt>

**運算子 const D3D12 \_ 著色器 \_ 位元組& () const**
</dt> <dd>

針對父結構類型定義 & 的傳址運算子。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 著色器 \_ 位元組碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

