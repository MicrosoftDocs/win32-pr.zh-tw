---
description: Windows Update Agent (WUA) API 是一組 COM 介面，可讓系統管理員和程式設計人員存取 Windows Update 和 Windows Server Update Services (WSUS) 。
ms.assetid: 611dc759-e0fc-472e-bdc2-fb952ba74999
title: Windows更新代理程式 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82e7e2c79a707424128082f8f3123cb5fff506a9fc98203ab1fdf8063393310d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738000"
---
# <a name="windows-update-agent-api"></a>Windows更新代理程式 API

## <a name="purpose"></a>目的

Windows Update Agent (WUA) API 是一組 COM 介面，可讓系統管理員和程式設計人員存取 Windows Update 和[Windows Server Update Services (WSUS) ](/previous-versions/windows/desktop/ms744624(v=vs.85))。 您可以撰寫腳本和程式來檢查目前可供電腦使用的更新，然後您就可以安裝或卸載更新。

## <a name="where-applicable"></a>適用時

系統管理員可以使用 WUA，以程式設計方式判斷應該套用至電腦的更新、下載這些更新，然後在幾乎不需要使用者介入的情況下進行安裝。

獨立軟體廠商 (ISV) 和使用者開發人員可以將 WUA 功能整合到電腦管理或更新管理軟體，以提供順暢的操作環境。

## <a name="developer-audience"></a>開發人員對象

您可以用數種程式設計語言撰寫 WUA 應用程式。 WUA 會定義可從 Visual Basic、Visual Basic 腳本版本 (VBScript) 、JScript 以及 c 和 c + + 存取的介面和物件。 熟悉 COM 程式設計對 WUA 程式設計師很有用。

## <a name="run-time-requirements"></a>執行階段需求求

從 Windows XP 開始支援 WUA。 從 Windows server 2003 開始，伺服器支援 WUA。

## <a name="in-this-section"></a>本節內容

-   [使用 Windows Update 代理程式 API](using-the-windows-update-agent-api.md)
-   [WUA API 參考](windows-update-agent--wua--api-reference.md)

 

 
