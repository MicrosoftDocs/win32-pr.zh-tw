---
title: 函式屬性
description: '\ 回呼 \ 和 \ 本機 \ 屬性可以套用為函式屬性。'
ms.assetid: 05e19164-072c-4a5a-878d-845273975854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be36cac561a10ae2e1177c29dfc0e1219f650daf26af8154c47cdbd7e3d2bd57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021018"
---
# <a name="function-attributes"></a>函式屬性

**\[**[**回呼**](/windows/desktop/Midl/callback) **\]** 和 **\[** [**本機**](/windows/desktop/Midl/local) **\]** 屬性可以套用為函式屬性。

回呼是從伺服器到用戶端的遠端呼叫，此用戶端會在概念單一執行執行緒中執行。 回呼一律會在遠端呼叫的內容中發出 (或回呼) ，而且是由發出原始遠端呼叫的執行緒 (或回呼) 所執行。

通常最好將本機程式宣告放在 IDL 檔案中，因為這是描述封裝介面的邏輯位置。 **\[** [**Local**](/windows/desktop/Midl/local) **\]** 屬性指出程式聲明實際上不是遠端函式，而是本機程式。 MIDL 編譯器不會為具有 **\[ 區域 \]** 屬性的函式產生任何 stub。

請務必注意， **\[** [](/windows/desktop/Midl/callback) **\]** 不建議在多執行緒程式設計中使用回呼。 作為單一執行緒程式設計功能，它並不支援多執行緒環境所提供的安全性需求。

 

 