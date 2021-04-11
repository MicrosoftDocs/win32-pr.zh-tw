---
description: 展示 Api 是一組方法，可控制影響使用者在監視器上看到的裝置狀態。 這些方法包括設定顯示模式，以及用來向使用者呈現影像的每一畫面一次的方法。
ms.assetid: fb2ddc0d-50ac-48aa-8a5c-f232b0f8e7aa
title: " (Direct3D 9) 呈現場景的簡介"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d909f2d7fcc04cd58c27c7598ca8f826b27f48a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317712"
---
# <a name="introduction-to-presenting-a-scene-direct3d-9"></a> (Direct3D 9) 呈現場景的簡介

展示 Api 是一組方法，可控制影響使用者在監視器上看到的裝置狀態。 這些方法包括設定顯示模式，以及用來向使用者呈現影像的每一畫面一次的方法。

-   [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
-   [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
-   [**IDirect3DDevice9::GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
-   [**IDirect3DDevice9::SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
-   [**IDirect3DDevice9::GetRasterStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)

若要瞭解簡報 Api，您必須熟悉下列詞彙。

-   前端緩衝區。 由圖形介面卡轉譯並顯示在監視器或其他輸出裝置上的記憶體矩形。
-   背景緩衝區。 其內容可升級至前端緩衝區的介面。
-   交換鏈。 可連續呈現給前端緩衝區的後置緩衝區集合。 一般而言，全螢幕交換鏈會以 (DDI) 的方式來呈現後續影像，並將設備磁碟機介面替換為視窗中的交換鏈，以提供具有 blitting DDI 的影像。

由於 Direct3D 9 有一個交換鏈作為裝置的屬性，因此每個裝置一律至少有一個交換鏈。 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面具有一組方法，可操作隱含交換鏈，而且是交換鏈本身介面的複本。 應用程式可以建立額外的交換鏈;不過，這對一般的單一視窗或全螢幕應用程式而言並不是必要的。

在 Direct3D 9 中不會直接公開 front 緩衝區。 因此，應用程式無法鎖定或轉譯至前端緩衝區。 如需詳細資訊，請參閱 [ (Direct3D 9) 存取色彩前端緩衝區 ](accessing-the-color-front-buffer.md)。

> [!Note]  
> DirectX 7 提供許多同時呼叫的簡報 Api。 IDirectDraw7：： SetCooperativeLevel、IDirectDraw7：： SetDisplayMode 和 IDirectDraw7：： CreateSurface 序列是很好的範例。 此外，IDirectDrawSurface7：： Flip 和 IDirectDrawSurface7：： Blt 方法會將轉譯的框架傳輸傳送給監視器。 Direct3D 9 將這些 Api 群組折迭成兩種主要方法：重設和呈現。 重設 subsumes SetCooperativeLevel、SetDisplayMode、CreateSurface 和某些要翻轉的參數。 提供 array.blit 的 subsumes flip 和簡報用途。

 

[**IDirect3D9：： CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)的呼叫代表裝置的隱含重設。 Direct3D 9 API 沒有主要表面的概念;您無法建立代表主要表面的物件。 它會被視為裝置的內部屬性。

Gamma 斜坡與交換鏈相關聯，並使用 [**IDirect3DDevice9：： GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) 和 [**IDirect3DDevice9：： SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) 方法來操作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[呈現場景](presenting-a-scene.md)
</dt> </dl>

 

 
