---
title: 自動裁剪
description: 自動裁剪
ms.assetid: 9107ee47-52aa-48c8-b141-c821f93fda45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dabc3fd7ece50250ee9e1fea89ff23dd23db533dfcc90d5a939ce1b563ce764
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551234"
---
# <a name="automatic-clipping"></a>自動裁剪

強烈建議 ActiveX 控制容器支援自動裁剪其控制項。 這會讓大部分的控制項更有效率地運作。 如果支援自動裁剪，則必須支援 AutoClip 環境屬性，並將值 **設為 TRUE**。

自動裁剪是容器的功能，可確保控制項的繪製輸出只會傳送至容器目前的裁剪區域。 在支援自動裁剪的容器中，控制項可以繪製，而不考慮其裁剪區域，因為容器會自動剪下在控制項區域以外發生的任何繪製。 如果容器不支援自動裁剪，則 CDK 產生的控制項將會在傳遞非 null 裁剪區域時建立額外的父視窗。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[容器](containers.md)
</dt> </dl>

 

 




