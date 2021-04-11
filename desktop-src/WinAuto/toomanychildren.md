---
title: TooManyChildren
description: TooManyChildren
ms.assetid: BF667CDC-C1F9-44B2-B64C-CD7F085CA364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e0eee0c29d0d5ee4cdfe66ee5b61aef4b31b32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183579"
---
# <a name="toomanychildren"></a>TooManyChildren

## <a name="text"></a>Text

在尋找同級之後，已停止尋找其他的同級 {0} 。 可能不正確的樹狀結構

## <a name="type"></a>類型

警告

## <a name="description"></a>描述

專案樹狀結構可能是迴圈，而樹狀結構深度是無限的。

此問題可能會導致自動化工具的導覽問題，因為它們會進入看似迴圈參考或無限迴圈的內容。

## <a name="possible-causes"></a>可能的原因

-   應用程式或控制項設計可能太複雜。 有大量專案的清單視圖控制項可能會報告此警告。 在這些情況下，您通常可以忽略此警告。
-   不正確或不正確 MSAA 執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IAccessible：： accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




