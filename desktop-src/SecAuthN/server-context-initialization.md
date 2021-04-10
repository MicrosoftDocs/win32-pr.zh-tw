---
description: 和用戶端一樣，伺服器也會取得認證控制碼，以準備回應來自用戶端的傳入驗證要求。
ms.assetid: 2a0aeadf-e099-4264-8522-e498f437bf75
title: 伺服器內容初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1362c8fd71e079392f10a8e35f76ad511de3c49f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692919"
---
# <a name="server-context-initialization"></a>伺服器內容初始化

和用戶端一樣，伺服器也會取得 [*認證*](../secgloss/c-gly.md) 控制碼，以準備回應來自用戶端的傳入驗證要求。 伺服器認證是用來在支援伺服器驗證或相互驗證的 [*安全性通訊協定*](../secgloss/s-gly.md) 中，對用戶端驗證服務器。 伺服器會取得用來啟動伺服器之服務帳戶所定義的認證控制碼。 它會藉由呼叫 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)來執行此動作。

伺服器可以取得其認證控制碼，然後進入「接聽」狀態，也可以在連線要求抵達之前等候接聽狀態，然後取得輸入認證控制碼。 如需認證功能的詳細資訊，請參閱 [認證管理](authentication-functions.md)。

當伺服器收到來自用戶端的連線要求訊息時，它會使用 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)來建立用戶端的本機 [*安全性內容*](../secgloss/s-gly.md)。 伺服器會使用這個本機安全性內容來執行相同用戶端的未來要求。 如需內容函數的詳細資訊，請參閱 [內容管理](authentication-functions.md)。

伺服器會檢查傳回狀態和輸出緩衝區描述項，以確定目前沒有任何錯誤，而且如果發生錯誤，就會拒絕連接要求。 如果 AcceptSecurityCoNtext 所傳回的輸出緩衝區中有資訊 [**(一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)，它會將該緩衝區組合至用戶端的回應訊息。

[**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)的任何輸出緩衝區都必須傳送回用戶端。 此外，如果傳回狀態需要通訊協定才能繼續 (需要繼續進行 \_ \_ \_ ，或每秒 \_ \_ 完成 \_ 並 \_ 繼續) ，則需要另一個與用戶端交換的訊息。

針對額外的腿，伺服器會等候用戶端以其他訊息回應。 這項等候的時間可能會讓用戶端刻意沒有回應，而導致伺服器執行緒，以及不久的所有伺服器執行緒停止回應。

 

 
