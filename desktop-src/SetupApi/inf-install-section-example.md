---
description: INF 檔案的 [安裝] 區段會定義安裝程式的步驟。
ms.assetid: 24d40dc6-ac09-4cf8-9229-f81da2925576
title: INF 安裝區段範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39c8162dbf06b87faf8a1ce432c361a28befca0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975804"
---
# <a name="inf-install-section-example"></a><span data-ttu-id="d1482-103">INF 安裝區段範例</span><span class="sxs-lookup"><span data-stu-id="d1482-103">INF Install Section Example</span></span>

<span data-ttu-id="d1482-104">INF 檔案的 [ **安裝** ] 區段會定義安裝程式的步驟。</span><span class="sxs-lookup"><span data-stu-id="d1482-104">The **Install** section of an INF File defines the steps of the installation procedure.</span></span> <span data-ttu-id="d1482-105">**安裝** 區段的每一行都有兩個部分。</span><span class="sxs-lookup"><span data-stu-id="d1482-105">Each line of an **Install** section has two parts.</span></span> <span data-ttu-id="d1482-106">在等號 (=) 的左邊是索引鍵。</span><span class="sxs-lookup"><span data-stu-id="d1482-106">On the left of the equals sign (=) is the key.</span></span> <span data-ttu-id="d1482-107">右側是一個或多個區段標題的清單。</span><span class="sxs-lookup"><span data-stu-id="d1482-107">On the right hand side, is a list of one or more section titles.</span></span> <span data-ttu-id="d1482-108">索引鍵會指定右側所列的區段類型。</span><span class="sxs-lookup"><span data-stu-id="d1482-108">The key specifies the type of the sections that are listed on the right.</span></span> <span data-ttu-id="d1482-109">如需本節格式的說明，請參閱 Microsoft Windows 2000 驅動程式開發工具組的「INF 檔案區段和指示詞」。</span><span class="sxs-lookup"><span data-stu-id="d1482-109">For a description of this section's format see the "INF File Sections and Directives" of the Microsoft Windows 2000 Driver Development Kit.</span></span>

<span data-ttu-id="d1482-110">以下是 **安裝** 區段的範例。</span><span class="sxs-lookup"><span data-stu-id="d1482-110">The following is an example of an **Install** section.</span></span>

``` syntax
[MyInstallSection]
Copyfiles=DataFiles, ProgramFiles
Delfiles=OldFiles
UpdateInis=NewIniInfo
AddReg=NewRegistryInfo, MoreNewRegistryInfo
DelReg=OldRegistryInfo, MoreOldRegistryInfo
```

<span data-ttu-id="d1482-111">在此範例中， **CopyFiles** 索引鍵會設定為 "資料檔案" 和 "ProgramFiles" 值。</span><span class="sxs-lookup"><span data-stu-id="d1482-111">In this example the **CopyFiles** key is set to the values "DataFiles" and "ProgramFiles".</span></span> <span data-ttu-id="d1482-112">這會指定 INF 檔案中的兩個 [ **複製** 檔案] 區段，其中包含複製作業所使用的原始程式檔名稱。</span><span class="sxs-lookup"><span data-stu-id="d1482-112">This specifies two **Copy Files** sections in the INF file that contain the names of the source files used by copying operations.</span></span> <span data-ttu-id="d1482-113">複製之檔案的目的地會在 INF 檔案的 **DestinationDirs** 區段中指定。</span><span class="sxs-lookup"><span data-stu-id="d1482-113">The destination for the copied files would be specified in a **DestinationDirs** section in the INF file.</span></span>

<span data-ttu-id="d1482-114">**Delfiles** 索引鍵的值為 "OldFiles"。</span><span class="sxs-lookup"><span data-stu-id="d1482-114">The **Delfiles** key is given the value "OldFiles".</span></span> <span data-ttu-id="d1482-115">這會指定 [ **刪除** 檔案] 區段，其中包含與檔案刪除作業相關的資訊。</span><span class="sxs-lookup"><span data-stu-id="d1482-115">This specifies a **Delete Files** section that contains information relevant to file deletion operations.</span></span>

<span data-ttu-id="d1482-116">**UpdateInis** 索引鍵會指定 **更新 ini** 檔案區段，其中包含有關在 INI 檔案中更新專案的資訊。</span><span class="sxs-lookup"><span data-stu-id="d1482-116">The **UpdateInis** key specifies **Update INI File** sections that contain information about updating entries in the INI file.</span></span>

<span data-ttu-id="d1482-117">**AddReg** 和 **DelReg** 金鑰指定 [**新增** 登錄] 和 [**刪除** 登錄] 區段，其中包含新增或刪除登錄資訊的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d1482-117">The **AddReg** and **DelReg** keys specify **Add Registry** and **Delete Registry** sections that contain information about adding or deleting registry information.</span></span>

 

 



