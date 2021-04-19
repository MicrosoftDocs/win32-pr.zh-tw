---
description: 將預先計算 radiance 傳輸 (PRT) 緩衝區儲存至磁片。
ms.assetid: 1fca69bd-6729-45af-981f-b7480c741bc2
title: 'D3DXSavePRTBufferToFile 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b796ee24be44bf65be7df938bdfe85d6784cc5f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985883"
---
# <a name="d3dxsaveprtbuffertofile-function"></a>D3DXSavePRTBufferToFile 函式

將預先計算 radiance 傳輸 (PRT) 緩衝區儲存至磁片。

## <a name="syntax"></a>語法

```cpp
HRESULT D3DXSavePRTBufferToFile(
  _In_ LPCSTR          pFileName,
  _In_ LPD3DXPRTBUFFER pBuffer
);
```

## <a name="parameters"></a>參數

*pFileName* \[在\]

類型： **[LPCSTR](../winprog/windows-data-types.md)**

要儲存緩衝區的檔案名。

*pBuffer* \[在\]

類型： **[LPD3DXPRTBUFFER](id3dxprtbuffer.md)**

輸入 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件之指標的位址。

## <a name="return-value"></a>傳回值

類型： **[HRESULT](../com/structure-of-com-error-codes.md)**

如果方法成功，則傳回值為「 **D3D \_ 正常**」。 如果方法失敗，則傳回值可以是 **D3DERR \_ INVALIDCALL**。

## <a name="remarks"></a>備註

編譯器設定也會決定函式版本。 如果已定義 Unicode，則函式呼叫會解析為 [D3DXSavePRTBufferToFileW]()。 否則，函式呼叫會解析為 **D3DXSavePRTBufferToFileA**。

PRT 檔案格式是一種二進位檔案，其格式為標頭，然後是資料區塊。

```cpp
struct PRTHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
};
```

如果 *bIsTex* 不是零， *NumSamples* 應該相等 `TexWidth * TexHeight` 。

標頭之後的資料區塊是 `NumSamples * NumCoeffs * NumChannels * sizeof(float)` 位元組。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |

## <a name="see-also"></a>另請參閱

[預先計算 Radiance 傳送函式](dx9-graphics-reference-d3dx-functions-prt.md)
