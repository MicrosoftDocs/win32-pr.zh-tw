---
title: 使用 Rebar 控制項
description: 本章節包含的主題會示範如何建立和使用 Rebar 控制項。
ms.assetid: b821216f-609e-41a4-8d45-69609f3572bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ed7d53fd09c03598b40414a4683a9f278797420f76c85150f63822b53fc793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077822"
---
# <a name="using-rebar-controls"></a>使用 Rebar 控制項

本章節包含的主題會示範如何建立和使用 Rebar 控制項。

## <a name="in-this-section"></a>本節內容



| 主題                                                                | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [如何建立 Rebar 控制項](create-rebar-controls.md)<br/> | 應用程式會藉由呼叫 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立 Rebar 控制項，並將 [**REBARCLASSNAME**](common-control-window-classes.md) 指定為 window 類別。 應用程式必須先呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函式來註冊視窗類別，並 \_ \_ 在伴隨的 [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) 結構中指定「ICC 非經常性存取類別」位。 <br/> |



 

 

