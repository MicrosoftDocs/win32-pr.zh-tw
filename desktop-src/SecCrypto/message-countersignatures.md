---
description: 有時簽署的訊息需要副署。
ms.assetid: de83a9ad-4e88-4477-8c9e-6dd7d5ec9e8f
title: 訊息副署
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8dff2920217dd9a79f917f7b625da3919747d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690740"
---
# <a name="message-countersignatures"></a>訊息副署

有時簽署的訊息需要 [*副署*](../secgloss/c-gly.md)。 例如，使用者 A 可能會將已簽署的資料訊息傳送給使用者 B，要求 B 以檔中包含的條款來確認協定。 使用者 B 會解碼訊息、讀取條款，並在協定中來副署訊息。 然後，副署訊息會傳送回使用者 A。使用者 A 現在知道，而且可以證明該使用者 B 是否同意這些條款。

下表列出的區段包含 message countersigning 的程式描述或 C 程式範例。



| 區段                                                                                                                                 | 目錄                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [訊息函數](cryptography-functions.md)                                                                       | 列出計數器特徵標記功能。                             |
| [Countersigning 訊息](countersigning-a-message.md)                                                                                | 詳細說明計數器簽署訊息的處理常式。                  |
| [驗證副署](verifying-a-countersignature.md)                                                                        | 詳細說明驗證計數器簽章的程式。           |
| [驗證已簽署的訊息](verifying-a-signed-message.md)                                                                            | 詳細說明在已簽署的訊息上驗證簽章的流程。 |
| [範例 C 程式：編碼和解碼副署訊息](example-c-program-encoding-and-decoding-a-countersigned-message.md) | 編碼和解碼副署訊息的 C 程式範例。 |



 

 

 
