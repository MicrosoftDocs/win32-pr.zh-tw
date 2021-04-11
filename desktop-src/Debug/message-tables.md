---
description: 訊息資料表是顯示錯誤訊息時使用的特殊字元串資源。 它們是使用 MESSAGETABLE 資源定義語句在資源檔中宣告的。 若要存取訊息字串，請使用 FormatMessage 函數。
ms.assetid: db84f190-1d1e-4192-8dba-baaee0a3e3ea
title: 訊息資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe12b28c9b4f89d9a6d32c398a2e246940bb79a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936099"
---
# <a name="message-tables"></a><span data-ttu-id="c1afe-105">訊息資料表</span><span class="sxs-lookup"><span data-stu-id="c1afe-105">Message Tables</span></span>

<span data-ttu-id="c1afe-106">訊息資料表是顯示錯誤訊息時使用的特殊字元串資源。</span><span class="sxs-lookup"><span data-stu-id="c1afe-106">Message tables are special string resources used when displaying error messages.</span></span> <span data-ttu-id="c1afe-107">它們是使用 [MESSAGETABLE](../menurc/messagetable-resource.md) 資源定義語句在資源檔中宣告的。</span><span class="sxs-lookup"><span data-stu-id="c1afe-107">They are declared in a resource file using the [MESSAGETABLE](../menurc/messagetable-resource.md) resource-definition statement.</span></span> <span data-ttu-id="c1afe-108">若要存取訊息字串，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函數。</span><span class="sxs-lookup"><span data-stu-id="c1afe-108">To access the message strings, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function.</span></span>

<span data-ttu-id="c1afe-109">系統會提供 [系統錯誤碼](system-error-codes.md)的訊息資料表。</span><span class="sxs-lookup"><span data-stu-id="c1afe-109">The system provides a message table for the [system error codes](system-error-codes.md).</span></span> <span data-ttu-id="c1afe-110">若要取得對應至錯誤碼的字串，請使用[](/windows/desktop/api/WinBase/nf-winbase-formatmessage) \_ \_ 來自 \_ 系統旗標的格式訊息來呼叫 FormatMessage。</span><span class="sxs-lookup"><span data-stu-id="c1afe-110">To retrieve the string that corresponds to the error code, call [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag.</span></span>

<span data-ttu-id="c1afe-111">若要為您的應用程式提供消息表，請依照 [訊息文字檔](../eventlog/message-text-files.md)中的指示進行。</span><span class="sxs-lookup"><span data-stu-id="c1afe-111">To provide a message table for your application, follow the instructions in [Message Text Files](../eventlog/message-text-files.md).</span></span> <span data-ttu-id="c1afe-112">若要從訊息資料表中取出字串， [](/windows/desktop/api/WinBase/nf-winbase-formatmessage)請使用 \_ \_ 來自 HMODULE 旗標的格式訊息來呼叫 FormatMessage \_ 。</span><span class="sxs-lookup"><span data-stu-id="c1afe-112">To retrieve strings from your message table, call [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) with the FORMAT\_MESSAGE\_FROM\_HMODULE flag.</span></span>

 

 
