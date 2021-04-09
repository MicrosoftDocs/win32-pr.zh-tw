---
description: 下列程式碼片段說明如何在 ILS 伺服器中發行使用者物件。 在使用者物件發佈之後，遠端合作物件就可以使用 user 物件來呼叫指定的使用者。
ms.assetid: 8b68886c-0df5-4005-bcd5-1a18336f5192
title: 將使用者物件加入至 ILS 伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85b15dcdbca47187cf4155dfbf7535d06718c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690068"
---
# <a name="adding-a-user-object-to-an-ils-server"></a>將使用者物件加入至 ILS 伺服器

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

下列程式碼片段說明如何在 ILS 伺服器中發行使用者物件。 在使用者物件發佈之後，遠端合作物件就可以使用 user 物件來呼叫指定的使用者。

此片段假設已經執行 [連接到 ILS 伺服器](connecting-to-an-ils-server.md) 。


```C++
hr = pDirectory->AddDirectoryObject(pDirectoryObject);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)
</dt> <dt>

[**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser)
</dt> </dl>

 

 



