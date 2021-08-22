---
description: 您可以利用樣板緩衝區以獲得更抽象的效果，例如：外框及剪影。
ms.assetid: 8b9cd2b3-c1bf-4ac9-aae5-7fc0c9e049ff
title: " (Direct3D 9) 的大綱與 Silhouettes"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b5fcf26b3f3cbbe6e051e1a7d8517cc6d69044beb6eaed7f54baef3509a748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563408"
---
# <a name="outlines-and-silhouettes-direct3d-9"></a> (Direct3D 9) 的大綱與 Silhouettes

您可以利用樣板緩衝區以獲得更抽象的效果，例如：外框及剪影。

如果應用程式將樣板遮罩套用至形狀相同但略小的基本類型影像，結果影像只包含基本類型影像的外框。 應用程式可以再以單色填滿影像中被樣板遮蔽的區域，給予原始物件浮凸的外觀。

如果樣板遮罩的大小及形狀與您正在轉譯的原始物件相同，產出的影像將會在原先原始物件所在的位置留下一個洞。 您的應用程式可以再以黑色填滿該空洞，產生原始物件的剪影效果。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[樣板緩衝區技術](stencil-buffer-techniques.md)
</dt> </dl>

 

 



