---
description: 使用者可以在命令提示字元中輸入 netsh interface teredo show state 和檢查輸出，以檢查 Teredo 介面的狀態。
ms.assetid: b6ac1708-fb8a-449b-b30f-c889688a4bac
title: 對等基礎結構和 Teredo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2550d8da46339205de60c4a537d03c10940da4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513408"
---
# <a name="the-peer-infrastructure-and-teredo"></a>對等基礎結構和 Teredo

使用者可以在命令提示字元中輸入 **netsh interface teredo show state** 和檢查輸出，以檢查 [Teredo](https://msdn.microsoft.com/library/ms819742.aspx)介面的狀態。 如果狀態為「離線」，Teredo 就不會處於作用中狀態，以防止使用者透過其 Teredo 位址連接到其他使用者。 Teredo 可能會離線，因為您的防火牆已停用或不支援 [IPv6](/previous-versions/windows/embedded/ms898970(v=msdn.10))。

 

 
