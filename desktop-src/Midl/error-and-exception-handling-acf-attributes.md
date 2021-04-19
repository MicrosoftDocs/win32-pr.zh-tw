---
title: 錯誤和例外狀況處理 ACF 屬性
description: 使用下列屬性來處理錯誤。
ms.assetid: fb00df67-4645-4ef0-9216-618d0af1d9d4
keywords:
- ACF MIDL、屬性、錯誤和例外狀況處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7187ab887fa1d09b18385b86065775ca0e656f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106984515"
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

 

 