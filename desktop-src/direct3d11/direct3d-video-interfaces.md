---
title: Direct3D Video 介面
description: 本主題列出 Direct3D 9Ex 中可用的 Direct3D video 介面，以及 windows 7 和更新版本的 windows 用戶端作業系統以及 Windows Server 2008 R2 和更新版本的 Windows server 作業系統支援的功能。
ms.assetid: 922AC983-B9C0-494C-BADD-CEF20931FC26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d20c86e172308d4be6f4c6218a110f49b033ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463253"
---
# <a name="direct3d-video-interfaces"></a>Direct3D Video 介面

本主題列出 Direct3D 9Ex 中可用的 Direct3D video 介面，以及 windows 7 和更新版本的 windows 用戶端作業系統以及 Windows Server 2008 R2 和更新版本的 Windows server 作業系統支援的功能。 您可以使用這些介面及其方法，取得圖形驅動程式的影片內容保護功能，以及 Direct3D 裝置的重迭硬體功能。 您也可以使用這些介面及其方法來保護影片內容。 這些介面和其方法都定義于 D3d9 中，並在 [Microsoft 媒體基礎](/windows/desktop/medfound/microsoft-media-foundation-sdk) 一節中描述。



| 介面                                                                                                                                                                                                                             | 描述                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="IDirect3D9ExOverlayExtension"></span><span id="idirect3d9exoverlayextension"></span><span id="IDIRECT3D9EXOVERLAYEXTENSION"></span>[**IDirect3D9ExOverlayExtension**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9exoverlayextension)<br/>           | 查詢 Direct3D 裝置的重迭硬體功能。<br/>                                                     |
| <span id="IDirect3DAuthenticatedChannel9"></span><span id="idirect3dauthenticatedchannel9"></span><span id="IDIRECT3DAUTHENTICATEDCHANNEL9"></span>[**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)<br/> | 提供與圖形驅動程式或 Direct3D 執行時間的通道。<br/>                                  |
| <span id="IDirect3DCryptoSession9"></span><span id="idirect3dcryptosession9"></span><span id="IDIRECT3DCRYPTOSESSION9"></span>[**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)<br/>                                    | 表示用來存取受保護介面的密碼編譯會話。<br/>                                      |
| <span id="IDirect3DDevice9Video"></span><span id="idirect3ddevice9video"></span><span id="IDIRECT3DDEVICE9VIDEO"></span>[**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)<br/>                                              | 讓應用程式使用由圖形驅動程式所執行的內容保護和加密服務。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 11) 的效果 ](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[Direct3D 11 的程式設計指南](dx-graphics-overviews.md)
</dt> </dl>

 

