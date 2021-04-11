---
description: 將元件安裝到特定應用程式的隔離位置時，必須在 MsiAssembly 資料表的 [檔案應用程式] 資料行中指定應用程式 \_ 。
ms.assetid: 8d7fc09c-1017-4a30-be00-b7b0e5f2a057
title: 安裝和移除元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44dee05940ab3c05e97a7145f9b2363226bb07c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195283"
---
# <a name="installing-and-removing-assemblies"></a><span data-ttu-id="510ce-103">安裝和移除元件</span><span class="sxs-lookup"><span data-stu-id="510ce-103">Installing and Removing Assemblies</span></span>

<span data-ttu-id="510ce-104">將元件安裝到特定應用程式的隔離位置時，必須在 MsiAssembly 資料表的 [檔案應用程式] 資料行中指定應用程式 \_ 。 [](msiassembly-table.md)</span><span class="sxs-lookup"><span data-stu-id="510ce-104">When installing an assembly to an isolated location for a specific application, the application must be specified in the File\_Application column of the [MsiAssembly table](msiassembly-table.md).</span></span> <span data-ttu-id="510ce-105">此欄位是檔案 [資料表](file-table.md)中的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="510ce-105">This field is a key into the [File table](file-table.md).</span></span> <span data-ttu-id="510ce-106">安裝程式會使用 [目錄資料表](directory-table.md) 中指定的目錄結構，將元件安裝到與包含這個檔案的元件相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="510ce-106">The installer uses the directory structure that is specified in the [Directory table](directory-table.md) to install the assembly into the same directory as the component that contains this file.</span></span>

<span data-ttu-id="510ce-107">將元件安裝到全域組件快取時， \_ [MsiAssembly 資料表](msiassembly-table.md) 的 File Application 資料行中的值必須是 Null。</span><span class="sxs-lookup"><span data-stu-id="510ce-107">When installing an assembly to the global assembly cache, the value in the File\_Application column of the [MsiAssembly Table](msiassembly-table.md) must be Null.</span></span>

<span data-ttu-id="510ce-108">下列各節說明 Win32 和 common language runtime 元件的安裝：</span><span class="sxs-lookup"><span data-stu-id="510ce-108">The following sections describe the installation of Win32 and common language runtime assemblies:</span></span>

-   [<span data-ttu-id="510ce-109">Win32 元件的安裝</span><span class="sxs-lookup"><span data-stu-id="510ce-109">Installation of Win32 Assemblies</span></span>](installation-of-win32-assemblies.md)
-   [<span data-ttu-id="510ce-110">Common Language Runtime 元件的安裝</span><span class="sxs-lookup"><span data-stu-id="510ce-110">Installation of Common Language Runtime Assemblies</span></span>](installation-of-common-language-runtime-assemblies.md)

 

 



