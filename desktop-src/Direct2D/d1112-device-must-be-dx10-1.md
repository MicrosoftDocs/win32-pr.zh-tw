---
title: D1112 裝置必須是 DX11 相互作用
ms.assetid: 39dcccaf-db56-402d-b62f-704ad4daf151
description: 與 DXGI 介面相關聯的裝置必須是 D3D11 裝置。
keywords:
- D1112 裝置必須是 DX11 相互作用 Direct2D
topic_type:
- apiref
api_name:
- D1112 Device Must Be DX11
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 24c8bf123d9e00eff90f216676ec03f7d68cbe692511118c36c1433cbf0354d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758108"
---
# <a name="d1112-device-must-be-dx11"></a>D1112：裝置必須是 DX11 相互作用

與 DXGI 介面相關聯的裝置必須是 D3D11 裝置。



| &nbsp;      |  &nbsp; |
|-------------|---------|
| 錯誤層級 | 警告 |



 

## <a name="possible-causes"></a>可能的原因

嘗試使用 [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) 搭配非 Direct3D11 裝置所建立的 DXGI 介面。

 

 




