---
title: 無視窗控制項
description: 無視窗控制項
ms.assetid: 1759e5db-423c-44cc-b901-f50046c91956
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf529349a1e1987870b3aac01a69aef3dacbd700d0060cd2177c05479409c7f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991988"
---
# <a name="windowless-controls"></a>無視窗控制項

ActiveX Controls 96 規格包含無視窗控制項的定義。 這類控制項無法在自己的視窗中操作，而且需要容器以提供控制項可能繪製的共用視窗，請參閱 ActiveX SDK。 無視窗控制項的設計是為了與舊版的控制項容器相容，方法是在這種情況下建立自己的視窗，無視窗控制項容器應以傳統方式裝載視窗控制項，而不會有任何問題。 不過，容器可以用來區別可在無視窗模式下運作的控制項，因此定義適當的元件類別目錄，可能會很有用。

CATID-{1D06B600-3AE3-11cf-87B9-00AA006C8166} CATID \_ WindowlessObject

## <a name="related-topics"></a>相關主題

<dl> <dt>

[元件類別](component-categories.md)
</dt> </dl>

 

 




