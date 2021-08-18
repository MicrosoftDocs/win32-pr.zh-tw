---
description: 將壓縮的預先計算 radiance 傳輸 (PRT) 緩衝區儲存至磁片。
ms.assetid: cc94a83e-f755-411d-a993-4529c5d53cd5
title: 'D3DXSavePRTCompBufferToFile 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTCompBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a62bd164ce8eb8175c62658b19dd5ce6282d6c75b081db45f8b0af4994322579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524508"
---
# <a name="d3dxsaveprtcompbuffertofile-function"></a>D3DXSavePRTCompBufferToFile 函式

將壓縮的預先計算 radiance 傳輸 (PRT) 緩衝區儲存至磁片。

## <a name="syntax"></a>語法

```cpp
HRESULT D3DXSavePRTCompBufferToFile(
  _In_ LPCSTR              pFileName,
  _In_ LPD3DXPRTCOMPBUFFER pBuffer
);
```

## <a name="parameters"></a>參數

*pFileName* \[在\]

類型： **[LPCSTR](../winprog/windows-data-types.md)**

要儲存壓縮緩衝區的檔案名。

*pBuffer* \[在\]

類型： **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**

輸入 [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) 物件之指標的位址。

## <a name="return-value"></a>傳回值

類型： **[HRESULT](../com/structure-of-com-error-codes.md)**

如果方法成功，則傳回值為「 **D3D \_ 正常**」。 如果方法失敗，則傳回值可以是 **D3DERR \_ INVALIDCALL**。

## <a name="remarks"></a>備註

編譯器設定也會決定函式版本。 如果已定義 Unicode，則函式呼叫會解析為 [D3DXSavePRTCompBufferToFileW]()。 否則，函式呼叫會解析為 **D3DXSavePRTCompBufferToFileA**。

PCA 檔案格式是一種二進位檔案，格式為標頭，再接著兩個或三個數據區塊。

```cpp
struct PRTCompressHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
    UINT NumClusters;
    UINT NumPCA;
};
```

如果 *bIsTex* 不是零， *NumSamples* 應該相等 `TexWidth * TexHeight` 。

標頭之後的基礎資料區塊是 `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` 位元組。

以下是 PCA 加權資料區塊，也就是 `NumPCA * NumSamples * sizeof(float)` 位元組。

如果 *NumClusters* 大於1，檔案就會以位元組的叢集識別碼資料區塊結尾 `NumSamples * sizeof(UINT)` 。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |

## <a name="see-also"></a>另請參閱

[預先計算 Radiance 傳送函式](dx9-graphics-reference-d3dx-functions-prt.md)
