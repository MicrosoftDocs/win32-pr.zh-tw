---
description: 描述建立已簽署訊息時必須完成的工作。
ms.assetid: 61896022-28c2-4f70-977a-c990b4b23c55
title: 建立已簽署的訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f68511c41a10fc0f690574e71c1dfe8a354efbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193459"
---
# <a name="creating-a-signed-message"></a>建立已簽署的訊息

下圖說明建立已簽署訊息時必須完成的工作。 這些步驟如下圖所示。

![簽署訊息](images/signdmsg.png)

**若要建立已簽署的訊息**

1.  視需要建立資料 (，) 並取得其指標。
2.  開啟包含簽署者憑證的 [*憑證存放區*](../secgloss/c-gly.md) 。
3.  取得憑證的 [*私密金鑰*](../secgloss/p-gly.md) 。 在使用憑證之前，必須先在憑證上設定屬性，以將憑證系結至特定的 [*csp*](../secgloss/c-gly.md)，並將該 csp 內的憑證系結至特定的私密金鑰。 這需要設定一次。
4.  選擇摘要作業的雜湊演算法。 我們建議您從可設定的位置選取雜湊演算法，以在不需要變更程式碼的情況下進行更新。
5.  使用雜湊演算法，透過雜湊函數傳送資料，藉此建立資料的 [*雜湊*](../secgloss/h-gly.md) (摘要) 。
6.  使用透過憑證上的屬性取得的 [*私密金鑰*](../secgloss/p-gly.md) ，加密摘要，建立簽章。
7.  在簽署的訊息中包含下列內容：

    -   簽署的資料
    -   雜湊演算法
    -   簽章
    -   簽署者識別碼 (憑證簽發者和序號) 
    -   簽署者的憑證 (選用) 

如需詳細的程式和範例，請參閱 [簽署資料](procedure-for-signing-data.md) 的 [程式和範例 C 程式：簽署訊息和驗證訊息簽](example-c-program-signing-a-message-and-verifying-a-message-signature.md)章。

 

 
