---
description: 您的應用程式可利用樣板緩衝區將 2D 或 3D 影像合成為 3D 場景。
ms.assetid: 9233d15d-fa99-41a2-a253-22f5ae5bf788
title: " (Direct3D 9) 的組合"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bca61559d2773bd1e4f7dc345e9ad4c1fb6fcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998052"
---
# <a name="compositing-direct3d-9"></a> (Direct3D 9) 的組合

您的應用程式可利用樣板緩衝區將 2D 或 3D 影像合成為 3D 場景。 樣板緩衝區中的遮罩可用於遮蔽轉譯目標的部分表面區域。 儲存的 2D 資訊 (例如文字或點陣圖) 接著便可寫入遮蔽區域。 或者，您的應用程式也可將其他 3D 原始物件轉譯至轉譯目標表面的樣板遮蔽區域。 甚至可以轉譯整個場景。

通常，遊戲會將多個 3D 場景合成在一起。 例如：競速遊戲通常都會顯示後照鏡。 後照鏡便包含了駕駛後方的 3D 場景。 該檢視基本上就是合成於駕駛前方檢視的第二個 3D 場景。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[樣板緩衝區技術](stencil-buffer-techniques.md)
</dt> </dl>

 

 



