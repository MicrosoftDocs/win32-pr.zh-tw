---
description: D3DX10GetImageInfoFromResource 函式-取得資源中指定影像的相關資訊。
ms.assetid: d413d887-77e0-43cc-a30e-67c3c40772f0
title: 'D3DX10GetImageInfoFromResource 函式 (D3DX10Tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: af4dea966b63549c4bcef913175c6c97e1c49d73e3d5694cfcd0f7b6c8170497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989158"
---
# <a name="d3dx10getimageinfofromresource-function"></a>D3DX10GetImageInfoFromResource 函式

抓取資源中指定影像的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSrcModule* \[在\]
</dt> <dd>

類型： **[ **HMODULE**](../winprog/windows-data-types.md)**

載入資源的模組。 將此參數設定為 **Null** ，以指定與作業系統用來建立目前進程的映射相關聯的模組。

</dd> <dt>

*pSrcResource* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**

指定檔案名之字串的指標。 如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。 否則，資料型別會解析為 LPCSTR。 請參閱＜備註＞。

</dd> <dt>

*pPump* \[在\]
</dt> <dd>

類型： **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

選擇性的執行緒抽取，可用來以非同步方式載入資訊。 可以是 **Null**。 請參閱 [**ID3DX10ThreadPump**](id3dx10threadpump.md)。

</dd> <dt>

*pSrcInfo* \[在\]
</dt> <dd>

類型： **[ **D3DX10 \_ 影像 \_ 資訊**](d3dx10-image-info.md)\***

D3DX10 影像資訊結構的指標，此 \_ \_ 結構會填入原始程式檔中的資料描述。

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

編譯器設定也會決定函式版本。 如果已定義 Unicode，函式呼叫會解析為 D3DX10GetImageInfoFromResourceW。 否則，函式呼叫會解析為 D3DX10GetImageInfoFromResourceA，因為正在使用 ANSI 字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 10 中的材質函數](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
