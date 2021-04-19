---
description: IPv6 的 IPSec 原則和安全性關聯的設定是使用 Ipsec6.exe 完成。
ms.assetid: 9a0c8e48-bc57-461d-9ade-54b75f7aa56d
title: Ipsec6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b373e8ab0dc54c3c8ee2fae8bc05722a9ac6aa64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989912"
---
# <a name="ipsec6exe"></a><span data-ttu-id="cdf48-103">Ipsec6.exe</span><span class="sxs-lookup"><span data-stu-id="cdf48-103">Ipsec6.exe</span></span>

<span data-ttu-id="cdf48-104">IPv6 的 IPSec 原則和安全性關聯的設定是使用 Ipsec6.exe 完成。</span><span class="sxs-lookup"><span data-stu-id="cdf48-104">Configuration of IPSec policies and security associations for IPv6 is done with Ipsec6.exe.</span></span> <span data-ttu-id="cdf48-105">以下是 Ipsec6.exe 子命令：</span><span class="sxs-lookup"><span data-stu-id="cdf48-105">The following are Ipsec6.exe subcommands:</span></span>

<dl> <dt>

<span data-ttu-id="cdf48-106"><span id="ipsec6_sp__Interface_"></span><span id="ipsec6_sp__interface_"></span><span id="IPSEC6_SP__INTERFACE_"></span>**ipsec6 sp \[**_介面_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="cdf48-106"><span id="ipsec6_sp__Interface_"></span><span id="ipsec6_sp__interface_"></span><span id="IPSEC6_SP__INTERFACE_"></span>**ipsec6 sp \[**_Interface_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="cdf48-107">顯示作用中的安全性原則。</span><span class="sxs-lookup"><span data-stu-id="cdf48-107">Displays active security policies.</span></span> <span data-ttu-id="cdf48-108">或者，會顯示特定介面的作用中安全性原則。</span><span class="sxs-lookup"><span data-stu-id="cdf48-108">Alternately, displays active security policies for a specific interface.</span></span>

</dd> <dt>

<span data-ttu-id="cdf48-109"><span id="ipsec6_sa"></span><span id="IPSEC6_SA"></span>**ipsec6 sa**</span><span class="sxs-lookup"><span data-stu-id="cdf48-109"><span id="ipsec6_sa"></span><span id="IPSEC6_SA"></span>**ipsec6 sa**</span></span>
</dt> <dd>

<span data-ttu-id="cdf48-110">顯示作用中的安全性關聯。</span><span class="sxs-lookup"><span data-stu-id="cdf48-110">Displays active security associations.</span></span>

</dd> <dt>

<span data-ttu-id="cdf48-111"><span id="ipsec6_c__FileName_without_extension__"></span><span id="ipsec6_c__filename_without_extension__"></span><span id="IPSEC6_C__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 c \[**_沒有副檔名的檔案名 ()_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="cdf48-111"><span id="ipsec6_c__FileName_without_extension__"></span><span id="ipsec6_c__filename_without_extension__"></span><span id="IPSEC6_C__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 c \[**_FileName(without extension)_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="cdf48-112">建立用來設定安全性原則和安全性關聯的檔案。</span><span class="sxs-lookup"><span data-stu-id="cdf48-112">Creates files used to configure security policy and security associations.</span></span> <span data-ttu-id="cdf48-113">建立安全性原則和 *檔案名* 為 Spd 的 *檔案名*。如果是安全性關聯，則為悲傷。</span><span class="sxs-lookup"><span data-stu-id="cdf48-113">Creates *FileName*.spd for security policies and *FileName*.sad for security associations.</span></span> <span data-ttu-id="cdf48-114">使用已建立的檔案做為範本，以設定安全性原則或安全性關聯。</span><span class="sxs-lookup"><span data-stu-id="cdf48-114">Use the created files as templates to configure security policies or security associations.</span></span> <span data-ttu-id="cdf48-115">您可以使用文字編輯器來修改檔案。</span><span class="sxs-lookup"><span data-stu-id="cdf48-115">The files can be modified with a text editor.</span></span> <span data-ttu-id="cdf48-116">若要叫用包含在 SPD 和悲傷檔案中的設定，請使用 **ipsec6** 命令。</span><span class="sxs-lookup"><span data-stu-id="cdf48-116">To invoke the configuration contained in the SPD and SAD files, use the **ipsec6 a** command.</span></span>

</dd> <dt>

<span data-ttu-id="cdf48-117"><span id="ipsec6_a__FileName_without_extension__"></span><span id="ipsec6_a__filename_without_extension__"></span><span id="IPSEC6_A__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 \[**_沒有副檔名的檔案名 ()_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="cdf48-117"><span id="ipsec6_a__FileName_without_extension__"></span><span id="ipsec6_a__filename_without_extension__"></span><span id="IPSEC6_A__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 a \[**_FileName(without extension)_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="cdf48-118">將 *檔案名中* 的安全性原則（副檔名為 spd 和安全性關聯）新增至有效的安全性原則和安全性關聯 *清單。*</span><span class="sxs-lookup"><span data-stu-id="cdf48-118">Adds security policies in *FileName*.spd and security associations in *FileName*.sad to the list of active security policies and security associations.</span></span>

</dd> <dt>

<span data-ttu-id="cdf48-119"><span id="ipsec6_i__Policy___FileName_without_extension__"></span><span id="ipsec6_i__policy___filename_without_extension__"></span><span id="IPSEC6_I__POLICY___FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 i \[** *_原則 \] 檔案名 \[_* _(沒有副檔名)_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="cdf48-119"><span id="ipsec6_i__Policy___FileName_without_extension__"></span><span id="ipsec6_i__policy___filename_without_extension__"></span><span id="IPSEC6_I__POLICY___FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 i \[**_Policy_*_\] \[_*_FileName(without extension)_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="cdf48-120">將 filename 中的安全性原則和 *檔案名\*\*中的* 安全性關聯新增至 active 安全性原則和安全性關聯的清單，如原則編號所參考。</span><span class="sxs-lookup"><span data-stu-id="cdf48-120">Adds security policies in *FileName*.spd and security associations in *FileName*.sad to the list of active security policies and security associations as referenced by policy number.</span></span>

</dd> <dt>

<span data-ttu-id="cdf48-121"><span id="ipsec6_d__type___sp_sa___IndexNumber_"></span><span id="ipsec6_d__type___sp_sa___indexnumber_"></span><span id="IPSEC6_D__TYPE___SP_SA___INDEXNUMBER_"></span>**ipsec6 d \[ type = sp sa \] \[** _IndexNumber_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="cdf48-121"><span id="ipsec6_d__type___sp_sa___IndexNumber_"></span><span id="ipsec6_d__type___sp_sa___indexnumber_"></span><span id="IPSEC6_D__TYPE___SP_SA___INDEXNUMBER_"></span>**ipsec6 d \[type = sp sa\] \[**_IndexNumber_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="cdf48-122">會從作用中的安全性原則和安全性關聯清單中刪除安全性原則或安全性關聯， (使用 **ipsec6 sp** 或 **ipsec6 sa**) 來顯示它們的索引編號。</span><span class="sxs-lookup"><span data-stu-id="cdf48-122">Deletes security policies or security associations from the list of active security policies and security associations, as referenced by their index number (displayed with **ipsec6 sp** or **ipsec6 sa**).</span></span>

</dd> </dl>

 

 



