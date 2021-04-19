---
description: IX509EndorsementKey 介面會公開下列屬性。
ms.assetid: 9E93622B-56E9-4F2F-9EFA-4F63D45EDCB6
title: IX509EndorsementKey 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4bbdbc464803988f5b1100ac42fc0e3697fb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989960"
---
# <a name="ix509endorsementkey-properties"></a>IX509EndorsementKey 屬性

[**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey)介面會公開下列屬性。

## <a name="in-this-section"></a>本節內容



| 主題                                                                        | 描述                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Length 屬性**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_length)<br/>             | 簽署金鑰的位長度。 您只能在呼叫 [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) 方法之後存取這個屬性。<br/>                                                                                                                                                                                            |
| [**開啟的屬性**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_opened)<br/>             | 指出是否已成功呼叫 [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) 方法。<br/>                                                                                                                                                                                                                                            |
| [**ProviderName 屬性**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername)<br/> | 加密提供者的名稱。 預設值為 Microsoft 平臺密碼編譯提供者。 您必須先設定 [**ProviderName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) 屬性，然後再呼叫 [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) 方法。 當您呼叫 **Open** 方法之後，就無法變更 **ProviderName** 屬性。<br/> |



 

 

 




