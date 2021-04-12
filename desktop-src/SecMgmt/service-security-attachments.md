---
description: Microsoft Security Configuration tool 組是一組 Microsoft Management Console 的 (MMC) 工具，可簡化系統安全性的設定和分析。
ms.assetid: c6558789-84eb-4998-a2c1-725d8a64d255
title: 服務安全性附件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47cdd0ca3799615125900a3ae6b0b78c26f4abc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318212"
---
# <a name="service-security-attachments"></a>服務安全性附件

Microsoft Security Configuration tool 組是一組 Microsoft Management Console 的 (MMC) 工具，可簡化系統安全性的設定和分析。 不過，有些服務具有特殊的設定需求，而不是標準工具組所提供的安全性設定。 若要處理這些需求，您可以撰寫可處理特定服務安全性工作的附件，以擴充工具集的功能。

例如，多工緩衝處理器是一種 Windows NT 服務，用來定義需要保護的私用物件，例如印表機。 標準工具組不會處理這項功能，因此需要附件來處理印表機物件的設定和分析。 一般安全性參數的設定（例如服務調用原則）仍由安全性設定工具集處理。

安全性服務附件會擴充安全性設定工具集的功能，以支援服務特定的設定。

附件有兩個元件：

-   一個 MMC 嵌入式管理單元延伸模組，可執行附件使用者介面。
-   處理服務特定安全性設定與分析工作的附件引擎。

附件嵌入式管理單元延伸是由安全性設定嵌入式管理單元所主控。這些是 MMC 嵌入式管理單元，可為使用者提供介面來設定及分析服務的一般安全性設定。 服務特定的設定是使用附件嵌入式管理單元擴充功能來設定。

當使用者變更設定時，[安全性設定] 嵌入式管理單元會儲存新的資訊，然後將要求傳遞至安全性設定引擎。 引擎會處理要求，並將服務設定為新的設定。 如果要求會影響標準安全性設定，則會由引擎處理。 如果要求是服務特定的，引擎會呼叫適當的附件引擎來處理要求。

下圖顯示「附件引擎」和「嵌入式管理單元」延伸模組在安全性設定工具集的架構內的運作方式。

![附件引擎和嵌入式管理單元](images/model1a.png)

如需使用 Microsoft 安全性設定工具集的詳細資訊，請使用您慣用的搜尋引擎來搜尋安全性設定。

 

 



