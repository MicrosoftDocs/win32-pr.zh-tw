---
description: 全域唯一識別碼 (GUID) 值，可識別 debug 訊息的產生者。
ms.assetid: 85946D30-5E49-4E4B-AC25-394ABFF0DB11
title: 'DXGI_DEBUG_ID (DXGIDebug) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3642f8ece96a7a63ed6137eef14069a33a418511321a4df10cdd95e122e13397
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068818"
---
# <a name="dxgi_debug_id"></a>DXGI \_ DEBUG \_ ID

全域唯一識別碼 (GUID) 值，可識別 debug 訊息的產生者。



| 常數/值                                                                                                                                                                                                                                                                                         | 描述                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_DEBUG_ALL"></span><span id="dxgi_debug_all"></span><dl> <dt>**DXGI \_DEBUG \_ ALL**</dt> <dt>0xe48ae283、0xda80、0x490b、0x87、0xe6、0x43、0xe9、0xa9、0xcf、0xda、0x8</dt> </dl>       | 所有 Direct3D 和 DXGI 物件和私用應用程式。<br/>                                                                                     |
| <span id="DXGI_DEBUG_DX"></span><span id="dxgi_debug_dx"></span><dl> <dt>**DXGI \_DEBUG \_ DX**</dt> <dt>0x35cdd7fc、0x13b2、0x421d、0xa5、0xd7、0x7e、0x44、0x51、0x28、0x7d、0x64</dt> </dl>         | Direct3D 和 DXGI 物件。<br/>                                                                                                          |
| <span id="DXGI_DEBUG_DXGI"></span><span id="dxgi_debug_dxgi"></span><dl> <dt>**DXGI \_DEBUG \_ DXGI**</dt> <dt>0x25cddaa4、0xb1c6、0x47e1、0xac、0x3e、0x98、0x87、0x5b、0x5a、0x2e、0x2a</dt> </dl>   | DXGI.<br/>                                                                                                                               |
| <span id="DXGI_DEBUG_APP"></span><span id="dxgi_debug_app"></span><dl> <dt>**DXGI \_DEBUG \_ APP**</dt> <dt>0x6cd6e01、0x4219、0x4ebd、0x87、0x9、0x27、0xed、0x23、0x36、0xc、0x62</dt> </dl>         | 私用應用程式。 您使用 [**IDXGIInfoQueue：： AddApplicationMessage**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-idxgiinfoqueue-addapplicationmessage)新增的任何訊息。<br/> |
| <span id="DXGI_DEBUG_D3D11"></span><span id="dxgi_debug_d3d11"></span><dl> <dt>**DXGI \_DEBUG \_ D3D11**</dt> <dt>0x4b99317b、0xac39、0x4aa6、0xbb、0xb、0xba、0xa0、0x47、0x84、0x79、0x8f</dt> </dl> | Direct3D 11。 定義于 D3D11SDKLayers 中。<br/>                                                                                           |



## <a name="remarks"></a>備註

使用這些值搭配 [**IDXGIInfoQueue**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue) 介面。

``` syntax
typedef GUID DXGI_DEBUG_ID;

DEFINE_GUID(DXGI_DEBUG_ALL, 0xe48ae283, 0xda80, 0x490b, 0x87, 0xe6, 0x43, 0xe9, 0xa9, 0xcf, 0xda, 0x8);
DEFINE_GUID(DXGI_DEBUG_DX, 0x35cdd7fc, 0x13b2, 0x421d, 0xa5, 0xd7, 0x7e, 0x44, 0x51, 0x28, 0x7d, 0x64);
DEFINE_GUID(DXGI_DEBUG_DXGI, 0x25cddaa4, 0xb1c6, 0x47e1, 0xac, 0x3e, 0x98, 0x87, 0x5b, 0x5a, 0x2e, 0x2a);
DEFINE_GUID(DXGI_DEBUG_APP, 0x6cd6e01, 0x4219, 0x4ebd, 0x87, 0x9, 0x27, 0xed, 0x23, 0x36, 0xc, 0x62);

DEFINE_GUID(DXGI_DEBUG_D3D11, 0x4b99317b, 0xac39, 0x4aa6, 0xbb, 0xb, 0xba, 0xa0, 0x47, 0x84, 0x79, 0x8f);
```

若要使用其中任何一個 GUID 值，請在您的程式碼中包含 DXGIDebug，並連結至 dxguid。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>DXGIDebug。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DXGI 常數](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




