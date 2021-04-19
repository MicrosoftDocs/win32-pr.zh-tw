---
title: 'DDS_HEADER 結構 (Dd. h) '
description: 描述 DDS 檔案標頭。
ms.assetid: 7f8bde30-0ff9-4bb9-b444-5c875e6a0865
keywords:
- DDS_HEADER 結構 DDS
topic_type:
- apiref
api_name:
- DDS_HEADER
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70fa0c4b05b6655ce0329cc73651ea21d4d808
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974842"
---
# <a name="dds_header-structure"></a>DDS \_ 標頭結構

描述 DDS 檔案標頭。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD           dwSize;
  DWORD           dwFlags;
  DWORD           dwHeight;
  DWORD           dwWidth;
  DWORD           dwPitchOrLinearSize;
  DWORD           dwDepth;
  DWORD           dwMipMapCount;
  DWORD           dwReserved1[11];
  DDS_PIXELFORMAT ddspf;
  DWORD           dwCaps;
  DWORD           dwCaps2;
  DWORD           dwCaps3;
  DWORD           dwCaps4;
  DWORD           dwReserved2;
} DDS_HEADER;
```



## <a name="members"></a>成員

<dl> <dt>

**dwSize**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

結構的大小。 此成員必須設定為124。

</dd> <dt>

**dwFlags**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

旗標，指出哪些成員包含有效的資料。



| 旗標              | 描述                                                  | 值    |
|-------------------|--------------------------------------------------------------|----------|
| DDSD \_ 帽        | 每個 dd 檔案都需要。                                 | 0x1      |
| DDSD \_ 高度      | 每個 dd 檔案都需要。                                 | 0x2      |
| DDSD \_ 寬度       | 每個 dd 檔案都需要。                                 | 0x4      |
| DDSD \_ 音調       | 針對未壓縮材質提供音調時需要。 | 0x8      |
| DDSD \_ PIXELFORMAT | 每個 dd 檔案都需要。                                 | 0x1000   |
| DDSD \_ MIPMAPCOUNT | Mipmapped 材質中的必要項。                             | 0x20000  |
| DDSD \_ LINEARSIZE  | 針對壓縮材質提供音調時需要。    | 0x80000  |
| DDSD \_ 深度       | 深度材質中的必要項。                                 | 0x800000 |



 

> [!Note]  
> 當您撰寫 dds 檔案時，您應該設定 DDSD \_ CAPS AND DDSD \_ PIXELFORMAT 旗標，而針對 mipmapped 紋理，您也應該設定 DDSD \_ MIPMAPCOUNT 旗標。 但是，當您讀取的是 dds 檔案時，不應該依賴設定的 DDSD \_ CAPS、DDSD \_ PIXELFORMAT 和 DDSD \_ MIPMAPCOUNT 旗標，因為這類檔案的某些寫入器可能不會設定這些旗標。

 

Dds \_ 標頭 \_ 旗標 \_ 材質旗標（定義于 dd. h 中）是 DDSD \_ CAPS、DDSD \_ HEIGHT、DDSD \_ WIDTH 和 DDSD \_ PIXELFORMAT 旗標的位 or 組合。

Dds \_ 標頭 \_ 旗標 \_ MIPMAP 旗標（定義于 dd. h）等於 DDSD \_ MIPMAPCOUNT 旗標。

Dds \_ 標頭 \_ 旗標 \_ 磁片區旗標（定義于 dd. h）等於 DDSD \_ DEPTH 旗標。

Dds \_ 標頭 \_ 旗標 \_ 音調旗標（定義于 dd. h 中）等於 DDSD \_ 音調旗標。

Dds \_ 標頭 \_ 旗標 \_ LINEARSIZE 旗標（定義于 dd. h）等於 DDSD \_ LINEARSIZE 旗標。

</dd> <dt>

**dwHeight**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

介面高度 (以圖元為單位) 。

</dd> <dt>

**dwWidth**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

介面寬度 (以圖元為單位) 。

</dd> <dt>

**dwPitchOrLinearSize**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

未壓縮材質中每個掃描行的字元數或位元組數;針對壓縮材質的最上層材質中的總位元組數。 如需如何計算推銷方式的詳細資訊，請參閱 [dds 程式設計指南](dx-graphics-dds-pguide.md)的 dds 檔案配置一節。

</dd> <dt>

**dwDepth**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

磁片區材質的深度 (（以圖元為單位）) ，否則未使用。

</dd> <dt>

**dwMipMapCount**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Mipmap 層級的數目，否則未使用。

</dd> <dt>

**dwReserved1 \[ 11\]**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

未使用的。

</dd> <dt>

**ddspf**
</dt> <dd>

類型： **[ **DDS \_ PIXELFORMAT**](dds-pixelformat.md)**

</dd> <dd>

像素格式 (查看 [**DDS \_ PIXELFORMAT**](dds-pixelformat.md)) 。

</dd> <dt>

**dwCaps**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

指定所儲存之表面的複雜度。



| 旗標             | 描述                                                                                                                              | 值    |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|----------|
| DDSCAPS \_ 複雜 | 參數必須用於包含多個介面 (mipmap、三層環境對應或 mipmapped 磁片區材質) 的任何檔案。 | 0x8      |
| DDSCAPS \_ MIPMAP  | 參數應用於 mipmap。                                                                                                   | 0x400000 |
| DDSCAPS \_ 材質 | 必要                                                                                                                                 | 0x1000   |



 

> [!Note]  
> 當您撰寫 dds 檔案時，您應該設定 DDSCAPS \_ 材質旗標，而針對多個表面，您也應該設定 DDSCAPS \_ 複雜旗標。 但是，當您讀取的是 dds 檔案時，不應該依賴 DDSCAPS \_ 材質和 DDSCAPS \_ 複雜旗標，因為這類檔案的某些寫入器可能不會設定這些旗標。

 

Dds \_ 介面 \_ 旗標 \_ MIPMAP 旗標是在 dds 中定義，它是 DDSCAPS \_ COMPLEX 和 DDSCAPS MIPMAP 旗標的位 or 組合 \_ 。

Dds \_ 介面 \_ 旗標 \_ 材質旗標（定義于 dd. h 中）等於 DDSCAPS \_ 材質旗標。

Dds \_ 介面 \_ 旗標 \_ 立方體貼圖旗標（定義于 dd. h）等於 DDSCAPS \_ 複雜旗標。

</dd> <dt>

**dwCaps2**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

所儲存之表面的其他詳細資料。



| 旗標                         | 描述                                            | 值    |
|------------------------------|--------------------------------------------------------|----------|
| DDSCAPS2 \_ 立方體貼圖            | Cube 對應的必要參數。                               | 0x200    |
| DDSCAPS2 \_ 立方體貼圖 \_ POSITIVEX | 當這些介面儲存在 cube 對應中時，這是必要的。 | 0x400    |
| DDSCAPS2 \_ 立方體貼圖 \_ NEGATIVEX | 當這些介面儲存在 cube 對應中時，這是必要的。 | 0x800    |
| DDSCAPS2 \_ 立方體貼圖 \_ POSITIVEY | 當這些介面儲存在 cube 對應中時，這是必要的。 | 0x1000   |
| DDSCAPS2 \_ 立方體貼圖 \_ NEGATIVEY | 當這些介面儲存在 cube 對應中時，這是必要的。 | 0x2000   |
| DDSCAPS2 \_ 立方體貼圖 \_ POSITIVEZ | 當這些介面儲存在 cube 對應中時，這是必要的。 | 0x4000   |
| DDSCAPS2 \_ 立方體貼圖 \_ NEGATIVEZ | 當這些介面儲存在 cube 對應中時，這是必要的。 | 0x8000   |
| DDSCAPS2 \_ 磁片區             | 磁片區材質的必要參數。                         | 0x200000 |



 

Dds \_ 立方體貼圖 \_ POSITIVEX 旗標是在 dds 中定義，它是 DDSCAPS2 \_ 立方體貼圖和 DDSCAPS2 \_ 立方體貼圖 POSITIVEX 旗標的位 or 組合 \_ 。

Dds \_ 立方體貼圖 \_ NEGATIVEX 旗標是在 dds 中定義，它是 DDSCAPS2 \_ 立方體貼圖和 DDSCAPS2 \_ 立方體貼圖 NEGATIVEX 旗標的位 or 組合 \_ 。

Dds \_ 立方體貼圖 \_ POSITIVEY 旗標是在 dds 中定義，它是 DDSCAPS2 \_ 立方體貼圖和 DDSCAPS2 \_ 立方體貼圖 POSITIVEY 旗標的位 or 組合 \_ 。

Dds \_ 立方體貼圖 \_ NEGATIVEY 旗標是在 dds 中定義，它是 DDSCAPS2 \_ 立方體貼圖和 DDSCAPS2 \_ 立方體貼圖 NEGATIVEY 旗標的位 or 組合 \_ 。

Dds \_ 立方體貼圖 \_ POSITIVEZ 旗標是在 dds 中定義，它是 DDSCAPS2 \_ 立方體貼圖和 DDSCAPS2 \_ 立方體貼圖 POSITIVEZ 旗標的位 or 組合 \_ 。

Dds \_ 立方體貼圖 \_ NEGATIVEZ 旗標是在 dds 中定義，它是 DDSCAPS2 \_ 立方體貼圖和 DDSCAPS2 \_ 立方體貼圖 NEGATIVEZ 旗標的位 or 組合 \_ 。

Dds \_ 立方體貼圖 \_ ALLFACES 旗標（定義于 dd. h 中）是 dds \_ 立方體貼圖 \_ POSITIVEX、DDS \_ 立方體貼圖 \_ NEGATIVEX、dds \_ 立方體貼圖 \_ POSITIVEY、DDS \_ 立方體貼圖 \_ NEGATIVEY、dds \_ 立方體貼圖 \_ POSITIVEZ 和 DDSCAPS2 \_ 立方體貼圖 \_ NEGATIVEZ 旗標的位 or 組合。

Dds \_ 旗標 \_ 磁片區旗標（定義于 dd. h）等於 DDSCAPS2 \_ VOLUME 旗標。

> [!Note]  
> 雖然 Direct3D 9 支援部分 cube 對應，Direct3D 10、10.1 和11都需要您定義全部六個立方體圖的臉部 (也就是說，您必須設定 DDS \_ 立方體貼圖 \_ ALLFACES) 。

 

</dd> <dt>

**dwCaps3**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

未使用的。

</dd> <dt>

**dwCaps4**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

未使用的。

</dd> <dt>

**dwReserved2**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

未使用的。

</dd> </dl>

## <a name="remarks"></a>備註

針對包含有效資料之結構的成員，包含 **dwFlags** 中的旗標。

搭配使用此結構與 [**dds \_ 標頭 \_ DXT10**](dds-header-dxt10.md) ，將資源陣列儲存在 dds 檔案中。 如需詳細資訊，請參閱 [材質陣列](dx-graphics-dds-pguide.md)。

**DDS \_標頭** 與 DIRECTDRAW DDSURFACEDESC2 結構完全相同，但沒有 directdraw 相依性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dd. h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DDS 的參考](dx-graphics-dds-reference.md)
</dt> </dl>

 

