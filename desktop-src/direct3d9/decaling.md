---
description: Direct3D 應用程式使用印花來控制從特定原始影像繪製到轉譯目標表面上的像素。 應用程式將印花套用至原始物件的影像，以正確地轉譯共面多邊形。
ms.assetid: 0d57983c-c8f3-4095-9495-a3ec5d280bda
title: 'Decaling (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5606bdbc798d8b1e834aff53b04984f659af650
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108752"
---
# <a name="decaling-direct3d-9"></a>Decaling (Direct3D 9) 

Direct3D 應用程式使用印花來控制從特定原始影像繪製到轉譯目標表面上的像素。 應用程式將印花套用至原始物件的影像，以正確地轉譯共面多邊形。

例如：將輪胎標記及黃線畫上道路之後，標記應該要直接出現在道路上方。 但是，標記和道路的 z 值是相同的。 因此，深度緩衝區不一定會在這兩者之間正常分離。 某些後方原始物件的像素可能會轉譯至前方原始物件的上方，反之亦然。 產生的影像似乎在影格間不斷閃爍。 此效果稱為「*z 衝突*」或「*影格閃爍*」。

若要解決這個問題，可使用樣板將後方原始物件上印花出現的區域遮蔽。 關閉 z 緩衝，並將前方原始物件的影像轉譯至轉譯目標表面上已被遮蔽的區域。

雖然您可使用多重紋理混合解決這個問題，如此一來會限制應用程式可產生的其他特殊效果數目。 使用樣板緩衝區套用印花會釋出紋理混合階段供其他效果使用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[樣板緩衝區技術](stencil-buffer-techniques.md)
</dt> </dl>

 

 



