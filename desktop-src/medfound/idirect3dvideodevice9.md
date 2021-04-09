---
description: 使用 DirectX Video 加速 (DXVA) 1.0 版，啟用從 Direct3D 9 裝置進行硬體加速解碼。
ms.assetid: abe3beac-f3f8-413d-8b83-9da3340b19ac
title: 'IDirect3DVideoDevice9 介面 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 89afef6f39b3aa196d8b1013e3d8873e329ce6ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114224"
---
# <a name="idirect3dvideodevice9-interface"></a>IDirect3DVideoDevice9 介面

使用 DirectX Video 加速 (DXVA) 1.0 版，啟用從 Direct3D 9 裝置進行硬體加速解碼。

## <a name="when-to-use"></a>使用時機

此介面不適用於一般應用程式用途。 DirectShow 解碼篩選器應該使用 [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) 介面，而不是 **IDirect3DVideoDevice9**。 影片混合轉譯器的輸入釘 (VMR) 濾波器和覆迭混音器篩選器會公開 **IAMVideoAccelerator**。

## <a name="members"></a>成員

**IDirect3DVideoDevice9** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IDirect3DVideoDevice9** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDirect3DVideoDevice9** 介面具有這些方法。



| 方法                                                                                   | 描述                                                                                                                       |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md)                       | 建立 DXVA 解碼器裝置。<br/>                                                                                         |
| [**CreateSurface**](idirect3dvideodevice9-createsurface.md)                             | 建立 DXVA 解碼的壓縮表面。<br/>                                                                        |
| [**GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) | 取得硬體加速解碼所需之壓縮緩衝區的相關資訊。<br/>                                |
| [**GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md)                               | 取得顯示驅動程式支援的 DXVA 配置檔案清單。<br/>                                             |
| [**GetDXVAInternalInfo**](idirect3dvideodevice9-getdxvainternalinfo.md)                 | 查詢硬體抽象層 (HAL) 將配置給其私用的記憶體數量。 <br/> |
| [**GetUncompressedDXVAFormats**](idirect3dvideodevice9-getuncompresseddxvaformats.md)   | 取得未壓縮像素格式的清單，這些格式可使用指定的 DXVA 設定檔來呈現。<br/>                         |



 

## <a name="remarks"></a>備註

若要取得這個介面的指標，請在 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)或 [**IDirect3DDevice9Ex**](/windows/win32/api/d3d9/nn-d3d9-idirect3ddevice9ex)指標上呼叫 **QueryInterface** 。

這個介面僅支援 DXVA 1.0。 它不支援 DXVA 2.0。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Dxva。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D Video 介面](direct3d-video-interfaces.md)
</dt> <dt>

[DirectX Video 加速2。0](directx-video-acceleration-2-0.md)
</dt> <dt>

[DXVA 1.0 規格](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
