---
description: 若要判斷資料庫的字碼頁，請呼叫 MsiDatabaseExport，並將 hDatabase 設為資料庫的控制碼，並將 szTableName 設定為 \_ ForceCodepage。
ms.assetid: afa3fbd9-9f54-4f72-ab5d-cb0dbbd9946c
title: 判斷安裝資料庫的字碼頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212978cbce0e73ae495a0ed10ea9070cce6bd374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850232"
---
# <a name="determining-an-installation-databases-code-page"></a><span data-ttu-id="31065-103">判斷安裝資料庫的字碼頁</span><span class="sxs-lookup"><span data-stu-id="31065-103">Determining an Installation Database's Code Page</span></span>

<span data-ttu-id="31065-104">若要判斷資料庫的字碼頁，請呼叫 [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) ，並將 *hDatabase* 設為資料庫的控制碼，並將 *szTableName* 設定為 \_ ForceCodepage。</span><span class="sxs-lookup"><span data-stu-id="31065-104">To determine the code page of a database, call [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) with *hDatabase* set to the handle of the database and *szTableName* set to \_ForceCodepage.</span></span> <span data-ttu-id="31065-105">這會匯出副檔名為 idt 的文字檔。</span><span class="sxs-lookup"><span data-stu-id="31065-105">This exports a text file with an .idt extension.</span></span> <span data-ttu-id="31065-106">這個檔案的前兩行是空白的。</span><span class="sxs-lookup"><span data-stu-id="31065-106">The first two lines of this file are blank.</span></span> <span data-ttu-id="31065-107">第三行是 ANSI 字碼頁編號，後面接著一個索引標籤，再加上名稱 \_ ForceCodepage。</span><span class="sxs-lookup"><span data-stu-id="31065-107">The third line is the ANSI code page number, followed by a tab, followed by the name \_ForceCodepage.</span></span> <span data-ttu-id="31065-108">另請參閱匯 [入和匯出資料表的字碼頁處理](code-page-handling-of-imported-and-exported-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="31065-108">See also [Code Page Handling of Imported and Exported Tables](code-page-handling-of-imported-and-exported-tables.md).</span></span>

<span data-ttu-id="31065-109">使用 [**Export 方法**](database-export.md) 來判斷字碼頁的範例，是在公用程式 WiLangId.vbs 的一部分 Windows Installer SDK 中提供。</span><span class="sxs-lookup"><span data-stu-id="31065-109">An example of determining the code page by using the [**Export method**](database-export.md) is provided in the Windows Installer SDK as a part of the utility WiLangId.vbs.</span></span> <span data-ttu-id="31065-110">如需使用 WiLangId.vbs 的詳細資訊，請參閱主題： [管理語言和字碼頁](manage-language-and-codepage.md)。</span><span class="sxs-lookup"><span data-stu-id="31065-110">For more information about using WiLangId.vbs see the topic: [Manage Language and Codepage](manage-language-and-codepage.md).</span></span>

 

 



