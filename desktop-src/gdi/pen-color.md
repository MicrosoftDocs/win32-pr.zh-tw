---
description: Color 屬性指定畫筆的色彩。
ms.assetid: ce775359-65fc-40d0-8725-b392cc0464a6
title: 畫筆色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e88d73fc80f6fe02a6d9e1de1d33568c94e05768f113c8bee0754c5d8afb418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117886203"
---
# <a name="pen-color"></a>畫筆色彩

Color 屬性指定畫筆的色彩。 應用程式可以使用 [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) 宏儲存紅色、綠色、藍色的三個，以指定 [COLORREF](colorref.md) 結構中所需的色彩，並將此結構的位址傳遞至 [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen)、 [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)或 [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) 函式，以建立具有唯一色彩的表面畫筆。  (股票筆的限制為黑色、白色和不可見 ) 。如需 RGB triplet 和色彩的詳細資訊，請參閱 [色彩](colors.md)。

 

 



