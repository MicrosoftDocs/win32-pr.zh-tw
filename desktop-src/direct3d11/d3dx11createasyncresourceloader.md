---
title: 'D3DX11CreateAsyncResourceLoader 函式 (D3DX11async) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。 建立異步資源載入器。
ms.assetid: b49900a1-866d-4a4a-bf3a-2deb9ce4a208
keywords:
- D3DX11CreateAsyncResourceLoader 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncResourceLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7dd914250f3d47b80643d88ef055681f2e8a9f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035396"
---
# <a name="d3dx11createasyncresourceloader-function"></a>D3DX11CreateAsyncResourceLoader 函式

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。

 

建立異步資源載入器。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX11CreateAsyncResourceLoader(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSrcModule* \[在\]
</dt> <dd>

類型： **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**

資源模組的控制碼。 使用 [GetModuleHandle 函數](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) 來取得控制碼。

</dd> <dt>

*pSrcResource* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

HSrcModule 中資源的名稱。 如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。 否則，資料型別會解析為 LPCSTR。

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

針對 Windows Store 應用程式， (的 DirectX 範例，例如 [Direct3D 教學課程範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) 包含使用 Windows 執行階段非同步程式設計模型 ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) 的 **BasicLoader** 模組。

針對 Win32 傳統型應用程式，您可以使用 [並行執行階段](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) 來執行類似于 Windows 執行階段非同步程式設計模型的內容。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX11async。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX11 .lib</dt> </dl>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 函式](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

