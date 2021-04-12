---
description: Windows Installer 可以使用數位簽章作為偵測損毀資源的途徑。
ms.assetid: fc982813-583b-4fcd-88d8-9de227994e7b
title: Msicert.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0a4df800bbcfa9ed2fb0d016794b3ebcf1535be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195278"
---
# <a name="msicertexe"></a><span data-ttu-id="3974a-103">Msicert.exe</span><span class="sxs-lookup"><span data-stu-id="3974a-103">Msicert.exe</span></span>

<span data-ttu-id="3974a-104">Windows Installer 可以使用數位簽章作為偵測損毀資源的途徑。</span><span class="sxs-lookup"><span data-stu-id="3974a-104">Windows Installer can use digital signatures as a means to detect corrupted resources.</span></span> <span data-ttu-id="3974a-105">簽署者憑證可以與要由封裝安裝之外部資源的簽署者憑證進行比較。</span><span class="sxs-lookup"><span data-stu-id="3974a-105">A signer certificate may be compared to the signer certificate of an external resource to be installed by the package.</span></span> <span data-ttu-id="3974a-106">如需詳細資訊，請參閱 [數位簽章和 Windows Installer](digital-signatures-and-windows-installer.md)。</span><span class="sxs-lookup"><span data-stu-id="3974a-106">For more information, see [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span>

<span data-ttu-id="3974a-107">MsiCert.exe 是一種命令列公用程式，可用來將外部封包檔的數位簽章資訊填入 [MsiDigitalSignature 資料表](msidigitalsignature-table.md) 和 [MsiDigitalCertificate 資料表](msidigitalcertificate-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="3974a-107">MsiCert.exe is a command line utility that can be used to populate the [MsiDigitalSignature table](msidigitalsignature-table.md) and [MsiDigitalCertificate table](msidigitalcertificate-table.md) with the digital signature information of an external cabinet file.</span></span> <span data-ttu-id="3974a-108">封包檔必須經過數位簽署並列在 [媒體資料表](media-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="3974a-108">The cabinet file must by digitally signed and listed in the [Media table](media-table.md).</span></span> <span data-ttu-id="3974a-109">MsiCert.exe 使用數位簽署的封包中的簽署者憑證資訊，並且會建立 MsiDigitalSignature 和 MsiDigitalCertificate 資料表，並將其新增至資料庫（如果它們還不存在的話）。</span><span class="sxs-lookup"><span data-stu-id="3974a-109">MsiCert.exe uses the signer certificate information from the digitally signed cabinet and will create and add the MsiDigitalSignature and MsiDigitalCertificate tables to the database if they do not already exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="3974a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="3974a-110">Syntax</span></span>

<span data-ttu-id="3974a-111">**msicert-d** *{database}* **-m** *{媒體輸入}* **-c** *{封包}* **\[ - \] h**</span><span class="sxs-lookup"><span data-stu-id="3974a-111">**msicert -d** *{database}* **-m** *{media entry}* **-c** *{cabinet}* **\[-h\]**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="3974a-112">命令列選項</span><span class="sxs-lookup"><span data-stu-id="3974a-112">Command Line Options</span></span>

<span data-ttu-id="3974a-113">命令列選項不區分大小寫，而且可以使用斜線分隔符號，而不是虛線。</span><span class="sxs-lookup"><span data-stu-id="3974a-113">The command line options are case-insensitive and slash delimiters may be used instead of a dash.</span></span>



| <span data-ttu-id="3974a-114">選項</span><span class="sxs-lookup"><span data-stu-id="3974a-114">Option</span></span> | <span data-ttu-id="3974a-115">參數</span><span class="sxs-lookup"><span data-stu-id="3974a-115">Parameter</span></span>        | <span data-ttu-id="3974a-116">Description</span><span class="sxs-lookup"><span data-stu-id="3974a-116">Description</span></span>                                                                                             |
|--------|------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3974a-117">-d</span><span class="sxs-lookup"><span data-stu-id="3974a-117">-d</span></span>     | <database> | <span data-ttu-id="3974a-118">正在更新的資料庫 ( .msi 檔案) 。</span><span class="sxs-lookup"><span data-stu-id="3974a-118">The database (.msi file) that is being updated.</span></span>                                                         |
| <span data-ttu-id="3974a-119">-M</span><span class="sxs-lookup"><span data-stu-id="3974a-119">-m</span></span>     | <media Id> | <span data-ttu-id="3974a-120">封包檔記錄中 [媒體資料表](media-table.md) 的 [DiskId] 欄位中的專案。</span><span class="sxs-lookup"><span data-stu-id="3974a-120">The entry in the DiskId field of the [Media table](media-table.md) in the record for the cabinet file.</span></span> |
| <span data-ttu-id="3974a-121">-c</span><span class="sxs-lookup"><span data-stu-id="3974a-121">-c</span></span>     | <cabinet>  | <span data-ttu-id="3974a-122">數位簽署的封包檔路徑。</span><span class="sxs-lookup"><span data-stu-id="3974a-122">The path to the digitally signed cabinet file.</span></span>                                                          |
| <span data-ttu-id="3974a-123">-H</span><span class="sxs-lookup"><span data-stu-id="3974a-123">-h</span></span>     |                  | <span data-ttu-id="3974a-124">包含數位簽章的雜湊。</span><span class="sxs-lookup"><span data-stu-id="3974a-124">Include the hash of the digital signature.</span></span> <span data-ttu-id="3974a-125">這是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="3974a-125">This is optional.</span></span>                                            |



 

<span data-ttu-id="3974a-126">此工具僅適用于 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。</span><span class="sxs-lookup"><span data-stu-id="3974a-126">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3974a-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="3974a-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3974a-128">Windows Installer 開發工具</span><span class="sxs-lookup"><span data-stu-id="3974a-128">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="3974a-129">已發行的版本、工具和可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="3974a-129">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



