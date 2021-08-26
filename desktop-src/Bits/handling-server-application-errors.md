---
title: 處理伺服器應用程式錯誤
description: 如果伺服器應用程式成功處理上傳的檔案，應用程式應該會傳回200。
ms.assetid: fd0b10f1-52b4-4564-9683-620f3b965680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c66654bdc0070bf5988d16ac2489d62dc3614b44156337747052df5c7c314e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005278"
---
# <a name="handling-server-application-errors"></a>處理伺服器應用程式錯誤

如果伺服器應用程式成功處理上傳的檔案，應用程式應該會傳回200。 如果應用程式未傳回200，BITS 用戶端會使用錯誤碼來判斷錯誤是暫時性錯誤或嚴重錯誤。

所有3xx 錯誤碼都是暫時性錯誤，除了 300-305 和307之外，這些都是嚴重錯誤。 除了408和409之外，所有4xx 錯誤碼都是嚴重錯誤，這是暫時性錯誤。 所有5xx 錯誤碼都是暫時性錯誤，除了501和505之外，這些都是嚴重錯誤。 所有其他 HTTP 代碼都會被視為暫時性錯誤。 請注意，403錯誤碼是唯一的錯誤碼，可防止 BITS 再次將上傳檔案張貼至伺服器應用程式。

若要取出錯誤，請呼叫 [**IBackgroundCopyError：： GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) 方法。 錯誤內容將會是 BG \_ 錯誤 \_ 內容 \_ 遠端 \_ 應用程式。

 

 




