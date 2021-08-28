---
title: 建立通用控制項
description: 本主題說明如何建立屬於通用控制項程式庫中所定義之視窗類別的視窗 Comctl32.dll。
ms.assetid: BCF25606-5B49-43A5-8107-E7220BE3253C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ddc06def47cef1a34849bbe31bc3871d4c098890bd3ef53830ae6fe7076520
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916338"
---
# <a name="creating-common-controls"></a>建立通用控制項

本主題說明如何建立屬於通用控制項程式庫中所定義之視窗類別的視窗 Comctl32.dll。


最常見的控制項屬於通用控制項 DLL 中定義的視窗類別。 視窗類別和對應的視窗程式會定義控制項的屬性、外觀和行為。 若要確定已載入通用控制項 DLL，請在您的應用程式中包含 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函式。 您可以在呼叫 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式時指定視窗類別的名稱，或在對話方塊範本中指定適當的類別名稱，藉以建立通用控制項。


每種類型的通用控制項都有一組控制項樣式，可用來改變控制項的外觀和行為。 通用控制項程式庫也包含一組控制項樣式，適用于兩種或多種類型的通用控制項。 [ [樣式](common-control-styles.md) ] 區段中描述的通用控制項樣式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於通用控制項](common-controls-intro.md)
</dt> </dl>

 

 