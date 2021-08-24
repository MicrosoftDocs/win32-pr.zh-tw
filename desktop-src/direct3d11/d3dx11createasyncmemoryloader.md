---
title: 'D3DX11CreateAsyncMemoryLoader 函式 (D3DX11async) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。 建立異步記憶體載入器。
ms.assetid: 0bf1e6a2-a968-4644-a7b4-e847ed4f7450
keywords:
- D3DX11CreateAsyncMemoryLoader 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncMemoryLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c65f1f094337aed5fee6b026896bba98c151576077c4d89ad750486e0fa48cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124873"
---
# <a name="d3dx11createasyncmemoryloader-function"></a>D3DX11CreateAsyncMemoryLoader 函式

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，不支援 Windows Store 應用程式。 請參閱＜備註＞。

 

建立異步記憶體載入器。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX11CreateAsyncMemoryLoader(
  _In_  LPCVOID           pData,
  _In_  SIZE_T            cbData,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*.pdata* \[在\]
</dt> <dd>

類型： **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**

資料的指標。

</dd> <dt>

*cbData* \[在\]
</dt> <dd>

類型： **[**大小 \_ T**](/windows/desktop/WinProg/windows-data-types)**

資料的大小。

</dd> <dt>

*ppDataLoader* \[擴展\]
</dt> <dd>

類型： **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***

非同步資料載入器指標的位址 (參閱 [**ID3DX11DataLoader 介面**](id3dx11dataloader.md)) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="remarks"></a>備註

D3DX 10 和 D3DX 11 以外的非同步載入器不會執行。

針對 Windows Store 應用程式，DirectX 範例 (例如， [Direct3D 教學課程範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) 包含使用 Windows 執行階段非同步程式設計模型 ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) 的 **BasicLoader** 模組。

針對 Win32 傳統型應用程式，您可以使用[並行執行階段](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100))來執行類似于 Windows 執行階段非同步程式設計模型的內容。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX11async。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX11 .lib</dt> </dl>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 函式](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

