---
title: 'D3DX11GetImageInfoFromResource 函式 (D3DX11tex) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用此函式，而是使用資源函式，然後使用 DirectXTex 程式庫 (工具) 、LoadFromXXXMemory (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。 抓取資源中指定影像的相關資訊。
ms.assetid: e4752eb3-38d5-4922-b3c8-5fdcd0cc0610
keywords:
- D3DX11GetImageInfoFromResource 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ada8118dac3e39f9f91012bb3ec681db7b156540cffae0fb7c0f1a7bc1819b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535953"
---
# <a name="d3dx11getimageinfofromresource-function"></a>D3DX11GetImageInfoFromResource 函式

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，不支援 Windows Store 應用程式。

 

> [!Note]  
> 我們建議您不要使用此函式，而是使用 [資源](/windows/desktop/menurc/resources-functions)函式，然後使用 [DirectXTex](https://github.com/Microsoft/DirectXTex) 程式庫 (工具) 、 **LOADFROMXXXMEMORY** (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。

 

抓取資源中指定影像的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX11GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSrcModule* \[在\]
</dt> <dd>

類型： **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**

載入資源的模組。 將此參數設定為 **Null** ，以指定與作業系統用來建立目前進程的映射相關聯的模組。

</dd> <dt>

*pSrcResource* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

指定檔案名之字串的指標。 如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。 否則，資料型別會解析為 LPCSTR。 請參閱＜備註＞。

</dd> <dt>

*pPump* \[在\]
</dt> <dd>

類型： **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

選擇性的執行緒抽取，可用來以非同步方式載入資訊。 可以是 **Null**。 請參閱 [**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)。

</dd> <dt>

*pSrcInfo* \[在\]
</dt> <dd>

類型： **[ **D3DX11 \_ 影像 \_ 資訊**](d3dx11-image-info.md)\***

D3DX11 影像資訊結構的指標，此 \_ \_ 結構會填入原始程式檔中的資料描述。

</dd> <dt>

*pHResult* \[擴展\]
</dt> <dd>

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

傳回值的指標。 可能是 **Null**。 如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL

## <a name="remarks"></a>備註

編譯器設定也會決定函式版本。 如果已定義 Unicode，函式呼叫會解析為 **D3DX11GetImageInfoFromResourceW**。 否則，函式呼叫會解析為 **D3DX11GetImageInfoFromResourceA** ，因為正在使用 ANSI 字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX11tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX11 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 函式](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

