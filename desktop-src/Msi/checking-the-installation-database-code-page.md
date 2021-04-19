---
description: 「字碼頁」（code page）是作業系統用來將符號 (字母、數位和標點符號) 字元對應到字元數位的內部資料表。
ms.assetid: e11193a2-2c72-43a9-8d35-fa524044e306
title: 檢查安裝資料庫字碼頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ea9513ec80413e00a9f3f4c1232a06704f83e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974646"
---
# <a name="checking-the-installation-database-code-page"></a><span data-ttu-id="7b45b-103">檢查安裝資料庫字碼頁</span><span class="sxs-lookup"><span data-stu-id="7b45b-103">Checking the Installation Database Code Page</span></span>

<span data-ttu-id="7b45b-104">「 *字碼頁」（code page* ）是作業系統用來將符號 (字母、數位和標點符號) 字元對應到字元數位的內部資料表。</span><span class="sxs-lookup"><span data-stu-id="7b45b-104">A *code page* is an internal table that the operating system uses to map symbols (letters, numerals, and punctuation characters) to a character number.</span></span> <span data-ttu-id="7b45b-105">不同的字碼頁提供不同國家或地區所使用之字元集的支援。</span><span class="sxs-lookup"><span data-stu-id="7b45b-105">Different code pages provide support for the character sets used in different countries or regions.</span></span> <span data-ttu-id="7b45b-106">字碼頁以 number 參考;例如，字碼頁932代表日文字元集，而字碼頁950則代表其中一個中文字元集。</span><span class="sxs-lookup"><span data-stu-id="7b45b-106">Code pages are referred to by number; for example, code page 932 represents the Japanese character set, and code page 950 represents one of the Chinese character sets.</span></span> <span data-ttu-id="7b45b-107">請參閱 [當地語系化錯誤和 ActionText 資料表](localizing-the-error-and-actiontext-tables.md) ，以取得 ASCII 字碼頁的清單。</span><span class="sxs-lookup"><span data-stu-id="7b45b-107">See [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md) for a list of ASCII code pages.</span></span>

<span data-ttu-id="7b45b-108">相同的 ASCII 字碼頁1252可用於英文和法文。</span><span class="sxs-lookup"><span data-stu-id="7b45b-108">The same ASCII code page, 1252, may be used for English and French.</span></span> <span data-ttu-id="7b45b-109">因此，您不需要重設資料庫 MNP2000.msi 的字碼頁 (英文) 就能將安裝變更為法文。</span><span class="sxs-lookup"><span data-stu-id="7b45b-109">Therefore the code page for the database MNP2000.msi (English) does not need to be reset to change the installation to French.</span></span>

<span data-ttu-id="7b45b-110">如需設定字碼頁的詳細資訊，請參閱 [字碼頁處理 (Windows Installer) ](code-page-handling-windows-installer-.md)。</span><span class="sxs-lookup"><span data-stu-id="7b45b-110">For more information about setting the code page see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>

[<span data-ttu-id="7b45b-111">繼續</span><span class="sxs-lookup"><span data-stu-id="7b45b-111">Continue</span></span>](importing-localized-error-and-actiontext-tables.md)

 

 



