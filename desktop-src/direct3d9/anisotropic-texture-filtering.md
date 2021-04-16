---
description: 在3D 物件的材質中可見的扭曲，其介面面向于螢幕平面的角度，稱為 anisotropy。
ms.assetid: f6c8a9e2-aab0-4f06-956e-bb86557c72e7
title: " (Direct3D 9) 的非等向材質篩選"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3443696e54410c6edc6a9998d4fcfd86b537a0e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468461"
---
# <a name="anisotropic-texture-filtering-direct3d-9"></a> (Direct3D 9) 的非等向材質篩選

在3D 物件的材質中可見的扭曲，其介面面向于螢幕平面的角度，稱為 anisotropy。 當非等向性原始物件的像素對應至材質時，其形狀會失真。 Direct3D 將像素的非等向性測量為延長部分，意即反向對應至紋理空間之螢幕像素的長度除以寬度。

您可搭配使用非等向性紋理篩選與線性紋理篩選或 Mipmap 紋理篩選，以改善轉譯結果。 您的應用程式會藉由呼叫 [**IDirect3DDevice9：： SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) 方法，啟用非等向材質篩選。 將第一個參數的值設定為您要選取材質篩選方法之材質 (0-7) 的整數索引編號。 \_ \_ 針對第二個參數傳遞 D3DSAMP MAGFILTER、D3DSAMP MINFILTER 或 D3DSAMP \_ MIPFILTER，以設定放大、縮制或 mipmap 篩選。 將第三個參數設定為 [D3DTEXF] \_ 。

您的應用程式也必須將 anisotropy 的程度設定為大於1的值。 若要這麼做，請呼叫 [**IDirect3DDevice9：： SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) 方法。 將第一個參數的值設定為您要設定 isotropy 程度之材質 (0-7) 的整數索引編號。 傳遞 D3DSAMP \_ MAXANISOTROPY 做為第二個參數的值。 最後一個參數應該是 isotropy 的程度。

您可以將 isotropy 的程度設定為1，以停用 isotropic 篩選。大於1的值會啟用它。 檢查 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構中的 MaxAnisotropy 旗標，以判斷 anisotropy 程度的可能值範圍。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質篩選](texture-filtering.md)
</dt> </dl>

 

 
