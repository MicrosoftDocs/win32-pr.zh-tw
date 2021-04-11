---
description: 您可以從命令列或從程式完全或部分地重新安裝應用程式，以將小型更新套用至應用程式。
ms.assetid: 6f8b68da-7748-436d-bc95-96e39cf42143
title: 重新安裝產品以套用小型更新
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27b97ff0274baac5a4ec30df244394a609ed525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944028"
---
# <a name="applying-small-updates-by-reinstalling-the-product"></a><span data-ttu-id="29e2c-103">重新安裝產品以套用小型更新</span><span class="sxs-lookup"><span data-stu-id="29e2c-103">Applying Small Updates by Reinstalling the Product</span></span>

<span data-ttu-id="29e2c-104">您可以從命令列或從程式完全或部分地重新安裝應用程式，以將小型更新套用至應用程式。</span><span class="sxs-lookup"><span data-stu-id="29e2c-104">A small update can be applied to an application by completely or partially reinstalling the application from the command line or from a program.</span></span>

<span data-ttu-id="29e2c-105">**若要將 small update 傳播給目前的使用者 (這是從命令列完整重新安裝)**</span><span class="sxs-lookup"><span data-stu-id="29e2c-105">**To propagate the small update to current users (this is a complete reinstall) from the command line**</span></span>

1.  <span data-ttu-id="29e2c-106">從命令列使用： **msiexec \[ /fvomus** _path 將 .msi_ 檔案 *_\]_* 或 **msiexec/i \[** 路徑更新 _為已更新的 .msi 檔案。_ *_\] 重新安裝 = ALL REINSTALLMODE = vomus reinstall_*。</span><span class="sxs-lookup"><span data-stu-id="29e2c-106">From the command line use either: **msiexec /fvomus \[**_path to updated .msi file_*_\]_* or **msiexec /I \[**_path to updated .msi file_*_\] REINSTALL=ALL REINSTALLMODE=vomus_*.</span></span>
2.  <span data-ttu-id="29e2c-107">更新的 .msi 檔案會快取在使用者的電腦上。</span><span class="sxs-lookup"><span data-stu-id="29e2c-107">The updated .msi file is cached on the user's computer.</span></span> <span data-ttu-id="29e2c-108">請注意，使用者無法使用 [新增/移除程式] 重新安裝產品，因為更新的 .msi 檔案尚未在使用者的電腦上。</span><span class="sxs-lookup"><span data-stu-id="29e2c-108">Note that it is not possible for the user to reinstall the product using Add/Remove Programs because the updated .msi file is not yet on the user's computer.</span></span>

<span data-ttu-id="29e2c-109">**若要將小型更新傳播給目前的使用者 (這是從程式完整重新安裝)**</span><span class="sxs-lookup"><span data-stu-id="29e2c-109">**To propagate a small update to current users (this is a complete reinstall) from a program**</span></span>

1.  <span data-ttu-id="29e2c-110">從程式中，呼叫 [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) 並指定 REINSTALLMODE \_ PACKAGE、REINSTALLMODE \_ FILEOLDERVERSION、REINSTALLMODE \_ MACHINEDATA、REINSTALLMODE \_ USERDATA 和 REINSTALLMODE \_ 快速鍵</span><span class="sxs-lookup"><span data-stu-id="29e2c-110">From a program, call [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) and specify REINSTALLMODE\_PACKAGE, REINSTALLMODE\_FILEOLDERVERSION, REINSTALLMODE\_MACHINEDATA, REINSTALLMODE\_USERDATA, and REINSTALLMODE\_SHORTCUT</span></span>
2.  <span data-ttu-id="29e2c-111">更新的 .msi 檔案會快取在使用者的電腦上。</span><span class="sxs-lookup"><span data-stu-id="29e2c-111">The updated .msi file is cached on the user's computer.</span></span>

<span data-ttu-id="29e2c-112">下列方法會啟動僅重新安裝受 small update 影響的功能或元件。</span><span class="sxs-lookup"><span data-stu-id="29e2c-112">The following method launches a reinstallation of only those features or components that are affected by the small update.</span></span>

<span data-ttu-id="29e2c-113">**若要將小型更新傳播給目前的使用者 (這是部分重新安裝)**</span><span class="sxs-lookup"><span data-stu-id="29e2c-113">**To propagate a small update to current users (this is a partial reinstall)**</span></span>

1.  <span data-ttu-id="29e2c-114">取得受 small update 影響的功能和元件名稱清單。</span><span class="sxs-lookup"><span data-stu-id="29e2c-114">Obtain a list of the names of features and components that are affected by the small update.</span></span>
2.  <span data-ttu-id="29e2c-115">從命令提示字元使用： **msiexec/i \[** _path to updated .msi file_ *_\] 重新安裝 = \[_* _Feature list \]_ **REINSTALLMODE = vomus reinstall**。</span><span class="sxs-lookup"><span data-stu-id="29e2c-115">From the command prompt use: **msiexec /I \[**_path to updated .msi file_*_\] REINSTALL=\[_*_Feature list\]_ **REINSTALLMODE=vomus**.</span></span>
3.  <span data-ttu-id="29e2c-116">更新的 .msi 檔案會快取在使用者的電腦上。</span><span class="sxs-lookup"><span data-stu-id="29e2c-116">The updated .msi file is cached on the user's computer.</span></span>

 

 



