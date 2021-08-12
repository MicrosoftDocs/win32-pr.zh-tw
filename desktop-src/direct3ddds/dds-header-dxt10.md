---
title: 'DDS_HEADER_DXT10 結構 (Dd. h) '
description: 用來處理資源陣列的 DDS 標頭延伸、未對應到舊版 Microsoft DirectDraw 像素格式結構的 DXGI 像素格式，以及其他中繼資料。
ms.assetid: 502d6943-8f25-446c-b990-8276f862c195
keywords:
- DDS_HEADER_DXT10 結構 DDS
topic_type:
- apiref
api_name:
- DDS_HEADER_DXT10
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da95b65739922861002ab134d33f276adabd19c29d14fdea6432616b6c5edc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289785"
---
# <a name="dds_header_dxt10-structure"></a>DDS \_ 標頭 \_ DXT10 結構

用來處理資源陣列的 DDS 標頭延伸、未對應到舊版 Microsoft DirectDraw 像素格式結構的 DXGI 像素格式，以及其他中繼資料。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DXGI_FORMAT              dxgiFormat;
  D3D10_RESOURCE_DIMENSION resourceDimension;
  UINT                     miscFlag;
  UINT                     arraySize;
  UINT                     miscFlags2;
} DDS_HEADER_DXT10;
```



## <a name="members"></a>成員

<dl> <dt>

**dxgiFormat**
</dt> <dd>

類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Surface 像素格式 (查看 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) 。

</dd> <dt>

**resourceDimension**
</dt> <dd>

類型： **[ **D3D10 \_ 資源 \_ 維度**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**

</dd> <dd>

識別資源的類型。 此成員的下列值是 [**D3D10 \_ 資源 \_ 維度**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) 或 [**D3D11 \_ 資源 \_ 維度**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension) 列舉中值的子集：



| 類型                                                              | 描述                                                                                                                                                                                                                                                                                                                                                            | 值 |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| DDS \_ 維度 \_ TEXTURE1D (D3D10 \_ 資源 \_ 維度 \_ TEXTURE1D)  | 資源是一 [維紋理](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types)。 [**DDS \_ 標頭**](dds-header.md)的 **dwWidth** 成員會指定紋理的大小。 一般來說，您會將 **dds \_ 標頭** 的 **dwHeight** 成員設為 1; 您也必須 \_ 在 **dds \_ 標頭** 的 **dwFlags** 成員中設定 DDSD HEIGHT 旗標。                      | 2     |
| DDS \_ 維度 \_ TEXTURE2D (D3D10 \_ 資源 \_ 維度 \_ TEXTURE2D)  | 資源是 [2d 材質](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types)，具有由 [**DDS \_ 標頭**](dds-header.md)的 **dwWidth** 和 **dwHeight** 成員所指定的區域。 您也可以使用此類型來識別 cube 對應材質。 如需如何識別 cube 對應材質的詳細資訊，請參閱 **miscFlag** 和 **arraySize** 成員。 | 3     |
| DDS \_ 維度 \_ TEXTURE3D (D3D10 \_ 資源 \_ 維度 \_ TEXTURE3D)  | 資源是包含 **dwWidth**、 **dwHeight** 和 **dwDepth** 之 [**DDS \_ 標頭**](dds-header.md)成員所指定之磁片區的 [3d 紋理](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types)。 您也必須 \_ 在 **DDS \_ 標頭** 的 **dwFlags** 成員中設定 DDSD DEPTH 旗標。                                                                   | 4     |



 

</dd> <dt>

**miscFlag**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

識別其他較不常用的資源選項。 此成員的下列值是 [**D3D10 \_ 資源 \_ 其他 \_ 旗**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) 標或 [**D3D11 \_ 資源 \_ 其他 \_ 旗**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) 標列舉中值的子集：



| 類型                             | 描述                                                                                                  | 值 |
|----------------------------------|--------------------------------------------------------------------------------------------------------------|-------|
| DDS \_ 資源的 \_ 其他 \_ TEXTURECUBE | 表示 [2d 材質](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) 是 cube 地圖材質。 | 0x4   |



 

</dd> <dt>

**arraySize**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

陣列中的項目數。

針對也是 cube 對應材質的 [2d 材質](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) ，此數位代表 cube 的數目。 這個數位與 [**D3D10 \_ TEXCUBE \_ Array \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1)或 [**D3D11 \_ TEXCUBE \_ ARRAY \_ SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv)) 的 **NumCubes** 成員中的數位相同。 在此情況下，DDS 檔案包含 **arraySize** \* 6 2d 材質。 如需此案例的詳細資訊，請參閱 **miscFlag** 描述。

若為 [3d 紋理](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types)，您必須將此數位設定為1。

</dd> <dt>

**miscFlags2**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

包含先前保留)  (的額外中繼資料。 較低的3位表示相關聯資源的 Alpha 模式。 前29個位是保留的，通常是0。



| 類型                            | 描述                                                                                                                              | 值 |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|-------|
| DDS \_ ALPHA \_ 模式 \_ 未知       | Alpha 通道內容不明。 這是舊版檔案的值，通常會假設為「直接」 Alpha。                 | 0x0   |
| DDS \_ ALPHA \_ 模式 \_ 直接      | 任何 Alpha 通道內容都會假設為使用直接 Alpha。                                                                             | 0x1   |
| 已預乘的 DDS \_ ALPHA \_ 模式 \_ | 任何 Alpha 通道內容都使用預乘 Alpha。 唯一指出此資訊的舊版檔案格式為 ' DX2 ' 和 ' DX4 '。 | 0x2   |
| DDS \_ ALPHA \_ 模式不 \_ 透明        | 所有 Alpha 通道內容都設為完全不透明。                                                                                    | 0x3   |
| DDS \_ ALPHA \_ 模式 \_ 自訂        | 任何 Alpha 通道內容都是用來作為第四個通道，而不是用來表示 (直接或預乘) 的透明度。      | 0x4   |



 

> [!Note]  
> 舊版 D3DX 10 和 [D3DX 11](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) 公用程式程式庫將無法載入任何一個。 **MiscFlags2** 不等於零的 DDS 檔。

 

</dd> </dl>

## <a name="remarks"></a>備註

將此結構與 [**dds \_ 標頭**](dds-header.md) 搭配使用，以將資源陣列儲存在 dds 檔案中。 如需詳細資訊，請參閱 [材質陣列](dx-graphics-dds-pguide.md)。

如果 [**DDS \_ PIXELFORMAT**](dds-pixelformat.md)結構的 **dwFourCC** 成員設定為 ' DX10 '，就會出現此標頭。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dd. h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DDS 的參考](dx-graphics-dds-reference.md)
</dt> </dl>

 

