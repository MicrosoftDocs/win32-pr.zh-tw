---
title: 自動裁剪
description: 自動裁剪
ms.assetid: 9107ee47-52aa-48c8-b141-c821f93fda45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71fb39f3a9f15ed6e1e96493ed2cbdd62db40403
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301515"
---
# <a name="automatic-clipping"></a>自動裁剪

強烈建議 ActiveX 控制項容器支援自動裁剪其控制項。 這會讓大部分的控制項更有效率地運作。 如果支援自動裁剪，則必須支援 AutoClip 環境屬性，並將值 **設為 TRUE**。

自動裁剪是容器的功能，可確保控制項的繪製輸出只會傳送至容器目前的裁剪區域。 在支援自動裁剪的容器中，控制項可以繪製，而不考慮其裁剪區域，因為容器會自動剪下在控制項區域以外發生的任何繪製。 如果容器不支援自動裁剪，則 CDK 產生的控制項將會在傳遞非 null 裁剪區域時建立額外的父視窗。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[容器](containers.md)
</dt> </dl>

 

 




