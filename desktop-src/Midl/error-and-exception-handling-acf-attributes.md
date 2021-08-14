---
title: 錯誤和例外狀況處理 ACF 屬性
description: 使用下列屬性來處理錯誤。
ms.assetid: fb00df67-4645-4ef0-9216-618d0af1d9d4
keywords:
- ACF MIDL、屬性、錯誤和例外狀況處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f780145854a463da9a983c7dccbb24b01c2eca16437bf1254f93ec34def5395
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384424"
---
# <a name="error-and-exception-handling-acf-attributes"></a>錯誤和例外狀況處理 ACF 屬性

使用下列屬性來處理錯誤。



| 屬性                                                                | 使用方式                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**通訊 \_ 狀態**](comm-status.md)[**錯誤 \_ 狀態**](fault-status.md) | 讓用戶端應用程式以正常方式處理例外狀況，方法是導致通訊和伺服器錯誤以參數值的形式傳回給用戶端。 然後，用戶端應用程式可以呼叫 RPC 執行時間函式 [**DceErrorInqText**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) ，將錯誤訊息轉送給使用者。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[匯入檔案和型別程式庫](importing-files-and-type-libraries.md)
</dt> </dl>

 

 