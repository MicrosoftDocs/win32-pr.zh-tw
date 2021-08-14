---
description: 識別壓縮的主要畫面格動畫資料。
ms.assetid: 2aab46db-e0ad-4bbb-b1c5-a254ec6cb984
title: 'XFILECOMPRESSEDANIMATIONSET 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XFILECOMPRESSEDANIMATIONSET
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 41c64ae7bb2ca4acf87e1b63de90f2ccfc78e8d769adf334aa1f68b9bf79de0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518557"
---
# <a name="xfilecompressedanimationset-structure"></a>XFILECOMPRESSEDANIMATIONSET 結構

識別壓縮的主要畫面格動畫資料。

## <a name="syntax"></a>語法


```C++
typedef struct XFILECOMPRESSEDANIMATIONSET {
  DWORD CompressedBlockSize;
  FLOAT TicksPerSec;
  DWORD PlaybackType;
  DWORD BufferLength;
} XFILECOMPRESSEDANIMATIONSET, *LPXFILECOMPRESSEDANIMATIONSET;
```



## <a name="members"></a>成員

<dl> <dt>

**CompressedBlockSize**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

壓縮的主要畫面格動畫資料緩衝區中壓縮資料的總大小（以位元組為單位）。

</dd> <dt>

**TicksPerSec**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

每秒發生的動畫主要畫面格刻度數目。

</dd> <dt>

**PlaybackType**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

動畫集合播放迴圈的型別。 請參閱 [**D3DXPLAYBACK \_ 類型**](./d3dxplayback-type.md)。

</dd> <dt>

**BufferLength**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

保存壓縮的主要畫面格動畫資料所需的緩衝區大小下限（以位元組為單位）。 值等於 ( ( CompressedBlockSize + 3 ) /4 ) 。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9mesh。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX X 檔案結構](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> <dt>

[**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md)
</dt> </dl>

 

 
