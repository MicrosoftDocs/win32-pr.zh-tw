---
title: 'DDS_PIXELFORMAT 結構 (Dd. h) '
description: Surface 像素格式。
ms.assetid: 39c5e48d-cf20-4d77-80d5-a67f04de4883
keywords:
- DDS_PIXELFORMAT 結構 DDS
topic_type:
- apiref
api_name:
- DDS_PIXELFORMAT
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd909d62a1be212f9ed4ef9af243a27f28be818
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982197"
---
# <a name="dds_pixelformat-structure"></a>DDS \_ PIXELFORMAT 結構

Surface 像素格式。

## <a name="syntax"></a>語法


```C++
struct DDS_PIXELFORMAT {
  DWORD dwSize;
  DWORD dwFlags;
  DWORD dwFourCC;
  DWORD dwRGBBitCount;
  DWORD dwRBitMask;
  DWORD dwGBitMask;
  DWORD dwBBitMask;
  DWORD dwABitMask;
};
```



## <a name="members"></a>成員

<dl> <dt>

**dwSize**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

結構大小;設定為 32 (位元組) 。

</dd> <dt>

**dwFlags**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

指出介面中資料類型的值。



| 旗標              | 描述                                                                                                                                                                                                                                | 值   |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|
| DDPF \_ ALPHAPIXELS | 材質包含 Alpha 資料; **dwRGBAlphaBitMask** 包含有效的資料。                                                                                                                                                                    | 0x1     |
| DDPF \_ ALPHA       | 用於 Alpha 通道的一些較舊的 DDS 檔 (dwRGBBitCount 包含 Alpha 通道 bitcount;dwABitMask 包含有效的資料)                                                                                   | 0x2     |
| DDPF \_ FOURCC      | 材質包含壓縮的 RGB 資料; **dwFourCC** 包含有效的資料。                                                                                                                                                                    | 0x4     |
| DDPF \_ RGB         | 材質包含未壓縮的 RGB 資料; **dwRGBBitCount** 和 RGB 遮罩 (**dwRBitMask**、 **dwGBitMask**、 **dwBBitMask**) 包含有效的資料。                                                                                           | 0x40    |
| DDPF \_ YUV         | 用在一些較舊的 DDS 檔中，用於 YUV 未壓縮的資料 (dwRGBBitCount 包含 YUV 位元數目;dwRBitMask 包含 Y 遮罩，dwGBitMask 包含 U 遮罩，dwBBitMask 包含 V 遮罩)                                           | 0x200   |
| DDPF \_ 亮度   | 用於某些較舊的 DDS 檔案，用於單一通道色彩未壓縮資料 (dwRGBBitCount 包含亮度通道位元數目;dwRBitMask 包含通道遮罩) 。 可以與 \_ 兩個通道 DDS 檔案的 DDPF ALPHAPIXELS 結合。 | 0x20000 |



 

</dd> <dt>

**dwFourCC**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

用來指定壓縮或自訂格式的四個字元的代碼。 可能的值包括： *DXT1*、 *DXT2*、 *DXT3*、 *DXT4* 或 *DXT5*。 FourCC of DX10 指出 [**DDS \_ 標頭 \_ DXT10**](dds-header-dxt10.md) 擴充標頭的 prescense，而該結構的 dxgiFormat 成員表示 true 格式。 使用四個字元的程式碼時，dwFlags 必須包含 *DDPF \_ FOURCC*。

</dd> <dt>

**dwRGBBitCount**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

RGB (中可能包含 Alpha) 格式的位數。 在 **dwFlags** 包含 *DDPF \_ RGB*、 *DDPF \_ 亮度* 或 *DDPF \_ YUV* 時有效。

</dd> <dt>

**dwRBitMask**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

用於讀取色彩資料的紅色 (或 lumiannce 或 Y) 遮罩。 例如，假設有 A8R8G8B8 格式，則會0x00ff0000 紅色遮罩。

</dd> <dt>

**dwGBitMask**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

綠色 (或 U) 遮罩來讀取色彩資料。 例如，假設有 A8R8G8B8 格式，則會0x0000ff00 綠色遮罩。

</dd> <dt>

**dwBBitMask**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

用於讀取色彩資料的藍色 (或 V) 遮罩。 例如，假設有 A8R8G8B8 格式，則會0x000000ff 藍色遮罩。

</dd> <dt>

**dwABitMask**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

用來讀取 Alpha 資料的 Alpha 遮罩。 dwFlags 必須包含 *DDPF \_ ALPHAPIXELS* 或 *DDPF \_ ALPHA*。 例如，假設有 A8R8G8B8 格式，則會 0xff000000 Alpha 遮罩。

</dd> </dl>

## <a name="remarks"></a>備註

若要儲存像浮點數資料等 DXGI 格式，請使用 DDPF FOURCC 的 **dwFlags** ， \_ 並將 **DwFourCC** 設定為 ' d '、' X '、' 1 '、' 0 '。 使用 [**DDS \_ 標頭 \_ DXT10**](dds-header-dxt10.md) 延伸模組標頭將 DXGI 格式儲存在 **dxgiFormat** 成員中。

請注意， **dwFlags** 具有 DDPF \_ FOURCC 且 **dwFourCC** 值直接設定為 D3DFORMAT 或 DXGI \_ 格式列舉值的 DDS 檔案有非標準的變體。 \_您無法使用這個非標準配置來區分 D3DFORMAT 與 DXGI 格式值，因此建議改用 DX10 延伸模組標頭。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dd. h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DDS 的參考](dx-graphics-dds-reference.md)
</dt> </dl>

 

