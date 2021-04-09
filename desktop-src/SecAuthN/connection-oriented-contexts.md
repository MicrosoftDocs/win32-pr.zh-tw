---
description: 使用連接導向的內容時，函式的呼叫端會負責格式化訊息。 呼叫端會依賴安全性封裝來驗證連接，並確保訊息特定部分的完整性。
ms.assetid: 82c6b1aa-304c-47f9-8e0f-ad70a89772aa
title: Connection-Oriented 內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fb9430cbcfd0536d18cd5cbd965c9f4a71742eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114937"
---
# <a name="connection-oriented-contexts"></a>Connection-Oriented 內容

使用連接導向的 [*內容*](/windows/desktop/SecGloss/c-gly)時，函式的呼叫端會負責格式化訊息。 呼叫端會依賴 [*安全性封裝*](/windows/desktop/SecGloss/s-gly) 來驗證連接，並確保訊息特定部分的完整性。

大部分的內容選項都可供連接導向的內容使用。 這些選項包括相互驗證、重新執行偵測和順序偵測，如 [內容需求](context-requirements.md)中所述。

安全性套件會設定 SECPKG \_ 旗 \_ 標連線旗標，表示它支援連接導向的語法。

 

 
