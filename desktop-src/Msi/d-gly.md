---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: d6dd73e7-657f-4f71-8e9b-70369cb21972
title: 'D (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e2673f845d85db88d55cbcd53838f7e682dbe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690836"
---
# <a name="d-windows-installer"></a><span data-ttu-id="29333-103">D (Windows Installer) </span><span class="sxs-lookup"><span data-stu-id="29333-103">D (Windows Installer)</span></span>

<span data-ttu-id="29333-104">[](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [](u-gly.md) [W X](v-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="29333-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="29333-105"><span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**database 函數**</span><span class="sxs-lookup"><span data-stu-id="29333-105"><span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**database function**</span></span>
</dt> <dd>

<span data-ttu-id="29333-106">存取安裝程式資料庫。</span><span class="sxs-lookup"><span data-stu-id="29333-106">Accesses the installer database.</span></span> <span data-ttu-id="29333-107">這些函式主要是提供給 [*安裝程式套件 authoring tools*](i-gly.md) 使用，它們並不適合用來呼叫安裝程式服務。</span><span class="sxs-lookup"><span data-stu-id="29333-107">These functions are provided primarily for use by [*installer package authoring tools*](i-gly.md) and they are not intended to be used to call installer services.</span></span> <span data-ttu-id="29333-108">如需詳細資訊，請參閱 [資料庫函數](database-functions.md) 和 [安裝程式函數參考](installer-function-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="29333-108">For more information, see [Database Functions](database-functions.md) and the [Installer Function Reference](installer-function-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="29333-109"><span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**資料庫控制碼**</span><span class="sxs-lookup"><span data-stu-id="29333-109"><span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**database handle**</span></span>
</dt> <dd>

<span data-ttu-id="29333-110">使用資料庫時所需。</span><span class="sxs-lookup"><span data-stu-id="29333-110">Required for working with a database.</span></span> <span data-ttu-id="29333-111">如需詳細資訊，請參閱 [取得資料庫控制碼](obtaining-a-database-handle.md)。</span><span class="sxs-lookup"><span data-stu-id="29333-111">For more information, see [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span>

</dd> <dt>

<span data-ttu-id="29333-112"><span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**delta patch**</span><span class="sxs-lookup"><span data-stu-id="29333-112"><span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**delta patch**</span></span>
</dt> <dd>

<span data-ttu-id="29333-113">Delta patch 是使用支援差異壓縮的工具（例如 Patchwiz.dll）所建立的差異壓縮 Windows Installer 修補程式。</span><span class="sxs-lookup"><span data-stu-id="29333-113">A delta patch is a delta-compressed Windows Installer patch created using a tool, such as Patchwiz.dll, that supports delta compression.</span></span> <span data-ttu-id="29333-114">使用差異壓縮的修補程式可以減少更新的大小，方法是在目的電腦上的現有檔案和所需的新檔案之間提供差異)  (差異。</span><span class="sxs-lookup"><span data-stu-id="29333-114">Patches that use delta compression can reduce the size of an update by providing only the differences (deltas) between existing files on a target computer and the desired new files.</span></span> <span data-ttu-id="29333-115">然後從現有的檔案和下載的差異合成所需的新檔案。</span><span class="sxs-lookup"><span data-stu-id="29333-115">The desired new files are then synthesized from the existing files and the downloaded deltas.</span></span> <span data-ttu-id="29333-116">如需差異壓縮技術的詳細資訊，請參閱 [差異壓縮應用程式開發介面](https://msdn.microsoft.com/library/ms811406.aspx)。</span><span class="sxs-lookup"><span data-stu-id="29333-116">For more information about delta compression technology, see the [Delta Compression Application Programming Interface](https://msdn.microsoft.com/library/ms811406.aspx).</span></span>

</dd> </dl>

 

 



