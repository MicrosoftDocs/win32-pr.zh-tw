---
description: 除了透過 IDirect3DDevice9 介面所擁有和操作的交換鏈之外，應用程式也可以建立額外的交換鏈，以顯示來自相同裝置的多個視圖。
ms.assetid: 4fc09b9c-7adb-4f5d-80e0-2d39bc10420e
title: '以視窗模式呈現多個視圖 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 039b02c487e06c7464dc8163c719371dc2b23706
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510353"
---
# <a name="presenting-multiple-views-in-windowed-mode-direct3d-9"></a>以視窗模式呈現多個視圖 (Direct3D 9) 

除了透過 [**IDirect3DDevice9**](/windows/desktop/api) 介面所擁有和操作的交換鏈之外，應用程式也可以建立額外的交換鏈，以顯示來自相同裝置的多個視圖。 應用程式通常會使用 [**IDirect3DDevice9：： CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) 方法為每個視圖建立一個交換鏈，並將每個交換鏈與特定的視窗產生關聯。 應用程式會將影像轉譯為每個交換鏈的後置緩衝區，然後個別呈現。

每個介面卡一次只能有一個全螢幕的交換鏈。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計秘訣](programming-tips.md)
</dt> </dl>

 

 
