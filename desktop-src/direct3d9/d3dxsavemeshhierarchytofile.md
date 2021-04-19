---
description: 建立 x.x 檔案，並在其中儲存網格階層和對應的動畫。
ms.assetid: 803926fe-8cb7-422a-9920-56f7d0b0d0ea
title: 'D3DXSaveMeshHierarchyToFile 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshHierarchyToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2de65f9bc2f9e40a5bc07c6f0b4d00112f0df21
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985530"
---
# <a name="d3dxsavemeshhierarchytofile-function"></a>D3DXSaveMeshHierarchyToFile 函式

建立 x.x 檔案，並在其中儲存網格階層和對應的動畫。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXSaveMeshHierarchyToFile(
  _In_       LPCSTR                    pFilename,
  _In_       DWORD                     XFormat,
  _In_ const D3DXFRAME                 *pFrameRoot,
  _In_       LPD3DXANIMATIONCONTROLLER pAnimController,
  _In_       LPD3DXSAVEUSERDATA        pUserDataSaver
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFilename* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

字串的指標，這個字串會指定識別已儲存網格的. x 檔案名。 如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。 否則，字串資料類型會解析為 LPCSTR。 請參閱＜備註＞。

</dd> <dt>

*XFormat* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

. X 檔案的格式 (文字或二進位檔案、壓縮或不) 。 請參閱 D3DXF \_ >fileformat。 您 \_ \_ 可以將 D3DXF >fileformat 壓縮 (使用邏輯 OR) 搭配 D3DXF \_ >FILEFORMAT \_ BINARY 或 D3DXF \_ >fileformat \_ 文字旗標，以縮減輸出檔案大小。

</dd> <dt>

*pFrameRoot* \[在\]
</dt> <dd>

Type： **Const [**D3DXFRAME**](d3dxframe.md) \***

要儲存之階層的根節點。 請參閱 [**D3DXFRAME**](d3dxframe.md)。

</dd> <dt>

*pAnimController* \[在\]
</dt> <dd>

類型： **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**

具有要儲存之動畫集的動畫控制器。 請參閱 [**ID3DXAnimationController**](id3dxanimationcontroller.md)。

</dd> <dt>

*pUserDataSaver* \[在\]
</dt> <dd>

類型： **[ **LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**

應用程式提供的介面，可儲存使用者資料。 請參閱 [**ID3DXSaveUserData**](id3dxsaveuserdata.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是： D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

編譯器設定也會決定函式版本。 如果已定義 Unicode，函式呼叫會解析為 D3DXSaveMeshHierarchyToFileW。 否則，函式呼叫會解析為 D3DXSaveMeshHierarchyToFileA。

此函數不會儲存壓縮的動畫集。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[動畫函數](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> <dt>

[X 檔案參考](dx9-graphics-reference-d3dx-x-file.md)
</dt> </dl>

 

 
