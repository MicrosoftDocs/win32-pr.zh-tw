---
title: 'D3DX11SHProjectCubeMap 函式 (D3DX11tex) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用這個函式，而是使用球形諧波數學程式庫 SHProjectCubeMap。
ms.assetid: 58c741a3-dd5d-4b18-b257-5e85a9b799fd
keywords:
- D3DX11SHProjectCubeMap 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SHProjectCubeMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf773c00a649e6ace065fcf552358fbf5eeb19c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992259"
---
# <a name="d3dx11shprojectcubemap-function"></a>D3DX11SHProjectCubeMap 函式

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。

 

> [!Note]  
> 我們建議您不要使用這個函數，而是使用 [球形諧波數學](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) 程式庫 **SHProjectCubeMap**。

 

將 cube 地圖中表示的函式投射到球面諧波。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX11SHProjectCubeMap(
   ID3D11DeviceContext *pContext,
   UINT                Order,
   ID3D11Texture2D     *pCubeMap,
   FLOAT               *pROut,
   FLOAT               *pGOut,
   FLOAT               *pBOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pContext* 
</dt> <dd>

類型： **[ **>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

[**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)物件的指標。

</dd> <dt>

*順序* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

SH 評估的順序會產生順序 ^ 2 係數，其度為順序-1。 有效範圍介於2到6之間。

</dd> <dt>

*pCubeMap* 
</dt> <dd>

類型： **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)的指標，代表即將投射到球面諧波的立方體貼圖。

</dd> <dt>

*pROut* 
</dt> <dd>

類型： **[ **FLOAT**](/windows/desktop/WinProg/windows-data-types)\***

紅色的輸出 SH 向量。

</dd> <dt>

*pGOut* 
</dt> <dd>

類型： **[ **FLOAT**](/windows/desktop/WinProg/windows-data-types)\***

綠色的輸出 SH 向量。

</dd> <dt>

*pBOut* 
</dt> <dd>

類型： **[ **FLOAT**](/windows/desktop/WinProg/windows-data-types)\***

藍色的輸出 SH 向量。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX11tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX11 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 函式](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

