---
description: '[調色板動畫] 是一種模擬動作的技巧，可快速變更色調色板中選取專案的色彩。'
ms.assetid: fc5b8061-fd4f-4751-883d-877fa32cdfcc
title: 調色板動畫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9761e99033e7a01fa875fce7c41e5a35cf40ab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691847"
---
# <a name="palette-animation"></a>調色板動畫

[調色板動畫] 是一種模擬動作的技巧，可快速變更色調色板中選取專案的色彩。 應用程式可以藉由建立包含 "reserved" 專案的邏輯選擇區，然後使用 [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) 函式來變更這些保留專案中的色彩，來執行調色板動畫。

應用程式會將 [**PALETTEENTRY**](/previous-versions//dd162769(v=vs.85))結構的 **peFlags** 成員設定為電腦保留旗標，以在邏輯調色板中建立保留專案 \_ 。 一旦選取此邏輯元件並實現之後，應用程式就可以呼叫 [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) 函數來變更一或多個保留專案。 如果指定的調色板與使用中視窗相關聯，系統就會立即更新畫面上的色彩。

 

 
