---
title: IOleContainer EnumObjects 方法
description: IOleContainer EnumObjects 方法
ms.assetid: 29562d0e-dc8b-49cd-a58f-1f3125a438ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbd74e4916eec4d58240f702a09fd8376008fe0bb352113e1512bd2882d8dee9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462318"
---
# <a name="the-iolecontainerenumobjects-method"></a>IOleContainer：： EnumObjects 方法

這個方法是用來列舉檔或表單中包含的所有 OLE 物件，並傳回每個 OLE 物件的介面指標。 容器必須傳回每個共用相同容器之 OLE 物件的指標。 您也必須列舉嵌套的表單或嵌套控制項。

某些容器會執行包裝非 ActiveX 控制項的擴充性控制項，然後將指標傳回至這些擴充項控制項，以列舉表單。 此行為可讓 ActiveX 控制項和 ActiveX 控制容器與非 ActiveX 控制項妥善整合，因此建議使用，但非必要。

 

 




