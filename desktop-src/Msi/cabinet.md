---
description: 您必須在媒體資料表的 [封包] 資料行中使用 [封包] 資料類型。
ms.assetid: 149c74ea-4342-45dd-8da4-4dfa7f4317a0
title: 內閣
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4814473ef4d21d5445b5b5319278a5e25a7f5540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848943"
---
# <a name="cabinet"></a><span data-ttu-id="7ea96-103">內閣</span><span class="sxs-lookup"><span data-stu-id="7ea96-103">Cabinet</span></span>

<span data-ttu-id="7ea96-104">您必須在 [媒體資料表](media-table.md)的 [封包] 資料行中使用 [封包] 資料類型。</span><span class="sxs-lookup"><span data-stu-id="7ea96-104">The Cabinet data type must be used in the Cabinet column of the [Media table](media-table.md).</span></span>

<span data-ttu-id="7ea96-105">如果封包名稱前面加上數位記號，封包會以資料流程的形式儲存在封裝內。</span><span class="sxs-lookup"><span data-stu-id="7ea96-105">If the cabinet name is preceded by the number sign, the cabinet is stored as a data stream inside the package.</span></span> <span data-ttu-id="7ea96-106">後面的字元字串 \# 是此資料流程的 [識別碼](identifier.md) 。</span><span class="sxs-lookup"><span data-stu-id="7ea96-106">The character string which follows the \# is an [Identifier](identifier.md) for this data stream.</span></span> <span data-ttu-id="7ea96-107">請注意，如果封包是儲存為數據流，封包的名稱會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="7ea96-107">Note that if the cabinet is stored as a data stream, the name of a cabinet is case-sensitive.</span></span>

<span data-ttu-id="7ea96-108">如果封包名稱前面沒有數位記號 \# ，封包會儲存在 [目錄資料表](directory-table.md)所指定來源樹狀結構的根目錄中的個別檔案中。</span><span class="sxs-lookup"><span data-stu-id="7ea96-108">If the cabinet name is not preceded by the number sign \#, the cabinet is stored in a separate file located at the root of the source tree specified by the [Directory Table](directory-table.md).</span></span> <span data-ttu-id="7ea96-109">封包檔必須使用由八個字元名稱、句號和三個字元副檔名組成的簡短檔案名語法。</span><span class="sxs-lookup"><span data-stu-id="7ea96-109">The cabinet file must use the short file name syntax consisting of an eight character name, a period, and a three character extension.</span></span> <span data-ttu-id="7ea96-110">封包資料類型無法針對檔案名使用簡短的 \| longname 語法。</span><span class="sxs-lookup"><span data-stu-id="7ea96-110">The Cabinet data type cannot use the short\|longname syntax for file names.</span></span> <span data-ttu-id="7ea96-111">如果封包檔儲存為個別的檔案，封包檔的名稱不會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="7ea96-111">If the cabinet file is stored as a separate file, the name of the cabinet file is not case-sensitive.</span></span>

<span data-ttu-id="7ea96-112">為了節省磁碟空間，安裝程式會先移除任何內嵌在 .msi 檔案中的封包，再快取使用者電腦上的安裝套件。</span><span class="sxs-lookup"><span data-stu-id="7ea96-112">To conserve disk space, the installer removes any cabinets embedded in the .msi file before caching the installation package on the user's computer.</span></span>

<span data-ttu-id="7ea96-113">請參閱 [在安裝中包含封包](including-a-cabinet-file-in-an-installation.md)檔。</span><span class="sxs-lookup"><span data-stu-id="7ea96-113">See [Including a Cabinet File in an Installation](including-a-cabinet-file-in-an-installation.md).</span></span>

 

 



