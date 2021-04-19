---
description: 您可以使用這些指導方針，透過數位簽章來涵蓋整個 Windows Installer 安裝。
ms.assetid: e70eab94-4615-4a73-bccc-e16bd24551f6
title: 撰寫經過完整驗證的已簽署安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e76bbfb77eab8b020cb1591847d2a36d09c96a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974649"
---
# <a name="authoring-a-fully-verified-signed-installation"></a><span data-ttu-id="d259f-103">撰寫經過完整驗證的已簽署安裝</span><span class="sxs-lookup"><span data-stu-id="d259f-103">Authoring a Fully Verified Signed Installation</span></span>

<span data-ttu-id="d259f-104">您可以使用這些指導方針，透過數位簽章來涵蓋整個 Windows Installer 安裝。</span><span class="sxs-lookup"><span data-stu-id="d259f-104">You can use these guidelines to cover an entire Windows Installer installation by a digital signature.</span></span>

<span data-ttu-id="d259f-105">Windows Installer 安裝的作者必須遵守下列各項，以確保安裝的所有部分都包含在數位簽章中：</span><span class="sxs-lookup"><span data-stu-id="d259f-105">Authors of Windows Installer installations must adhere to the following to ensure that all parts of the installation are covered by a digital signature:</span></span>

-   <span data-ttu-id="d259f-106">使用內部封包檔，或使用已簽署的外部封包檔，並正確地撰寫 [MsiDigitalSignature 資料表](msidigitalsignature-table.md) 和 [MsiDigitalCertificate 資料表](msidigitalcertificate-table.md)。</span><span class="sxs-lookup"><span data-stu-id="d259f-106">Use internal cabinet files, or use signed external cabinet files and correctly author the [MsiDigitalSignature table](msidigitalsignature-table.md) and [MsiDigitalCertificate table](msidigitalcertificate-table.md).</span></span>
-   <span data-ttu-id="d259f-107">只使用儲存在封裝內或隨封裝一起安裝的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="d259f-107">Use only custom actions stored within the package or installed with the package.</span></span>
-   <span data-ttu-id="d259f-108">簽署安裝套件。</span><span class="sxs-lookup"><span data-stu-id="d259f-108">Sign the installation package.</span></span>
-   <span data-ttu-id="d259f-109">在封裝中包含 [MsiPatchCertificate 資料表](msipatchcertificate-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="d259f-109">Include an [MsiPatchCertificate table](msipatchcertificate-table.md) in the package.</span></span> <span data-ttu-id="d259f-110">若要啟用 [使用者帳戶控制 (UAC) 修補](user-account-control--uac--patching.md)，此資料表必須包含用來識別用來數位簽署修補程式之簽署者憑證的資訊。</span><span class="sxs-lookup"><span data-stu-id="d259f-110">To enable [User Account Control (UAC) Patching](user-account-control--uac--patching.md), this table must contain information used to identify the signer certificates used to digitally sign patches.</span></span> <span data-ttu-id="d259f-111">UAC 修補讓安裝套件的作者能夠找出可供非系統管理員使用者未來套用的數位簽署修補程式。</span><span class="sxs-lookup"><span data-stu-id="d259f-111">UAC patching enables the author of the installation package to identify digitally-signed patches that can be applied in the future by non-administrator users.</span></span>

<span data-ttu-id="d259f-112">如需示範如何使用自動化撰寫已簽署安裝的範例，請參閱 [使用自動化撰寫經過完整驗證的已簽署安裝](authoring-a-fully-verified-signed-installation-using-automation.md)。</span><span class="sxs-lookup"><span data-stu-id="d259f-112">For an example showing how to author a signed installation using automation, see [Authoring a Fully Verified Signed Installation Using Automation](authoring-a-fully-verified-signed-installation-using-automation.md).</span></span>

 

 



