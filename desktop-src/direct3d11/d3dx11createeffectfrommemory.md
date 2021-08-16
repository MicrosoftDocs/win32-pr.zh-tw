---
title: 'D3DX11CreateEffectFromMemory 函式 (D3dx11effect) '
description: 從二進位效果或檔案建立效果。
ms.assetid: 4aa65efb-4c6b-4faf-b48f-01329bdff6cd
keywords:
- D3DX11CreateEffectFromMemory 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateEffectFromMemory
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99cdef28acae9419a5b597d5be1703ea9e866d521d7f94bb330b151abc74842
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124803"
---
# <a name="d3dx11createeffectfrommemory-function"></a>D3DX11CreateEffectFromMemory 函式

從二進位效果或檔案建立效果。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX11CreateEffectFromMemory(
   void          *pData,
   SIZE_T        DataLength,
   UINT          FXFlags,
   ID3D11Device  *pDevice,
   ID3DX11Effect **ppEffect
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*.Pdata* 
</dt> <dd>

類型： **void \***

已編譯之效果資料的 Blob。

</dd> <dt>

*DataLength* 
</dt> <dd>

類型： **[**大小 \_ T**](/windows/desktop/WinProg/windows-data-types)**

資料 blob 的長度。

</dd> <dt>

*FXFlags* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

沒有效果旗標存在。 設定為零。

</dd> <dt>

*pDevice* 
</dt> <dd>

類型： **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

要在其上建立效果資源之 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 的指標。

</dd> <dt>

*ppEffect* 
</dt> <dd>

類型： **[ **ID3DX11Effect**](id3dx11effect.md)\*\***

新建立之 [**ID3DX11Effect**](id3dx11effect.md) 介面的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="remarks"></a>備註

> [!Note]  
> 您必須使用 [效果11來源](https://github.com/Microsoft/FX11) 來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx11effect。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果11函數](d3d11-graphics-reference-effects11-functions.md)
</dt> </dl>

 

