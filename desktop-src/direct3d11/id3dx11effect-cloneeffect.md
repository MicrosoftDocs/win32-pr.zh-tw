---
title: 'ID3DX11Effect CloneEffect 方法 (D3dx11effect .h) '
description: 建立效果介面的複本。
ms.assetid: 98cc8e25-38c5-4b87-99eb-39d2edd9053c
keywords:
- CloneEffect 方法 Direct3D 11
- CloneEffect 方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，CloneEffect 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.CloneEffect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d9fa68fe05674573468eb684d8149d8dae45e540572f4d777bb860755c60e0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124523"
---
# <a name="id3dx11effectcloneeffect-method"></a>ID3DX11Effect：： CloneEffect 方法

建立效果介面的複本。

## <a name="syntax"></a>語法


```C++
HRESULT CloneEffect(
   UINT          Flags,
   ID3DX11Effect **ppClonedEffect
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*旗標* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

影響建立複製效果的旗標。 可以是0或下列其中一個值。



| 旗標                                    | 描述                                                                                                                                      |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DX11 \_ 效果 \_ 複製 \_ 強制 \_ NONSINGLE | 忽略 cbuffers 上的所有 "single" 限定詞。 所有 cbuffers 都將會在複製的效果中建立自己的 [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)。 |



 

</dd> <dt>

*ppClonedEffect* 
</dt> <dd>

類型： **[ **ID3DX11Effect**](id3dx11effect.md)\*\***

將設定為效果複本之 [**ID3DX11Effect**](id3dx11effect.md) 指標的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。

## <a name="remarks"></a>備註

> [!Note]  
> DirectX SDK 不提供任何已編譯的二進位檔來產生效果。 您必須使用效果11來源來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx11effect。h</dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

