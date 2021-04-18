---
description: 任何安裝程式的核心都是檔案的實際安裝。
ms.assetid: e6f6d6a5-bdb0-4866-8d2c-56313d92c94c
title: 檔案版本控制規則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c6f8e59b4f15774f898217690dbb1c4d57b1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983542"
---
# <a name="file-versioning-rules"></a><span data-ttu-id="6e23d-103">檔案版本控制規則</span><span class="sxs-lookup"><span data-stu-id="6e23d-103">File Versioning Rules</span></span>

<span data-ttu-id="6e23d-104">任何安裝程式的核心都是檔案的實際安裝。</span><span class="sxs-lookup"><span data-stu-id="6e23d-104">At the core of any installer is the actual installation of files.</span></span> <span data-ttu-id="6e23d-105">判斷是否要安裝檔案是很複雜的進程。</span><span class="sxs-lookup"><span data-stu-id="6e23d-105">Determining whether to install a file is a complex process.</span></span> <span data-ttu-id="6e23d-106">在最高的層級上，這取決於檔案所屬的元件是否標記為要安裝。</span><span class="sxs-lookup"><span data-stu-id="6e23d-106">At the highest level, this determination depends on whether the component to which a file belongs is marked for installation.</span></span> <span data-ttu-id="6e23d-107">一旦決定要複製檔案之後，如果目的檔案夾中有另一個具有相同名稱的檔案，程式就會很複雜。</span><span class="sxs-lookup"><span data-stu-id="6e23d-107">Once determined that a file should be copied, the process is complicated if another file with the same name exists in the target folder.</span></span> <span data-ttu-id="6e23d-108">在這種情況下，進行判斷需要一組涉及下列屬性的規則：</span><span class="sxs-lookup"><span data-stu-id="6e23d-108">In such situations, making the determination requires a set of rules involving the following properties:</span></span>

-   <span data-ttu-id="6e23d-109">版本</span><span class="sxs-lookup"><span data-stu-id="6e23d-109">Version</span></span>
-   <span data-ttu-id="6e23d-110">Date</span><span class="sxs-lookup"><span data-stu-id="6e23d-110">Date</span></span>
-   <span data-ttu-id="6e23d-111">語言</span><span class="sxs-lookup"><span data-stu-id="6e23d-111">Language</span></span>

<span data-ttu-id="6e23d-112">安裝程式只會在嘗試將檔案安裝至已包含同名檔案的位置時，才會使用這些規則。</span><span class="sxs-lookup"><span data-stu-id="6e23d-112">The installer only uses these rules when trying to install a file to a location that already contains a file with the same name.</span></span> <span data-ttu-id="6e23d-113">在此情況下，Windows Installer 會使用下列規則，所有其他專案都相等，以判斷是否要安裝。</span><span class="sxs-lookup"><span data-stu-id="6e23d-113">In this case, the Windows Installer uses the following rules, all other things being equal, to determine whether to install.</span></span>

<span data-ttu-id="6e23d-114">最高版本獲勝—所有其他專案都相等，最高版本的檔案會獲勝，即使電腦上的檔案具有最高版本也是如此。</span><span class="sxs-lookup"><span data-stu-id="6e23d-114">Highest Version Wins—All other things being equal, the file with the highest version wins, even if the file on the computer has the highest version.</span></span>

<span data-ttu-id="6e23d-115">已建立版本的檔案獲勝—已建立版本的檔案會透過 nonversioned 檔案進行安裝。</span><span class="sxs-lookup"><span data-stu-id="6e23d-115">Versioned Files Win—A versioned file gets installed over a nonversioned file.</span></span>

<span data-ttu-id="6e23d-116">偏好產品語言—如果所安裝的檔案與電腦上的檔案具有不同的語言，請使用符合所要安裝產品的語言。</span><span class="sxs-lookup"><span data-stu-id="6e23d-116">Favor Product Language—If the file being installed has a different language than the file on the computer, favor the file with the language that matches the product being installed.</span></span> <span data-ttu-id="6e23d-117">非語言相關的檔案會被視為另一種語言，因此會再次接受安裝的產品。</span><span class="sxs-lookup"><span data-stu-id="6e23d-117">Language-neutral files are treated as just another language so the product being installed is favored again.</span></span>

<span data-ttu-id="6e23d-118">不相符的多個語言—在將所安裝的檔案和電腦上的檔案中的任何通用語言分解出來之後，會根據所安裝產品所需的語言來偏好任何其他語言。</span><span class="sxs-lookup"><span data-stu-id="6e23d-118">Mismatched Multiple Languages—After factoring out any common languages between the file being installed and the file on the computer, any remaining languages are favored according to what is needed by the product being installed.</span></span>

<span data-ttu-id="6e23d-119">保留超集合語言：無論檔案是否已在電腦上或正在安裝，都會保留支援多種語言的檔案。</span><span class="sxs-lookup"><span data-stu-id="6e23d-119">Preserve Superset Languages—Preserve the file that supports multiple languages regardless of whether it is already on the computer or is being installed.</span></span>

