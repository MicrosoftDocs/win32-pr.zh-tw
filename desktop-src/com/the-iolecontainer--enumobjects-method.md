---
title: IOleContainer EnumObjects 方法
description: IOleContainer EnumObjects 方法
ms.assetid: 29562d0e-dc8b-49cd-a58f-1f3125a438ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a2dff2331374299abbc13cdd595aa709ec1aa74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183091"
---
# <a name="the-iolecontainerenumobjects-method"></a>IOleContainer：： EnumObjects 方法

這個方法是用來列舉檔或表單中包含的所有 OLE 物件，並傳回每個 OLE 物件的介面指標。 容器必須傳回每個共用相同容器之 OLE 物件的指標。 您也必須列舉嵌套的表單或嵌套控制項。

某些容器會執行擴充性控制項，以包裝非 ActiveX 控制項，然後將指標傳回至這些擴充項控制項，以列舉表單。 此行為可讓 ActiveX 控制項和 ActiveX 控制項容器妥善整合非 ActiveX 控制項，因此建議使用，但非必要。

 

 




