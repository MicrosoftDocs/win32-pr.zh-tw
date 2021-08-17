---
description: 使用者可以在命令提示字元中輸入 netsh interface teredo show state 和檢查輸出，以檢查 Teredo 介面的狀態。
ms.assetid: b6ac1708-fb8a-449b-b30f-c889688a4bac
title: 對等基礎結構和 Teredo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18dfa3fe075d0829358849b3783272aac74e60545c1e58e1d9bf1663738e3721
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794235"
---
# <a name="the-peer-infrastructure-and-teredo"></a>對等基礎結構和 Teredo

使用者可以在命令提示字元中輸入 **netsh interface teredo show state** 和檢查輸出，以檢查 [Teredo](https://msdn.microsoft.com/library/ms819742.aspx)介面的狀態。 如果狀態為「離線」，Teredo 就不會處於作用中狀態，以防止使用者透過其 Teredo 位址連接到其他使用者。 Teredo 可能會離線，因為您的防火牆已停用或不支援 [IPv6](/previous-versions/windows/embedded/ms898970(v=msdn.10))。

 

 
