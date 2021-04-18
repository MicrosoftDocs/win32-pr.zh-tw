---
title: 'D3DX11_IMAGE_LOAD_INFO 結構 (D3DX11tex .h) '
description: '請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 選擇性地提供材質載入器 Api 的資訊，以控制如何載入紋理。 |D3DX11_IMAGE_LOAD_INFO 結構 (D3DX11tex .h) '
ms.assetid: 6cd2f590-4e15-41e6-9f04-cd91eeb082db
keywords:
- D3DX11_IMAGE_LOAD_INFO 結構 Direct3D 11
- LPD3DX11_IMAGE_LOAD_INFO 結構指標 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2905d135a515f4ef90557ac74c35665623462439
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974709"
---
# <a name="d3dx11_image_load_info-structure"></a>D3DX11 \_ 映射 \_ 載入 \_ 資訊結構

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。

 

選擇性地提供材質載入器 Api 的資訊，以控制如何載入紋理。 \_任何這些參數的 D3DX11 預設值都會導致 D3DX 自動使用來源檔案的值。

## <a name="syntax"></a>語法


```C++
typedef struct D3DX11_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D11_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX11_IMAGE_INFO *pSrcInfo;
} D3DX11_IMAGE_LOAD_INFO, *LPD3DX11_IMAGE_LOAD_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**寬度**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

材質的目標寬度。 如果材質的實際寬度大於或等於這個值，則紋理會向上或向下調整以符合此目標寬度。

</dd> <dt>

**高度**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

材質的目標高度。 如果紋理的實際高度大於或等於這個值，則紋理會向上或向下調整以符合此目標高度。

</dd> <dt>

**深度**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

材質的深度。 這僅適用于磁片區紋理。

</dd> <dt>

**FirstMipLevel**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

材質的最高解析度 mipmap 層級。 如果大於0，則在載入紋理之後，FirstMipLevel 會對應至 mipmap 層級0。

</dd> <dt>

**MipLevels**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

材質中 mipmap 層級的最大數目。 請參閱 [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv)中的備註。 使用0或 D3DX11 \_ 預設值，將會建立完整的 mipmap 鏈。

</dd> <dt>

**使用量**
</dt> <dd>

類型： **[ **D3D11 \_ 使用** 方式](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**

</dd> <dd>

材質資源的使用方式。 請參閱 [**D3D11 \_ 使用量**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)。

</dd> <dt>

**BindFlags**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

將允許紋理系結的管線階段。 請參閱 [**D3D11 \_ BIND \_ 旗**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)標。

</dd> <dt>

**CpuAccessFlags**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Cpu 對材質資源將擁有的存取權限。 請參閱 [**D3D11 \_ CPU \_ 存取 \_ 旗**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag)標。

</dd> <dt>

**MiscFlags**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

其他資源屬性 (參閱 [**D3D11 \_ 資源 \_ 其他 \_ 旗**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) 標) 。

</dd> <dt>

**格式**
</dt> <dd>

類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

一個 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 列舉，指出材質載入後的材質格式。

</dd> <dt>

**Filter**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

只有在重新取樣) 時，才使用指定的篩選 (篩選材質。 請參閱 [**D3DX11 \_ 篩選 \_ 旗**](d3dx11-filter-flag.md)標。

</dd> <dt>

**MipFilter**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

只有在產生 mipmap) 時，才使用指定的篩選 (來篩選材質 mip 層級。 有效的值為 D3DX11 \_ filter \_ NONE、D3DX11 \_ FILTER \_ POINT、D3DX11 \_ filter \_ 線性或 D3DX11 \_ filter \_ 三角形。 請參閱 [**D3DX11 \_ 篩選 \_ 旗**](d3dx11-filter-flag.md)標。

</dd> <dt>

**pSrcInfo**
</dt> <dd>

類型： **[ **D3DX11 \_ 影像 \_ 資訊**](d3dx11-image-info.md)\***

</dd> <dd>

原始影像的相關資訊。 請參閱 [**D3DX11 \_ 影像 \_ 資訊**](d3dx11-image-info.md)。 可以使用 [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md)、 [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)或 [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md)取得。

</dd> </dl>

## <a name="remarks"></a>備註

在初始化結構時，您可以將任何成員設定為 D3DX11 \_ 預設值，而 D3DX 會在載入紋理時，使用來源材質的預設值將它初始化。

下列 Api 可以使用此結構：

-   建立資源，例如 [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) 和 [**D3DX11CreateShaderResourceViewFromFile**](d3dx11createshaderresourceviewfromfile.md)。
-   建立資料處理器，例如 [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) 或 [**D3DX11CreateAsyncShaderResourceViewProcessor**](d3dx11createasyncshaderresourceviewprocessor.md)。

預設值是：


```
    Width = D3DX11_DEFAULT;
    Height = D3DX11_DEFAULT;
    Depth = D3DX11_DEFAULT;
    FirstMipLevel = D3DX11_DEFAULT;
    MipLevels = D3DX11_DEFAULT;
    Usage = (D3D11_USAGE) D3DX11_DEFAULT;
    BindFlags = D3DX11_DEFAULT;
    CpuAccessFlags = D3DX11_DEFAULT;
    MiscFlags = D3DX11_DEFAULT;
    Format = DXGI_FORMAT_FROM_FILE;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
    pSrcInfo = NULL;
```



以下是在載入材質時，使用此結構來提供像素格式的簡短範例。 如需完整的程式碼，請參閱 [HDRToneMappingCS11 範例](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx)中的 HDRFormats10 .cpp。


```
ID3D11ShaderResourceView* pCubeRV = NULL;
WCHAR strPath[MAX_PATH];
D3DX11_IMAGE_LOAD_INFO LoadInfo;

    DXUTFindDXSDKMediaFileCch( strPath, MAX_PATH, 
        L"Light Probes\\uffizi_cross.dds" );

    LoadInfo.Format = DXGI_FORMAT_R16G16B16A16_FLOAT;

    hr = D3DX11CreateShaderResourceViewFromFile( pd3dDevice, strPath, 
        &LoadInfo, NULL, &pCubeRV, NULL );
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX11tex。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

