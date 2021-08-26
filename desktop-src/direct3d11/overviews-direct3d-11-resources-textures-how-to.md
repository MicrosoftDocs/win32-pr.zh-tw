---
title: 如何從檔案初始化材質
description: 本主題說明如何使用 Windows 影像處理元件 (WIC) 來分開建立材質和視圖。
ms.assetid: ea3c6003-191d-47d1-8931-f43598728ad4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b3e8035e630a7b2182c114e329cf4b08428ab3a83ca218b933cb2b922ff305c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027938"
---
# <a name="how-to-initialize-a-texture-from-a-file"></a>如何：從檔案初始化材質

您可以使用[Windows 影像處理元件](/windows/desktop/wic/-wic-lh)API，從檔案初始化[材質](overviews-direct3d-11-resources-textures.md)。 若要載入紋理，您必須建立材質和材質視圖。 本主題說明如何使用 Windows 影像處理元件 (WIC) 來分開建立材質和視圖。

> [!Note]  
> 本主題適用于您建立為簡單2D 材質的影像。 如需更複雜的資源，請使用 [DDS](/windows/desktop/direct3ddds/dx-graphics-dds)。 如需完整功能的 DDS 檔案讀取器、寫入器和材質處理管線，請參閱 [DirectXTex](https://github.com/Microsoft/DirectXTex) 和 [DirectXTK](https://github.com/Microsoft/DirectXTK)。

 

在本主題的結尾，您將會找到完整的範例程式碼。 本主題說明建立材質和視圖的範例程式碼部分。

**分別初始化材質和 view。**

1.  呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 以建立映射處理站介面 ([**IWICImagingFactory**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory)) 。
2.  呼叫 [**IWICImagingFactory：： CreateDecoderFromFilename**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) 方法，從影像檔案名稱建立 [**IWICBitmapDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder) 物件。
3.  呼叫 [**IWICBitmapDecoder：： GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframe) 方法，以取得影像框架的 [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) 介面。
4.  呼叫 [**IWICBitmapSource：： GetPixelFormat**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-getpixelformat) 方法 ([**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) 介面繼承自 [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource)) ，以取得影像的像素格式。
5.  根據下表，將像素格式轉換為 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 類型：

    | WIC 像素格式                                  | 相等的 [ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) |
    |---------------------------------------------------|---------------------------------------------------------|
    | GUID \_ WICPixelFormat128bppRGBAFloat               | DXGI \_ 格式 \_ R32G32B32A32 \_ FLOAT                       |
    | GUID \_ WICPixelFormat64bppRGBAHalf                 | DXGI \_ 格式 \_ R16G16B16A16 \_ FLOAT                       |
    | GUID \_ WICPixelFormat64bppRGBA                     | DXGI \_ 格式 \_ R16G16B16A16 \_ UNORM                       |
    | GUID \_ WICPixelFormat32bppRGBA                     | DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM                           |
    | GUID \_ WICPixelFormat32bppBGRA                     | DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM (DXGI 1.1)                 |
    | GUID \_ WICPixelFormat32bppBGR                      | DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM (DXGI 1.1)                 |
    | GUID \_ WICPixelFormat32bppRGBA1010102XR            | DXGI \_ 格式 \_ R10G10B10 \_ XR \_ 偏差 \_ A2 \_ UNORM (DXGI 1.1)  |
    | GUID \_ WICPixelFormat32bppRGBA1010102              | DXGI \_ 格式 \_ R10G10B10A2 \_ UNORM                        |
    | GUID \_ WICPixelFormat32bppRGBE                     | DXGI \_ 格式 \_ R9G9B9E5 \_ SHAREDEXP                       |
    | GUID \_ WICPixelFormat16bppBGRA5551                 | DXGI \_ 格式 \_ B5G5R5A1 \_ UNORM (DXGI 1.2)                 |
    | GUID \_ WICPixelFormat16bppBGR565                   | DXGI \_ 格式 \_ B5G6R5 \_ UNORM (DXGI 1.2)                   |
    | GUID \_ WICPixelFormat32bppGrayFloat                | DXGI \_ 格式 \_ R32 \_ FLOAT\*                              |
    | GUID \_ WICPixelFormat16bppGrayHalf                 | DXGI \_ 格式 \_ R16 \_ FLOAT\*                              |
    | GUID \_ WICPixelFormat16bppGray                     | DXGI \_ 格式 \_ R16 \_ UNORM\*                              |
    | GUID \_ WICPixelFormat8bppGray                      | DXGI \_ 格式 \_ R8 \_ UNORM\*                               |
    | GUID \_ WICPixelFormat8bppAlpha                     | DXGI \_ 格式 \_ A8 \_ UNORM                                 |
    | GUID \_ WICPixelFormat96bppRGBFloat (Windows 8 WIC)  | DXGI \_ 格式 \_ R32G32B32 \_ FLOAT                          |

    

     

    \* 單一通道 DXGI 格式是紅色通道，因此您需要 HLSL 著色器 swizzles，例如 rrr 將這些格式轉譯為灰階。

6.  呼叫 [**IWICBitmapSource：： CopyPixels**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels) 方法，將影像圖元複製到緩衝區。 使用 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 類型和緩衝區來初始化2d 材質資源和著色器資源檢視物件。
7.  呼叫 [**ID3D11Device：： CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) 方法，以初始化2d 材質資源。 在此呼叫中，傳遞 [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) 介面指標的位址。

    ```C++
        // Create texture
        D3D11_TEXTURE2D_DESC desc;
        desc.Width = width;
        desc.Height = height;
        desc.MipLevels = 1;
        desc.ArraySize = 1;
        desc.Format = format;
        desc.SampleDesc.Count = 1;
        desc.SampleDesc.Quality = 0;
        desc.Usage = D3D11_USAGE_DEFAULT;
        desc.BindFlags = D3D11_BIND_SHADER_RESOURCE;
        desc.CPUAccessFlags = 0;
        desc.MiscFlags = 0;

        D3D11_SUBRESOURCE_DATA initData;
        initData.pSysMem = temp.get();
        initData.SysMemPitch = static_cast<UINT>( rowPitch );
        initData.SysMemSlicePitch = static_cast<UINT>( imageSize );

        ID3D11Texture2D* tex = nullptr;
        hr = d3dDevice->CreateTexture2D( &desc, &initData, &tex );
    
    ```

    

8.  呼叫 [**ID3D11Device：： CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview) 方法，以初始化著色器-資源檢視物件。 傳遞 **Null** 著色器-資源檢視描述 (，以取得具有預設參數的視圖) 或非 **Null** 著色器-資源檢視描述 (取得具有非預設參數) 的視圖。 如有必要，藉由呼叫 [**ID3D11Resource：： GetType**](/windows/desktop/api/D3D11/nf-d3d11-id3d11resource-gettype) 和材質格式（藉由呼叫 [**ID3D11ShaderResourceView：： GetDesc**](/windows/desktop/api/D3D11/nf-d3d11-id3d11shaderresourceview-getdesc)）來判斷紋理類型。
    ```C++
        if ( SUCCEEDED(hr) && tex != 0 )
        {
            if (textureView != 0)
            {
                D3D11_SHADER_RESOURCE_VIEW_DESC SRVDesc;
                memset( &SRVDesc, 0, sizeof( SRVDesc ) );
                SRVDesc.Format = format;
                SRVDesc.ViewDimension = D3D11_SRV_DIMENSION_TEXTURE2D;
                SRVDesc.Texture2D.MipLevels = 1;

                hr = d3dDevice->CreateShaderResourceView( tex, &SRVDesc, textureView );
                if ( FAILED(hr) )
                {
                    tex->Release();
                    return hr;
                }
            }
       }
    ```

    

上述範例程式碼假設 *d3dDevice* 變數是先前已初始化的 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 物件。

以下是您可以包含在應用程式中的標頭。 標頭會宣告 **CreateWICTextureFromFile** 和 **CreateWICTextureFromMemory** 函式，您可以在應用程式中呼叫這些函式，以從檔案和記憶體建立紋理。


```C++
//--------------------------------------------------------------------------------------
// File: WICTextureLoader.h
//
// Function for loading a WIC image and creating a Direct3D 11 runtime texture for it
// (auto-generating mipmaps if possible)
//
// Note: Assumes application has already called CoInitializeEx
//
// Warning: CreateWICTexture* functions are not thread-safe if given a d3dContext instance for
//          auto-gen mipmap support.
//
// Note these functions are useful for images created as simple 2D textures. For
// more complex resources, DDSTextureLoader is an excellent light-weight runtime loader.
// For a full-featured DDS file reader, writer, and texture processing pipeline see
// the 'Texconv' sample and the 'DirectXTex' library.
//
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved.
//
// https://go.microsoft.com/fwlink/?LinkId=248926
// https://go.microsoft.com/fwlink/?LinkId=248929
//--------------------------------------------------------------------------------------

#ifdef _MSC_VER
#pragma once
#endif

#include <d3d11.h>

#pragma warning(push)
#pragma warning(disable : 4005)
#include <stdint.h>
#pragma warning(pop)

HRESULT CreateWICTextureFromMemory( _In_ ID3D11Device* d3dDevice,
                                    _In_opt_ ID3D11DeviceContext* d3dContext,
                                    _In_bytecount_(wicDataSize) const uint8_t* wicData,
                                    _In_ size_t wicDataSize,
                                    _Out_opt_ ID3D11Resource** texture,
                                    _Out_opt_ ID3D11ShaderResourceView** textureView,
                                    _In_ size_t maxsize = 0
                                  );

HRESULT CreateWICTextureFromFile( _In_ ID3D11Device* d3dDevice,
                                  _In_opt_ ID3D11DeviceContext* d3dContext,
                                  _In_z_ const wchar_t* szFileName,
                                  _Out_opt_ ID3D11Resource** texture,
                                  _Out_opt_ ID3D11ShaderResourceView** textureView,
                                  _In_ size_t maxsize = 0
                                );
```



以下是您可以在應用程式中使用的完整來源。 來源會執行 **CreateWICTextureFromFile** 和 **CreateWICTextureFromMemory** 函數。


```C++
//--------------------------------------------------------------------------------------
// File: WICTextureLoader.cpp
//
// Function for loading a WIC image and creating a Direct3D 11 runtime texture for it
// (auto-generating mipmaps if possible)
//
// Note: Assumes application has already called CoInitializeEx
//
// Warning: CreateWICTexture* functions are not thread-safe if given a d3dContext instance for
//          auto-gen mipmap support.
//
// Note these functions are useful for images created as simple 2D textures. For
// more complex resources, DDSTextureLoader is an excellent light-weight runtime loader.
// For a full-featured DDS file reader, writer, and texture processing pipeline see
// the 'Texconv' sample and the 'DirectXTex' library.
//
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved.
//
// https://go.microsoft.com/fwlink/?LinkId=248926
// https://go.microsoft.com/fwlink/?LinkId=248929
//--------------------------------------------------------------------------------------

// We could load multi-frame images (TIFF/GIF) into a texture array.
// For now, we just load the first frame (note: DirectXTex supports multi-frame images)

#include <dxgiformat.h>
#include <assert.h>

#pragma warning(push)
#pragma warning(disable : 4005)
#include <wincodec.h>
#pragma warning(pop)

#include <memory>

#include "WICTextureLoader.h"

#if (_WIN32_WINNT >= 0x0602 /*_WIN32_WINNT_WIN8*/) && !defined(DXGI_1_2_FORMATS)
#define DXGI_1_2_FORMATS
#endif

//---------------------------------------------------------------------------------
template<class T> class ScopedObject
{
public:
    explicit ScopedObject( T *p = 0 ) : _pointer(p) {}
    ~ScopedObject()
    {
        if ( _pointer )
        {
            _pointer->Release();
            _pointer = nullptr;
        }
    }

    bool IsNull() const { return (!_pointer); }

    T& operator*() { return *_pointer; }
    T* operator->() { return _pointer; }
    T** operator&() { return &_pointer; }

    void Reset(T *p = 0) { if ( _pointer ) { _pointer->Release(); } _pointer = p; }

    T* Get() const { return _pointer; }

private:
    ScopedObject(const ScopedObject&);
    ScopedObject& operator=(const ScopedObject&);
        
    T* _pointer;
};

//-------------------------------------------------------------------------------------
// WIC Pixel Format Translation Data
//-------------------------------------------------------------------------------------
struct WICTranslate
{
    GUID                wic;
    DXGI_FORMAT         format;
};

static WICTranslate g_WICFormats[] = 
{
    { GUID_WICPixelFormat128bppRGBAFloat,       DXGI_FORMAT_R32G32B32A32_FLOAT },

    { GUID_WICPixelFormat64bppRGBAHalf,         DXGI_FORMAT_R16G16B16A16_FLOAT },
    { GUID_WICPixelFormat64bppRGBA,             DXGI_FORMAT_R16G16B16A16_UNORM },

    { GUID_WICPixelFormat32bppRGBA,             DXGI_FORMAT_R8G8B8A8_UNORM },
    { GUID_WICPixelFormat32bppBGRA,             DXGI_FORMAT_B8G8R8A8_UNORM }, // DXGI 1.1
    { GUID_WICPixelFormat32bppBGR,              DXGI_FORMAT_B8G8R8X8_UNORM }, // DXGI 1.1

    { GUID_WICPixelFormat32bppRGBA1010102XR,    DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM }, // DXGI 1.1
    { GUID_WICPixelFormat32bppRGBA1010102,      DXGI_FORMAT_R10G10B10A2_UNORM },
    { GUID_WICPixelFormat32bppRGBE,             DXGI_FORMAT_R9G9B9E5_SHAREDEXP },

#ifdef DXGI_1_2_FORMATS

    { GUID_WICPixelFormat16bppBGRA5551,         DXGI_FORMAT_B5G5R5A1_UNORM },
    { GUID_WICPixelFormat16bppBGR565,           DXGI_FORMAT_B5G6R5_UNORM },

#endif // DXGI_1_2_FORMATS

    { GUID_WICPixelFormat32bppGrayFloat,        DXGI_FORMAT_R32_FLOAT },
    { GUID_WICPixelFormat16bppGrayHalf,         DXGI_FORMAT_R16_FLOAT },
    { GUID_WICPixelFormat16bppGray,             DXGI_FORMAT_R16_UNORM },
    { GUID_WICPixelFormat8bppGray,              DXGI_FORMAT_R8_UNORM },

    { GUID_WICPixelFormat8bppAlpha,             DXGI_FORMAT_A8_UNORM },

#if (_WIN32_WINNT >= 0x0602 /*_WIN32_WINNT_WIN8*/)
    { GUID_WICPixelFormat96bppRGBFloat,         DXGI_FORMAT_R32G32B32_FLOAT },
#endif
};

//-------------------------------------------------------------------------------------
// WIC Pixel Format nearest conversion table
//-------------------------------------------------------------------------------------

struct WICConvert
{
    GUID        source;
    GUID        target;
};

static WICConvert g_WICConvert[] = 
{
    // Note target GUID in this conversion table must be one of those directly supported formats (above).

    { GUID_WICPixelFormatBlackWhite,            GUID_WICPixelFormat8bppGray }, // DXGI_FORMAT_R8_UNORM

    { GUID_WICPixelFormat1bppIndexed,           GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM 
    { GUID_WICPixelFormat2bppIndexed,           GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM 
    { GUID_WICPixelFormat4bppIndexed,           GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM 
    { GUID_WICPixelFormat8bppIndexed,           GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM 

    { GUID_WICPixelFormat2bppGray,              GUID_WICPixelFormat8bppGray }, // DXGI_FORMAT_R8_UNORM 
    { GUID_WICPixelFormat4bppGray,              GUID_WICPixelFormat8bppGray }, // DXGI_FORMAT_R8_UNORM 

    { GUID_WICPixelFormat16bppGrayFixedPoint,   GUID_WICPixelFormat16bppGrayHalf }, // DXGI_FORMAT_R16_FLOAT 
    { GUID_WICPixelFormat32bppGrayFixedPoint,   GUID_WICPixelFormat32bppGrayFloat }, // DXGI_FORMAT_R32_FLOAT 

#ifdef DXGI_1_2_FORMATS

    { GUID_WICPixelFormat16bppBGR555,           GUID_WICPixelFormat16bppBGRA5551 }, // DXGI_FORMAT_B5G5R5A1_UNORM

#else

    { GUID_WICPixelFormat16bppBGR555,           GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM
    { GUID_WICPixelFormat16bppBGRA5551,         GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM
    { GUID_WICPixelFormat16bppBGR565,           GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM

#endif // DXGI_1_2_FORMATS

    { GUID_WICPixelFormat32bppBGR101010,        GUID_WICPixelFormat32bppRGBA1010102 }, // DXGI_FORMAT_R10G10B10A2_UNORM

    { GUID_WICPixelFormat24bppBGR,              GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM 
    { GUID_WICPixelFormat24bppRGB,              GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM 
    { GUID_WICPixelFormat32bppPBGRA,            GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM 
    { GUID_WICPixelFormat32bppPRGBA,            GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM 

    { GUID_WICPixelFormat48bppRGB,              GUID_WICPixelFormat64bppRGBA }, // DXGI_FORMAT_R16G16B16A16_UNORM
    { GUID_WICPixelFormat48bppBGR,              GUID_WICPixelFormat64bppRGBA }, // DXGI_FORMAT_R16G16B16A16_UNORM
    { GUID_WICPixelFormat64bppBGRA,             GUID_WICPixelFormat64bppRGBA }, // DXGI_FORMAT_R16G16B16A16_UNORM
    { GUID_WICPixelFormat64bppPRGBA,            GUID_WICPixelFormat64bppRGBA }, // DXGI_FORMAT_R16G16B16A16_UNORM
    { GUID_WICPixelFormat64bppPBGRA,            GUID_WICPixelFormat64bppRGBA }, // DXGI_FORMAT_R16G16B16A16_UNORM

    { GUID_WICPixelFormat48bppRGBFixedPoint,    GUID_WICPixelFormat64bppRGBAHalf }, // DXGI_FORMAT_R16G16B16A16_FLOAT 
    { GUID_WICPixelFormat48bppBGRFixedPoint,    GUID_WICPixelFormat64bppRGBAHalf }, // DXGI_FORMAT_R16G16B16A16_FLOAT 
    { GUID_WICPixelFormat64bppRGBAFixedPoint,   GUID_WICPixelFormat64bppRGBAHalf }, // DXGI_FORMAT_R16G16B16A16_FLOAT 
    { GUID_WICPixelFormat64bppBGRAFixedPoint,   GUID_WICPixelFormat64bppRGBAHalf }, // DXGI_FORMAT_R16G16B16A16_FLOAT 
    { GUID_WICPixelFormat64bppRGBFixedPoint,    GUID_WICPixelFormat64bppRGBAHalf }, // DXGI_FORMAT_R16G16B16A16_FLOAT 
    { GUID_WICPixelFormat64bppRGBHalf,          GUID_WICPixelFormat64bppRGBAHalf }, // DXGI_FORMAT_R16G16B16A16_FLOAT 
    { GUID_WICPixelFormat48bppRGBHalf,          GUID_WICPixelFormat64bppRGBAHalf }, // DXGI_FORMAT_R16G16B16A16_FLOAT 

    { GUID_WICPixelFormat96bppRGBFixedPoint,    GUID_WICPixelFormat128bppRGBAFloat }, // DXGI_FORMAT_R32G32B32A32_FLOAT 
    { GUID_WICPixelFormat128bppPRGBAFloat,      GUID_WICPixelFormat128bppRGBAFloat }, // DXGI_FORMAT_R32G32B32A32_FLOAT 
    { GUID_WICPixelFormat128bppRGBFloat,        GUID_WICPixelFormat128bppRGBAFloat }, // DXGI_FORMAT_R32G32B32A32_FLOAT 
    { GUID_WICPixelFormat128bppRGBAFixedPoint,  GUID_WICPixelFormat128bppRGBAFloat }, // DXGI_FORMAT_R32G32B32A32_FLOAT 
    { GUID_WICPixelFormat128bppRGBFixedPoint,   GUID_WICPixelFormat128bppRGBAFloat }, // DXGI_FORMAT_R32G32B32A32_FLOAT 

    { GUID_WICPixelFormat32bppCMYK,             GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM 
    { GUID_WICPixelFormat64bppCMYK,             GUID_WICPixelFormat64bppRGBA }, // DXGI_FORMAT_R16G16B16A16_UNORM
    { GUID_WICPixelFormat40bppCMYKAlpha,        GUID_WICPixelFormat64bppRGBA }, // DXGI_FORMAT_R16G16B16A16_UNORM
    { GUID_WICPixelFormat80bppCMYKAlpha,        GUID_WICPixelFormat64bppRGBA }, // DXGI_FORMAT_R16G16B16A16_UNORM

#if (_WIN32_WINNT >= 0x0602 /*_WIN32_WINNT_WIN8*/)
    { GUID_WICPixelFormat32bppRGB,              GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM
    { GUID_WICPixelFormat64bppRGB,              GUID_WICPixelFormat64bppRGBA }, // DXGI_FORMAT_R16G16B16A16_UNORM
    { GUID_WICPixelFormat64bppPRGBAHalf,        GUID_WICPixelFormat64bppRGBAHalf }, // DXGI_FORMAT_R16G16B16A16_FLOAT 
#endif

    // We don't support n-channel formats
};

//--------------------------------------------------------------------------------------
static IWICImagingFactory* _GetWIC()
{
    static IWICImagingFactory* s_Factory = nullptr;

    if ( s_Factory )
        return s_Factory;

    HRESULT hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        nullptr,
        CLSCTX_INPROC_SERVER,
        __uuidof(IWICImagingFactory),
        (LPVOID*)&s_Factory
        );

    if ( FAILED(hr) )
    {
        s_Factory = nullptr;
        return nullptr;
    }

    return s_Factory;
}

//---------------------------------------------------------------------------------
static DXGI_FORMAT _WICToDXGI( const GUID& guid )
{
    for( size_t i=0; i < _countof(g_WICFormats); ++i )
    {
        if ( memcmp( &g_WICFormats[i].wic, &guid, sizeof(GUID) ) == 0 )
            return g_WICFormats[i].format;
    }

    return DXGI_FORMAT_UNKNOWN;
}

//---------------------------------------------------------------------------------
static size_t _WICBitsPerPixel( REFGUID targetGuid )
{
    IWICImagingFactory* pWIC = _GetWIC();
    if ( !pWIC )
        return 0;
 
    ScopedObject<IWICComponentInfo> cinfo;
    if ( FAILED( pWIC->CreateComponentInfo( targetGuid, &cinfo ) ) )
        return 0;

    WICComponentType type;
    if ( FAILED( cinfo->GetComponentType( &type ) ) )
        return 0;

    if ( type != WICPixelFormat )
        return 0;

    ScopedObject<IWICPixelFormatInfo> pfinfo;
    if ( FAILED( cinfo->QueryInterface( __uuidof(IWICPixelFormatInfo), reinterpret_cast<void**>( &pfinfo )  ) ) )
        return 0;

    UINT bpp;
    if ( FAILED( pfinfo->GetBitsPerPixel( &bpp ) ) )
        return 0;

    return bpp;
}

//---------------------------------------------------------------------------------
static HRESULT CreateTextureFromWIC( _In_ ID3D11Device* d3dDevice,
                                     _In_opt_ ID3D11DeviceContext* d3dContext,
                                     _In_ IWICBitmapFrameDecode *frame,
                                     _Out_opt_ ID3D11Resource** texture,
                                     _Out_opt_ ID3D11ShaderResourceView** textureView,
                                     _In_ size_t maxsize )
{
    UINT width, height;
    HRESULT hr = frame->GetSize( &width, &height );
    if ( FAILED(hr) )
        return hr;

    assert( width > 0 && height > 0 );

    if ( !maxsize )
    {
        // This is a bit conservative because the hardware could support larger textures than
        // the Feature Level defined minimums, but doing it this way is much easier and more
        // performant for WIC than the 'fail and retry' model used by DDSTextureLoader

        switch( d3dDevice->GetFeatureLevel() )
        {
            case D3D_FEATURE_LEVEL_9_1:
            case D3D_FEATURE_LEVEL_9_2:
                maxsize = 2048 /*D3D_FL9_1_REQ_TEXTURE2D_U_OR_V_DIMENSION*/;
                break;

            case D3D_FEATURE_LEVEL_9_3:
                maxsize = 4096 /*D3D_FL9_3_REQ_TEXTURE2D_U_OR_V_DIMENSION*/;
                break;

            case D3D_FEATURE_LEVEL_10_0:
            case D3D_FEATURE_LEVEL_10_1:
                maxsize = 8192 /*D3D10_REQ_TEXTURE2D_U_OR_V_DIMENSION*/;
                break;

            default:
                maxsize = D3D11_REQ_TEXTURE2D_U_OR_V_DIMENSION;
                break;
        }
    }

    assert( maxsize > 0 );

    UINT twidth, theight;
    if ( width > maxsize || height > maxsize )
    {
        float ar = static_cast<float>(height) / static_cast<float>(width);
        if ( width > height )
        {
            twidth = static_cast<UINT>( maxsize );
            theight = static_cast<UINT>( static_cast<float>(maxsize) * ar );
        }
        else
        {
            theight = static_cast<UINT>( maxsize );
            twidth = static_cast<UINT>( static_cast<float>(maxsize) / ar );
        }
        assert( twidth <= maxsize && theight <= maxsize );
    }
    else
    {
        twidth = width;
        theight = height;
    }

    // Determine format
    WICPixelFormatGUID pixelFormat;
    hr = frame->GetPixelFormat( &pixelFormat );
    if ( FAILED(hr) )
        return hr;

    WICPixelFormatGUID convertGUID;
    memcpy( &convertGUID, &pixelFormat, sizeof(WICPixelFormatGUID) );

    size_t bpp = 0;

    DXGI_FORMAT format = _WICToDXGI( pixelFormat );
    if ( format == DXGI_FORMAT_UNKNOWN )
    {
        for( size_t i=0; i < _countof(g_WICConvert); ++i )
        {
            if ( memcmp( &g_WICConvert[i].source, &pixelFormat, sizeof(WICPixelFormatGUID) ) == 0 )
            {
                memcpy( &convertGUID, &g_WICConvert[i].target, sizeof(WICPixelFormatGUID) );

                format = _WICToDXGI( g_WICConvert[i].target );
                assert( format != DXGI_FORMAT_UNKNOWN );
                bpp = _WICBitsPerPixel( convertGUID );
                break;
            }
        }

        if ( format == DXGI_FORMAT_UNKNOWN )
            return HRESULT_FROM_WIN32( ERROR_NOT_SUPPORTED );
    }
    else
    {
        bpp = _WICBitsPerPixel( pixelFormat );
    }

    if ( !bpp )
        return E_FAIL;

    // Verify our target format is supported by the current device
    // (handles WDDM 1.0 or WDDM 1.1 device driver cases as well as DirectX 11.0 Runtime without 16bpp format support)
    UINT support = 0;
    hr = d3dDevice->CheckFormatSupport( format, &support );
    if ( FAILED(hr) || !(support & D3D11_FORMAT_SUPPORT_TEXTURE2D) )
    {
        // Fallback to RGBA 32-bit format which is supported by all devices
        memcpy( &convertGUID, &GUID_WICPixelFormat32bppRGBA, sizeof(WICPixelFormatGUID) );
        format = DXGI_FORMAT_R8G8B8A8_UNORM;
        bpp = 32;
    }

    // Allocate temporary memory for image
    size_t rowPitch = ( twidth * bpp + 7 ) / 8;
    size_t imageSize = rowPitch * theight;

    std::unique_ptr<uint8_t[]> temp( new uint8_t[ imageSize ] );

    // Load image data
    if ( memcmp( &convertGUID, &pixelFormat, sizeof(GUID) ) == 0
         && twidth == width
         && theight == height )
    {
        // No format conversion or resize needed
        hr = frame->CopyPixels( 0, static_cast<UINT>( rowPitch ), static_cast<UINT>( imageSize ), temp.get() );  
        if ( FAILED(hr) )
            return hr;
    }
    else if ( twidth != width || theight != height )
    {
        // Resize
        IWICImagingFactory* pWIC = _GetWIC();
        if ( !pWIC )
            return E_NOINTERFACE;

        ScopedObject<IWICBitmapScaler> scaler;
        hr = pWIC->CreateBitmapScaler( &scaler );
        if ( FAILED(hr) )
            return hr;

        hr = scaler->Initialize( frame, twidth, theight, WICBitmapInterpolationModeFant );
        if ( FAILED(hr) )
            return hr;

        WICPixelFormatGUID pfScaler;
        hr = scaler->GetPixelFormat( &pfScaler );
        if ( FAILED(hr) )
            return hr;

        if ( memcmp( &convertGUID, &pfScaler, sizeof(GUID) ) == 0 )
        {
            // No format conversion needed
            hr = scaler->CopyPixels( 0, static_cast<UINT>( rowPitch ), static_cast<UINT>( imageSize ), temp.get() );  
            if ( FAILED(hr) )
                return hr;
        }
        else
        {
            ScopedObject<IWICFormatConverter> FC;
            hr = pWIC->CreateFormatConverter( &FC );
            if ( FAILED(hr) )
                return hr;

            hr = FC->Initialize( scaler.Get(), convertGUID, WICBitmapDitherTypeErrorDiffusion, 0, 0, WICBitmapPaletteTypeCustom );
            if ( FAILED(hr) )
                return hr;

            hr = FC->CopyPixels( 0, static_cast<UINT>( rowPitch ), static_cast<UINT>( imageSize ), temp.get() );  
            if ( FAILED(hr) )
                return hr;
        }
    }
    else
    {
        // Format conversion but no resize
        IWICImagingFactory* pWIC = _GetWIC();
        if ( !pWIC )
            return E_NOINTERFACE;

        ScopedObject<IWICFormatConverter> FC;
        hr = pWIC->CreateFormatConverter( &FC );
        if ( FAILED(hr) )
            return hr;

        hr = FC->Initialize( frame, convertGUID, WICBitmapDitherTypeErrorDiffusion, 0, 0, WICBitmapPaletteTypeCustom );
        if ( FAILED(hr) )
            return hr;

        hr = FC->CopyPixels( 0, static_cast<UINT>( rowPitch ), static_cast<UINT>( imageSize ), temp.get() );  
        if ( FAILED(hr) )
            return hr;
    }

    // See if format is supported for auto-gen mipmaps (varies by feature level)
    bool autogen = false;
    if ( d3dContext != 0 && textureView != 0 ) // Must have context and shader-view to auto generate mipmaps
    {
        UINT fmtSupport = 0;
        hr = d3dDevice->CheckFormatSupport( format, &fmtSupport );
        if ( SUCCEEDED(hr) && ( fmtSupport & D3D11_FORMAT_SUPPORT_MIP_AUTOGEN ) )
        {
            autogen = true;
        }
    }

    // Create texture
    D3D11_TEXTURE2D_DESC desc;
    desc.Width = twidth;
    desc.Height = theight;
    desc.MipLevels = (autogen) ? 0 : 1;
    desc.ArraySize = 1;
    desc.Format = format;
    desc.SampleDesc.Count = 1;
    desc.SampleDesc.Quality = 0;
    desc.Usage = D3D11_USAGE_DEFAULT;
    desc.BindFlags = (autogen) ? (D3D11_BIND_SHADER_RESOURCE | D3D11_BIND_RENDER_TARGET) : (D3D11_BIND_SHADER_RESOURCE);
    desc.CPUAccessFlags = 0;
    desc.MiscFlags = (autogen) ? D3D11_RESOURCE_MISC_GENERATE_MIPS : 0;

    D3D11_SUBRESOURCE_DATA initData;
    initData.pSysMem = temp.get();
    initData.SysMemPitch = static_cast<UINT>( rowPitch );
    initData.SysMemSlicePitch = static_cast<UINT>( imageSize );

    ID3D11Texture2D* tex = nullptr;
    hr = d3dDevice->CreateTexture2D( &desc, (autogen) ? nullptr : &initData, &tex );
    if ( SUCCEEDED(hr) && tex != 0 )
    {
        if (textureView != 0)
        {
            D3D11_SHADER_RESOURCE_VIEW_DESC SRVDesc;
            memset( &SRVDesc, 0, sizeof( SRVDesc ) );
            SRVDesc.Format = format;
            SRVDesc.ViewDimension = D3D11_SRV_DIMENSION_TEXTURE2D;
            SRVDesc.Texture2D.MipLevels = (autogen) ? -1 : 1;

            hr = d3dDevice->CreateShaderResourceView( tex, &SRVDesc, textureView );
            if ( FAILED(hr) )
            {
                tex->Release();
                return hr;
            }

            if ( autogen )
            {
                assert( d3dContext != 0 );
                d3dContext->UpdateSubresource( tex, 0, nullptr, temp.get(), static_cast<UINT>(rowPitch), static_cast<UINT>(imageSize) );
                d3dContext->GenerateMips( *textureView );
            }
        }

        if (texture != 0)
        {
            *texture = tex;
        }
        else
        {
#if defined(_DEBUG) || defined(PROFILE)
            tex->SetPrivateData( WKPDID_D3DDebugObjectName,
                                 sizeof("WICTextureLoader")-1,
                                 "WICTextureLoader"
                               );
#endif
            tex->Release();
        }
    }

    return hr;
}

//--------------------------------------------------------------------------------------
HRESULT CreateWICTextureFromMemory( _In_ ID3D11Device* d3dDevice,
                                    _In_opt_ ID3D11DeviceContext* d3dContext,
                                    _In_bytecount_(wicDataSize) const uint8_t* wicData,
                                    _In_ size_t wicDataSize,
                                    _Out_opt_ ID3D11Resource** texture,
                                    _Out_opt_ ID3D11ShaderResourceView** textureView,
                                    _In_ size_t maxsize
                                  )
{
    if (!d3dDevice || !wicData || (!texture && !textureView))
    {
        return E_INVALIDARG;
    }

    if ( !wicDataSize )
    {
        return E_FAIL;
    }

#ifdef _M_AMD64
    if ( wicDataSize > 0xFFFFFFFF )
        return HRESULT_FROM_WIN32( ERROR_FILE_TOO_LARGE );
#endif

    IWICImagingFactory* pWIC = _GetWIC();
    if ( !pWIC )
        return E_NOINTERFACE;

    // Create input stream for memory
    ScopedObject<IWICStream> stream;
    HRESULT hr = pWIC->CreateStream( &stream );
    if ( FAILED(hr) )
        return hr;

    hr = stream->InitializeFromMemory( const_cast<uint8_t*>( wicData ), static_cast<DWORD>( wicDataSize ) );
    if ( FAILED(hr) )
        return hr;

    // Initialize WIC
    ScopedObject<IWICBitmapDecoder> decoder;
    hr = pWIC->CreateDecoderFromStream( stream.Get(), 0, WICDecodeMetadataCacheOnDemand, &decoder );
    if ( FAILED(hr) )
        return hr;

    ScopedObject<IWICBitmapFrameDecode> frame;
    hr = decoder->GetFrame( 0, &frame );
    if ( FAILED(hr) )
        return hr;

    hr = CreateTextureFromWIC( d3dDevice, d3dContext, frame.Get(), texture, textureView, maxsize );
    if ( FAILED(hr)) 
        return hr;

#if defined(_DEBUG) || defined(PROFILE)
    if (texture != 0 && *texture != 0)
    {
        (*texture)->SetPrivateData( WKPDID_D3DDebugObjectName,
                                    sizeof("WICTextureLoader")-1,
                                    "WICTextureLoader"
                                  );
    }

    if (textureView != 0 && *textureView != 0)
    {
        (*textureView)->SetPrivateData( WKPDID_D3DDebugObjectName,
                                        sizeof("WICTextureLoader")-1,
                                        "WICTextureLoader"
                                      );
    }
#endif

    return hr;
}

//--------------------------------------------------------------------------------------
HRESULT CreateWICTextureFromFile( _In_ ID3D11Device* d3dDevice,
                                  _In_opt_ ID3D11DeviceContext* d3dContext,
                                  _In_z_ const wchar_t* fileName,
                                  _Out_opt_ ID3D11Resource** texture,
                                  _Out_opt_ ID3D11ShaderResourceView** textureView,
                                  _In_ size_t maxsize )
{
    if (!d3dDevice || !fileName || (!texture && !textureView))
    {
        return E_INVALIDARG;
    }

    IWICImagingFactory* pWIC = _GetWIC();
    if ( !pWIC )
        return E_NOINTERFACE;

    // Initialize WIC
    ScopedObject<IWICBitmapDecoder> decoder;
    HRESULT hr = pWIC->CreateDecoderFromFilename( fileName, 0, GENERIC_READ, WICDecodeMetadataCacheOnDemand, &decoder );
    if ( FAILED(hr) )
        return hr;

    ScopedObject<IWICBitmapFrameDecode> frame;
    hr = decoder->GetFrame( 0, &frame );
    if ( FAILED(hr) )
        return hr;

    hr = CreateTextureFromWIC( d3dDevice, d3dContext, frame.Get(), texture, textureView, maxsize );
    if ( FAILED(hr)) 
        return hr;

#if defined(_DEBUG) || defined(PROFILE)
    if (texture != 0 || textureView != 0)
    {
        CHAR strFileA[MAX_PATH];
        WideCharToMultiByte( CP_ACP,
                             WC_NO_BEST_FIT_CHARS,
                             fileName,
                             -1,
                             strFileA,
                             MAX_PATH,
                             nullptr,
                             FALSE
                           );
        const CHAR* pstrName = strrchr( strFileA, '\\' );
        if (!pstrName)
        {
            pstrName = strFileA;
        }
        else
        {
            pstrName++;
        }

        if (texture != 0 && *texture != 0)
        {
            (*texture)->SetPrivateData( WKPDID_D3DDebugObjectName,
                                        static_cast<UINT>( strnlen_s(pstrName, MAX_PATH) ),
                                        pstrName
                                      );
        }

        if (textureView != 0 && *textureView != 0 )
        {
            (*textureView)->SetPrivateData( WKPDID_D3DDebugObjectName,
                                            static_cast<UINT>( strnlen_s(pstrName, MAX_PATH) ),
                                            pstrName
                                          );
        }
    }
#endif

    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何使用 Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[紋理](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 