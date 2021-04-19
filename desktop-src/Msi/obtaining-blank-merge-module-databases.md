---
description: 取得空白的合併模組資料庫。 您可以使用 Windows Installer SDK 隨附的檔案架構做為合併模組的起始資料庫。 如需詳細資訊，請參閱 Windows Installer 開發人員 Windows SDK 元件。
ms.assetid: 8408e892-adc6-4ef5-ad36-4d04c021c899
title: 取得空白合併模組資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba75d55763d30b0ab545d2dbddbc19c1b0c279d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975017"
---
# <a name="obtaining-blank-merge-module-databases"></a><span data-ttu-id="077cc-105">取得空白合併模組資料庫</span><span class="sxs-lookup"><span data-stu-id="077cc-105">Obtaining Blank Merge Module Databases</span></span>

<span data-ttu-id="077cc-106">取得空白的合併模組資料庫。</span><span class="sxs-lookup"><span data-stu-id="077cc-106">Obtain a blank merge module database.</span></span> <span data-ttu-id="077cc-107">您可以使用 Windows Installer SDK 隨附的檔案架構做為合併模組的起始資料庫。</span><span class="sxs-lookup"><span data-stu-id="077cc-107">You can use the file Schema.msm provided with the Windows Installer SDK as a starting database for your merge module.</span></span> <span data-ttu-id="077cc-108">如需詳細資訊，請參閱 [Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。</span><span class="sxs-lookup"><span data-stu-id="077cc-108">For more information, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="077cc-109">開發人員應該使用安裝其元件的最簡單資料庫架構來撰寫合併模組。</span><span class="sxs-lookup"><span data-stu-id="077cc-109">Developers should author merge modules using the simplest database schema that installs their components.</span></span> <span data-ttu-id="077cc-110">使用簡單的架構可確保合併模組的最大相容性。</span><span class="sxs-lookup"><span data-stu-id="077cc-110">The use of a simple schema ensures the greatest compatibility for the merge module.</span></span> <span data-ttu-id="077cc-111">將合併模組合併為具有不同資料庫架構的安裝套件，通常會導致合併衝突。</span><span class="sxs-lookup"><span data-stu-id="077cc-111">Merging a merge module into an installation package with a different database schema usually results in merge conflicts.</span></span>

<span data-ttu-id="077cc-112">如需合併模組中所有必要和選擇性資料表的完整清單，請參閱 [合併模組資料庫資料表](merge-module-database-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="077cc-112">For a complete list of all the required and optional tables in merge modules, see [Merge Module Database Tables](merge-module-database-tables.md).</span></span>

 

 



