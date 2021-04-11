---
description: 您可以使用安裝程式將文字封存匯入至使用中的資料庫，以及將資料庫檔案匯出至文字封存。 這對以文字為基礎的原始檔控制系統很有用。
ms.assetid: 1025da16-9e1f-4fb4-9ce1-f992970eb903
title: 匯入和匯出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb778f4a0fe415686c80f2609f63958ae042d920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114329"
---
# <a name="importing-and-exporting"></a><span data-ttu-id="9faaa-104">匯入和匯出</span><span class="sxs-lookup"><span data-stu-id="9faaa-104">Importing and Exporting</span></span>

<span data-ttu-id="9faaa-105">您可以使用安裝程式將文字封存匯入至使用中的資料庫，以及將資料庫檔案匯出至文字封存。</span><span class="sxs-lookup"><span data-stu-id="9faaa-105">You can use the installer to import a text archive into an active database as well as to export a database file to a text archive.</span></span> <span data-ttu-id="9faaa-106">這對以文字為基礎的原始檔控制系統很有用。</span><span class="sxs-lookup"><span data-stu-id="9faaa-106">This can be useful for text-based source control systems.</span></span>

<span data-ttu-id="9faaa-107">若要將文字封存匯入作用中的資料庫，請呼叫 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) 函式。</span><span class="sxs-lookup"><span data-stu-id="9faaa-107">To import a text archive into an active database, call the [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) function.</span></span>

<span data-ttu-id="9faaa-108">若要將資料庫檔案匯出至文字封存，請呼叫 [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) 函數。</span><span class="sxs-lookup"><span data-stu-id="9faaa-108">To export a database file to a text archive, call the [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) function.</span></span>

 

 



