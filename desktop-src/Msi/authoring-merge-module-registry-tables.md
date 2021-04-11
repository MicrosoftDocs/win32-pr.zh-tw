---
description: 根據登錄資訊的類型，使用合併模組登錄表。
ms.assetid: 091429ff-a8f4-4e1b-929f-1559cd173c3d
title: 撰寫合併模組登錄資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d10e31ac82d190c87019da5bc77408b58122a523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944011"
---
# <a name="authoring-merge-module-registry-tables"></a><span data-ttu-id="ad7a9-103">撰寫合併模組登錄資料表</span><span class="sxs-lookup"><span data-stu-id="ad7a9-103">Authoring Merge Module Registry Tables</span></span>

<span data-ttu-id="ad7a9-104">根據登錄資訊的類型，使用合併模組登錄表。</span><span class="sxs-lookup"><span data-stu-id="ad7a9-104">Use Merge Module Registry tables according to the type of registry information.</span></span>

## <a name="typelib-class-appid-progid-extension-verb-or-mime-tables"></a><span data-ttu-id="ad7a9-105">TypeLib、Class、AppId、ProgId、Extension、Verb 或 MIME 資料表</span><span class="sxs-lookup"><span data-stu-id="ad7a9-105">TypeLib, Class, AppId, ProgId, Extension, Verb, or MIME Tables</span></span>

<span data-ttu-id="ad7a9-106">針對型別程式庫、類別、延伸模組和動詞，將登錄資訊撰寫至合併模組的 [TypeLib](typelib-table.md)、 [類別](class-table.md)、 [AppId](appid-table.md)、 [ProgId](progid-table.md)、 [擴充](extension-table.md)、 [動詞](verb-table.md)或 [MIME](mime-table.md) 資料表中。</span><span class="sxs-lookup"><span data-stu-id="ad7a9-106">For type libraries, classes, extensions, and verbs, author registry information into the merge module's [TypeLib](typelib-table.md), [Class](class-table.md), [AppId](appid-table.md), [ProgId](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md), or [MIME](mime-table.md) tables.</span></span> <span data-ttu-id="ad7a9-107">如果您使用登錄 [表](registry-table.md) 來新增這項資訊，Windows 2000 就無法為這些元件提供整個系統的公告。</span><span class="sxs-lookup"><span data-stu-id="ad7a9-107">If you use the [Registry table](registry-table.md) to add this information, Windows 2000 cannot provide system-wide advertisement for these components.</span></span>

<span data-ttu-id="ad7a9-108">合併模組作者可能會因為下列原因而決定不使用類別表進行註冊：</span><span class="sxs-lookup"><span data-stu-id="ad7a9-108">Merge module authors may decide not to register using the Class table for the following reasons:</span></span>

-   <span data-ttu-id="ad7a9-109">若要由類別資料表註冊，檔案必須是其元件的 KeyPath。</span><span class="sxs-lookup"><span data-stu-id="ad7a9-109">To be registered by the Class table, the file has to be the KeyPath of its component.</span></span> <span data-ttu-id="ad7a9-110">這可能需要元件組織中的無法接受變更。</span><span class="sxs-lookup"><span data-stu-id="ad7a9-110">This may require an unacceptable change in the organization of components.</span></span>
-   <span data-ttu-id="ad7a9-111">COM 呼叫可能會觸發安裝程式嘗試重新安裝已公告的類別。</span><span class="sxs-lookup"><span data-stu-id="ad7a9-111">A COM call may trigger an installer attempt to reinstall an advertised class.</span></span> <span data-ttu-id="ad7a9-112">作者可以決定不要使用類別表註冊類別，以避免在用戶端電腦不支援使用者介面時觸發重新安裝。</span><span class="sxs-lookup"><span data-stu-id="ad7a9-112">Authors may decide not to register a class using the Class table in order to avoid triggering a reinstallation when the client computer does not support a user interface.</span></span>

## <a name="registry-table"></a><span data-ttu-id="ad7a9-113">登錄資料表</span><span class="sxs-lookup"><span data-stu-id="ad7a9-113">Registry Table</span></span>

<span data-ttu-id="ad7a9-114">使用登錄資料表來加入無法撰寫到 TypeLib、類別、AppId、ProgId、延伸模組、動詞或 MIME 資料表的登錄資訊。</span><span class="sxs-lookup"><span data-stu-id="ad7a9-114">Use the Registry table to add registry information that cannot be authored into the TypeLib, Class, AppId, ProgId, Extension, Verb, or MIME tables.</span></span> <span data-ttu-id="ad7a9-115">Windows 2000 無法針對使用登錄表的元件提供整個系統的公告。</span><span class="sxs-lookup"><span data-stu-id="ad7a9-115">Windows 2000 cannot provide system-wide advertisement for components that use the Registry table.</span></span>

<span data-ttu-id="ad7a9-116">編寫登錄表時，請參閱使用檔案的檔案路徑 \[ \# \] 或 \[ ！檔 \] 格式，而不是 \[ 目錄 \] 檔案名。</span><span class="sxs-lookup"><span data-stu-id="ad7a9-116">When authoring the Registry table, refer to file paths using the \[\#File\] or \[!File\] format rather than as \[Directory\]Filename.</span></span> <span data-ttu-id="ad7a9-117">後者的格式不支援從來源執行安裝。</span><span class="sxs-lookup"><span data-stu-id="ad7a9-117">The latter format does not support run-from-source installation.</span></span> <span data-ttu-id="ad7a9-118">先前的格式也會讓遺失的檔案和錯誤的元件更容易偵測。</span><span class="sxs-lookup"><span data-stu-id="ad7a9-118">The former format also makes missing files and faulty components easier to detect.</span></span>

<span data-ttu-id="ad7a9-119">在登錄表的索引鍵資料行中使用格式化文字時，需要注意。</span><span class="sxs-lookup"><span data-stu-id="ad7a9-119">Care is needed when using formatted text in the Key column of the Registry table.</span></span> <span data-ttu-id="ad7a9-120">因為 Windows Installer 不會重新安裝已安裝的元件，所以使用此欄位中格式化的文字可能會導致在移除應用程式時留下登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="ad7a9-120">Because Windows Installer does not reinstall components that are already installed, using formatted text in this field may cause registry keys to be left behind on application removal.</span></span>

## <a name="selfreg-table"></a><span data-ttu-id="ad7a9-121">SelfReg 資料表</span><span class="sxs-lookup"><span data-stu-id="ad7a9-121">SelfReg Table</span></span>

<span data-ttu-id="ad7a9-122">不建議使用 SelfReg 資料表。</span><span class="sxs-lookup"><span data-stu-id="ad7a9-122">Using the SelfReg table is not recommended.</span></span> <span data-ttu-id="ad7a9-123">如需不使用自我註冊的原因清單，請參閱 [SelfReg 資料表](selfreg-table.md)。</span><span class="sxs-lookup"><span data-stu-id="ad7a9-123">For a list of reasons for not using self-registration, see [SelfReg table](selfreg-table.md).</span></span> <span data-ttu-id="ad7a9-124">在其他所有情況下，您應該盡可能使用 TypeLib、Class、AppId、ProgId、Extension、Verb 和 MIME 資料表，以及登錄資料表。</span><span class="sxs-lookup"><span data-stu-id="ad7a9-124">You should use the TypeLib, Class, AppId, ProgId, Extension, Verb, and MIME tables where possible instead and the Registry table in all other cases.</span></span>

 

 



