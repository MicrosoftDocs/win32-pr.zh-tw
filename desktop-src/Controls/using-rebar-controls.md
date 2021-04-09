---
title: 使用 Rebar 控制項
description: 本章節包含的主題會示範如何建立和使用 Rebar 控制項。
ms.assetid: b821216f-609e-41a4-8d45-69609f3572bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9174a4ee05b966037bb30be3e796bcc2c3e00da
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683159"
---
# <a name="using-rebar-controls"></a>使用 Rebar 控制項

本章節包含的主題會示範如何建立和使用 Rebar 控制項。

## <a name="in-this-section"></a>本節內容



| 主題                                                                | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [如何建立 Rebar 控制項](create-rebar-controls.md)<br/> | 應用程式會藉由呼叫 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立 Rebar 控制項，並將 [**REBARCLASSNAME**](common-control-window-classes.md) 指定為 window 類別。 應用程式必須先呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函式來註冊視窗類別，並 \_ \_ 在伴隨的 [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) 結構中指定「ICC 非經常性存取類別」位。 <br/> |



 

 

