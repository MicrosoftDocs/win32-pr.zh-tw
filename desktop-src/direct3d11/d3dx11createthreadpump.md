---
title: 'D3DX11CreateThreadPump 函式 (D3DX11core) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。 建立執行緒抽取。
ms.assetid: 8983a2e2-185f-43c0-baf0-a4c883d91220
keywords:
- D3DX11CreateThreadPump 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a3a19c338b330604caae9ce5a1e7f7222664b0521f9874c3eff07ff1fc8a4f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536099"
---
# <a name="d3dx11createthreadpump-function"></a>D3DX11CreateThreadPump 函式

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，不支援 Windows Store 應用程式。 請參閱＜備註＞。

 

建立執行緒抽取。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX11CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX11ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cIoThreads* \[在\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

要建立的 i/o 執行緒數目。 如果指定0，Direct3D 將會根據硬體設定嘗試計算最佳的執行緒數目。

</dd> <dt>

*cProcThreads* \[在\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

要建立的進程執行緒數目。 如果指定0，Direct3D 將會根據硬體設定嘗試計算最佳的執行緒數目。

</dd> <dt>

*ppThreadPump* \[擴展\]
</dt> <dd>

類型： **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\*\***

建立的執行緒抽取。 請參閱 [**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="remarks"></a>備註

執行緒抽取是非常耗費資源的物件。 每個應用程式只應建立一個執行緒抽取。

D3DX 10 和 D3DX 11 以外的非同步載入器不會執行。

針對 Windows Store 應用程式，DirectX 範例 (例如， [Direct3D 教學課程範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) 包含使用 Windows 執行階段非同步程式設計模型 ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) 的 **BasicLoader** 模組。

針對 Win32 傳統型應用程式，您可以使用[並行執行階段](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100))來執行類似于 Windows 執行階段非同步程式設計模型的內容。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX11core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX11 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 函式](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

