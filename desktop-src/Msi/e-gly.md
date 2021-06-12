---
description: 瞭解以字母 E 開頭的 Windows Installer 概念，例如提高許可權的和外部原始程式檔。
ms.assetid: 8f180e2c-06f4-41d5-b167-52525f4a9985
title: 'E (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2c65c50427b1f8271be838971a387388ea53db
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011091"
---
# <a name="e-windows-installer"></a><span data-ttu-id="54e1b-103">E (Windows Installer) </span><span class="sxs-lookup"><span data-stu-id="54e1b-103">E (Windows Installer)</span></span>

<span data-ttu-id="54e1b-104">[](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) E [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [](u-gly.md) [W X](v-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="54e1b-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) E [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="54e1b-105"><span id="_msi_elevated_gly"></span><span id="_MSI_ELEVATED_GLY"></span>**升高**</span><span class="sxs-lookup"><span data-stu-id="54e1b-105"><span id="_msi_elevated_gly"></span><span id="_MSI_ELEVATED_GLY"></span>**elevated**</span></span>
</dt> <dd>

<span data-ttu-id="54e1b-106">以系統許可權執行的動作會以較高的許可權來呼叫。</span><span class="sxs-lookup"><span data-stu-id="54e1b-106">Actions performed with system privileges are called elevated.</span></span>

</dd> <dt>

<span data-ttu-id="54e1b-107"><span id="_msi_execution_phase_gly"></span><span id="_MSI_EXECUTION_PHASE_GLY"></span>**執行階段**</span><span class="sxs-lookup"><span data-stu-id="54e1b-107"><span id="_msi_execution_phase_gly"></span><span id="_MSI_EXECUTION_PHASE_GLY"></span>**execution phase**</span></span>
</dt> <dd>

<span data-ttu-id="54e1b-108">當安裝程式執行安裝程式動作的腳本時。</span><span class="sxs-lookup"><span data-stu-id="54e1b-108">When the installer executes a script of installer actions.</span></span> <span data-ttu-id="54e1b-109">在 Microsoft Windows 2000 中，此程式是由安裝程式服務所執行。</span><span class="sxs-lookup"><span data-stu-id="54e1b-109">In Microsoft Windows 2000, this process is performed by the installer service.</span></span> <span data-ttu-id="54e1b-110">在受控應用程式中，腳本是以系統許可權執行。</span><span class="sxs-lookup"><span data-stu-id="54e1b-110">In a managed application, the script is executed with system privileges.</span></span> <span data-ttu-id="54e1b-111">如需詳細資訊，請參閱 [安裝機制](installation-mechanism.md)。</span><span class="sxs-lookup"><span data-stu-id="54e1b-111">For more information, see [Installation Mechanism](installation-mechanism.md).</span></span>

</dd> <dt>

<span data-ttu-id="54e1b-112"><span id="_msi_execution_script_gly"></span><span id="_MSI_EXECUTION_SCRIPT_GLY"></span>**執行腳本**</span><span class="sxs-lookup"><span data-stu-id="54e1b-112"><span id="_msi_execution_script_gly"></span><span id="_MSI_EXECUTION_SCRIPT_GLY"></span>**execution script**</span></span>
</dt> <dd>

<span data-ttu-id="54e1b-113">安裝的安裝程式動作。</span><span class="sxs-lookup"><span data-stu-id="54e1b-113">Installer actions for an installation.</span></span> <span data-ttu-id="54e1b-114">執行腳本 [*會在安裝*](a-gly.md) 期間產生，並在 [*執行階段*](/windows)期間執行。</span><span class="sxs-lookup"><span data-stu-id="54e1b-114">The execution script is generated during the [*acquisition phase*](a-gly.md) of installation and executed during the [*execution phase*](/windows).</span></span> <span data-ttu-id="54e1b-115">如需詳細資訊，請參閱 [安裝機制](installation-mechanism.md)。</span><span class="sxs-lookup"><span data-stu-id="54e1b-115">For more information, see [Installation Mechanism](installation-mechanism.md).</span></span>

</dd> <dt>

<span data-ttu-id="54e1b-116"><span id="_msi_external_source_files_gly"></span><span id="_MSI_EXTERNAL_SOURCE_FILES_GLY"></span>**外部來源檔案**</span><span class="sxs-lookup"><span data-stu-id="54e1b-116"><span id="_msi_external_source_files_gly"></span><span id="_MSI_EXTERNAL_SOURCE_FILES_GLY"></span>**external source files**</span></span>
</dt> <dd>

<span data-ttu-id="54e1b-117">所安裝之應用程式的原始程式檔，儲存在 [*.msi*](m-gly.md)檔之外。</span><span class="sxs-lookup"><span data-stu-id="54e1b-117">Source files of the application being installed that are stored outside of the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="54e1b-118">您可以將多個外部來源檔案壓縮並儲存在封裝 [*內含的*](c-gly.md) 封 [*包*](p-gly.md)檔中。</span><span class="sxs-lookup"><span data-stu-id="54e1b-118">Multiple external source files can be compressed and stored together inside of a [*cabinet file*](c-gly.md) included in the [*package*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="54e1b-119"><span id="_msi_external_user_interface_gly"></span><span id="_MSI_EXTERNAL_USER_INTERFACE_GLY"></span>**外部使用者介面**</span><span class="sxs-lookup"><span data-stu-id="54e1b-119"><span id="_msi_external_user_interface_gly"></span><span id="_MSI_EXTERNAL_USER_INTERFACE_GLY"></span>**external user interface**</span></span>
</dt> <dd>

<span data-ttu-id="54e1b-120">由安裝套件作者提供的 UI。</span><span class="sxs-lookup"><span data-stu-id="54e1b-120">UI provided by the author of an installation package.</span></span> <span data-ttu-id="54e1b-121">它不會使用安裝程式的內部 UI 功能。</span><span class="sxs-lookup"><span data-stu-id="54e1b-121">It does not use the internal UI capabilities of the installer.</span></span> <span data-ttu-id="54e1b-122">如需詳細資訊，請參閱 [關於消費者介面](about-the-user-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="54e1b-122">For more information, see [About the User Interface](about-the-user-interface.md).</span></span>

</dd> </dl>

 

 
