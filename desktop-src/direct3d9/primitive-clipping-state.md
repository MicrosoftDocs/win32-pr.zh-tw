---
description: 部分位於 (或完全外部的原始物件) 視圖的截斷可以裁剪，如此就只會轉譯基本專案的可見部分。
ms.assetid: 096683a4-2d8f-49d3-b1a0-832150907f11
title: " (Direct3D 9) 的基本剪切狀態"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5a305118d8db5c71e0e3cfa97132052777be68
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385837"
---
# <a name="primitive-clipping-state-direct3d-9"></a> (Direct3D 9) 的基本剪切狀態

部分位於 (或完全外部的原始物件) [視圖](viewports-and-clipping.md) 的截斷可以裁剪，如此就只會轉譯基本專案的可見部分。 裁剪會減少只針對可見的基本或部分基本專案所完成的工作量。

若要使用管線進行裁剪，請將 D3DRS \_ 剪切轉譯狀態設為 **TRUE** (預設值) 啟用剪切，或設定為 **FALSE** 以停用 Direct3D 剪切。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯狀態](render-states.md)
</dt> </dl>

 

 



