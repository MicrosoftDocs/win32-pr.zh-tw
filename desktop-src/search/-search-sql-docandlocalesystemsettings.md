---
description: 當作業系統（甚至是應用程式）設定為使用特定語言和地區設定時，許多設定都會受到影響。
ms.assetid: cec164d1-125f-483c-9d74-0e24b8215157
title: 檔和系統地區設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9408093a8583a4b17566b5fcd118b30439c0ebda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970578"
---
# <a name="document-and-system-locale-settings"></a>檔和系統地區設定

當作業系統（甚至是應用程式）設定為使用特定語言和地區設定時，許多設定都會受到影響。 這些設定包括數值格式、日期格式、貨幣格式、大寫和小寫對應、字典排序次序、token 化和其他設定。 雖然這些設定有助於 Windows Search 提供絕佳的當地語系化支援，但使用設定為其他地區設定的系統搜尋來自某個地區設定的檔時，可能會發生非預期的結果。

當 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 物件處理檔的文字屬性和內容時，會將該檔的語言報告給內容索引器。 使用此資訊，Windows Search 可以套用適當的斷詞工具。

 

 
