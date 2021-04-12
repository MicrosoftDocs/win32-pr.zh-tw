---
title: IDWriteFactory2 CreateCustomRenderingParams 方法
description: 使用指定的屬性建立呈現參數物件。
ms.assetid: 947d50fd-888c-2f0b-25c2-b19b0e6fad58
keywords:
- CreateCustomRenderingParams 方法直接寫入
- CreateCustomRenderingParams 方法 Direct Write，IDWriteFactory2 介面
- IDWriteFactory2 介面 Direct Write，CreateCustomRenderingParams 方法
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateCustomRenderingParams
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bd69cde6858061b69b8143dcdd0560342e65f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384929"
---
# <a name="idwritefactory2createcustomrenderingparams-method"></a>IDWriteFactory2：： CreateCustomRenderingParams 方法

使用指定的屬性建立呈現參數物件。

## <a name="syntax"></a>語法


```C++
virtual HRESULT CreateCustomRenderingParams(
        FLOAT                   gamma,
        FLOAT                   enhancedContrast,
        FLOAT                   grayscaleEnhancedContrast,
        FLOAT                   clearTypeLevel,
        DWRITE_PIXEL_GEOMETRY   pixelGeometry,
        DWRITE_RENDERING_MODE   renderingMode,
        DWRITE_GRID_FIT_MODE    gridFitMode,
  [out] IDWriteRenderingParams2 **renderingParams
) = 0;
```



## <a name="parameters"></a>參數

<dl> <dt>

*伽 瑪* 
</dt> <dd>

類型： **FLOAT**

用於 gamma 更正的 gamma 值，必須大於零且不能超過256。

</dd> <dt>

*enhancedContrast* 
</dt> <dd>

類型： **FLOAT**

對比增強功能（零或更大）的數量。

</dd> <dt>

*grayscaleEnhancedContrast* 
</dt> <dd>

類型： **FLOAT**

對比增強功能（零或更大）的數量。

</dd> <dt>

*clearTypeLevel* 
</dt> <dd>

類型： **FLOAT**

ClearType 層級的程度，從 0.0 f (無 ClearType) 到 1.0 f (完整 ClearType) 。

</dd> <dt>

*pixelGeometry* 
</dt> <dd>

類型： **[ **DWRITE \_ 圖元 \_ 幾何**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**

裝置圖元的幾何。

</dd> <dt>

*renderingMode* 
</dt> <dd>

類型： **[ **DWRITE \_ 轉譯 \_ 模式**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**

轉譯字型的方法。 在大多數情況下，這應該是 DWRITE 轉譯 \_ \_ 模式 \_ 預設值，以自動使用適當的模式。

</dd> <dt>

*gridFitMode* 
</dt> <dd>

類型： **[ **DWRITE \_ 格線 \_ 擬合 \_ 模式**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**

如何讓格線符合圖像的輪廓。 在大部分的情況下，這應該是 DWRITE \_ 方格 \_ 符合 \_ 預設值，以自動選擇適當的模式。

</dd> <dt>

*renderingParams* \[擴展\]
</dt> <dd>

類型： **[ **IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***

保存新建立的轉譯參數物件，或如果發生失敗，則為 Null。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                          |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/> |
| 程式庫<br/>                  | <dl> <dt>Dwrite .lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