<span data-ttu-id="6e23d-120">Nonversioned 檔案是使用者資料—如果修改日期晚于電腦上檔案的建立日期，請勿安裝檔案，因為系統會刪除使用者自訂。</span><span class="sxs-lookup"><span data-stu-id="6e23d-120">Nonversioned Files are User Data—If the Modified date is later than the Create date for the file on the computer, do not install the file because user customizations would be deleted.</span></span> <span data-ttu-id="6e23d-121">如果修改日期和建立日期相同，請安裝檔案。</span><span class="sxs-lookup"><span data-stu-id="6e23d-121">If the Modified and Create dates are the same, install the file.</span></span> <span data-ttu-id="6e23d-122">如果建立日期晚于修改日期，則會將檔案視為未修改，並安裝檔案。</span><span class="sxs-lookup"><span data-stu-id="6e23d-122">If the Create date is later than the Modified date, the file is considered unmodified, install the file.</span></span>

<span data-ttu-id="6e23d-123">[隨附](companion-files.md)檔案的安裝並不依賴自己的檔案版本設定資訊，而是在其附屬父系的版本控制上。</span><span class="sxs-lookup"><span data-stu-id="6e23d-123">The installation of a [Companion File](companion-files.md) depends not on its own file versioning information, but on the versioning of its companion parent.</span></span> <span data-ttu-id="6e23d-124">在隨附檔案的情況下，只有在父檔案的版本較高時，才會略過安裝。</span><span class="sxs-lookup"><span data-stu-id="6e23d-124">In the case of Companion Files, the installation is skipped only if the parent file has a higher version.</span></span> <span data-ttu-id="6e23d-125">請注意，做為元件之金鑰路徑的檔案不能是隨附的檔案，因為這會導致金鑰路徑檔案的版本設定邏輯是由隨附的父檔案所決定。</span><span class="sxs-lookup"><span data-stu-id="6e23d-125">Note that a file that is the key path for its component must not be a companion file because this results in the versioning logic of the key path file being determined by the companion parent file.</span></span>

<span data-ttu-id="6e23d-126">使用 [隨附](companion-files.md)檔案的 Nonversioned 檔案-與已建立版本的檔案相關聯的 Nonversioned 檔案，該檔案會使用已建立版本之檔案的規則所遵守的隨附機制來建立關聯的檔案。</span><span class="sxs-lookup"><span data-stu-id="6e23d-126">Nonversioned Files Using [Companion Files](companion-files.md)-A nonversioned file that is associated with a versioned file using the companion mechanism abides by the rules for the versioned file.</span></span> <span data-ttu-id="6e23d-127">唯一的例外狀況是，如果電腦上已建立版本的檔案，且安裝的版本檔案具有相同的版本和語言，但是電腦上遺漏了附屬檔案。</span><span class="sxs-lookup"><span data-stu-id="6e23d-127">The only exception is if the versioned file on the computer and the versioned file being installed have the same version and language but the companion file is missing on the computer.</span></span> <span data-ttu-id="6e23d-128">在此情況下，即使使用電腦上已建立版本的檔案，仍會使用所安裝的隨附檔案。</span><span class="sxs-lookup"><span data-stu-id="6e23d-128">In this case the companion file being installed is used even though the versioned file on the computer is used.</span></span> <span data-ttu-id="6e23d-129">此外，如果 [**REINSTALLMODE**](reinstallmode.md) 屬性包含覆寫舊版選項 ( "o" 或 "e" ) ，而隨附檔案的版本等於已存在於電腦上的檔案，則會安裝使用隨附檔案的 nonversioned 檔案。</span><span class="sxs-lookup"><span data-stu-id="6e23d-129">Additionally, a nonversioned file using a companion file is installed if the [**REINSTALLMODE**](reinstallmode.md) property includes the overwrite older versions options ("o" or "e") and the companion file's version is equal to a file already on the machine.</span></span>

<span data-ttu-id="6e23d-130">規則是全域的，用來決定何時要安裝檔案的規則會位於安裝程式內的一個位置，而且是全域的，這表示它們同樣適用于所有檔案。</span><span class="sxs-lookup"><span data-stu-id="6e23d-130">Rules are Global—The rules for determining when to install a file reside in one place within the installer and are global, meaning they apply to all files equally.</span></span>

<span data-ttu-id="6e23d-131">如需用於檔案版本之格式的範例，請參閱 [版本](version.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="6e23d-131">For examples of the format used for file versions, see the [Version](version.md) data type.</span></span> <span data-ttu-id="6e23d-132">如需更具體的資訊，請參閱 [取代現有](replacing-existing-files.md) 的檔案或 [預設檔案版本控制](default-file-versioning.md)。</span><span class="sxs-lookup"><span data-stu-id="6e23d-132">For more specific information, see [Replacing Existing Files](replacing-existing-files.md) or [Default File Versioning](default-file-versioning.md).</span></span>

 

 



