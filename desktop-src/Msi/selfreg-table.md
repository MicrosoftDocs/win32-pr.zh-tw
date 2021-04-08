---
description: SelfReg 資料表包含需要自行註冊之模組的相關資訊。
ms.assetid: 7fe5c96e-16a4-49c9-9a93-616608aa55b2
title: SelfReg 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5895b1d23369a7c121547fed841731b5d3e76ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695404"
---
# <a name="selfreg-table"></a><span data-ttu-id="7d1db-103">SelfReg 資料表</span><span class="sxs-lookup"><span data-stu-id="7d1db-103">SelfReg Table</span></span>

<span data-ttu-id="7d1db-104">SelfReg 資料表包含需要自行註冊之模組的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7d1db-104">The SelfReg table contains information about modules that need to be self registered.</span></span> <span data-ttu-id="7d1db-105">安裝程式會在安裝模組期間呼叫 [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) 函式;它會在模組的卸載期間呼叫 [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) 。</span><span class="sxs-lookup"><span data-stu-id="7d1db-105">The installer calls the [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) function during installation of the module; it calls [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) during uninstallation of the module.</span></span> <span data-ttu-id="7d1db-106">安裝程式不會自行註冊 EXE 檔案。</span><span class="sxs-lookup"><span data-stu-id="7d1db-106">The installer does not self register EXE files.</span></span>

<span data-ttu-id="7d1db-107">SelfReg 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="7d1db-107">The SelfReg table has the following columns.</span></span>



| <span data-ttu-id="7d1db-108">Column</span><span class="sxs-lookup"><span data-stu-id="7d1db-108">Column</span></span> | <span data-ttu-id="7d1db-109">類型</span><span class="sxs-lookup"><span data-stu-id="7d1db-109">Type</span></span>                         | <span data-ttu-id="7d1db-110">答案</span><span class="sxs-lookup"><span data-stu-id="7d1db-110">Key</span></span> | <span data-ttu-id="7d1db-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="7d1db-111">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="7d1db-112">檔案\_</span><span class="sxs-lookup"><span data-stu-id="7d1db-112">File\_</span></span> | [<span data-ttu-id="7d1db-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="7d1db-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="7d1db-114">Y</span><span class="sxs-lookup"><span data-stu-id="7d1db-114">Y</span></span>   | <span data-ttu-id="7d1db-115">N</span><span class="sxs-lookup"><span data-stu-id="7d1db-115">N</span></span>        |
| <span data-ttu-id="7d1db-116">成本</span><span class="sxs-lookup"><span data-stu-id="7d1db-116">Cost</span></span>   | [<span data-ttu-id="7d1db-117">整數</span><span class="sxs-lookup"><span data-stu-id="7d1db-117">Integer</span></span>](integer.md)       | <span data-ttu-id="7d1db-118">N</span><span class="sxs-lookup"><span data-stu-id="7d1db-118">N</span></span>   | <span data-ttu-id="7d1db-119">Y</span><span class="sxs-lookup"><span data-stu-id="7d1db-119">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7d1db-120">資料行</span><span class="sxs-lookup"><span data-stu-id="7d1db-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7d1db-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_</span><span class="sxs-lookup"><span data-stu-id="7d1db-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="7d1db-122">在 [檔資料表](file-table.md) 的第一個資料行中的外部索引鍵，表示需要註冊的模組。</span><span class="sxs-lookup"><span data-stu-id="7d1db-122">External key into the first column of the [File table](file-table.md) indicating the module that needs to be registered.</span></span>

</dd> <dt>

<span data-ttu-id="7d1db-123"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>成本</span><span class="sxs-lookup"><span data-stu-id="7d1db-123"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Cost</span></span>
</dt> <dd>

<span data-ttu-id="7d1db-124">註冊模組的成本（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7d1db-124">The cost of registering the module in bytes.</span></span> <span data-ttu-id="7d1db-125">此值必須是非負數。</span><span class="sxs-lookup"><span data-stu-id="7d1db-125">This must be a non-negative number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d1db-126">備註</span><span class="sxs-lookup"><span data-stu-id="7d1db-126">Remarks</span></span>

<span data-ttu-id="7d1db-127">使用自我註冊時，強烈建議使用安裝套件作者。</span><span class="sxs-lookup"><span data-stu-id="7d1db-127">Installation package authors are strongly advised against using self registration.</span></span> <span data-ttu-id="7d1db-128">相反地，他們應針對此目的撰寫一或多個安裝程式所提供的資料表來註冊模組。</span><span class="sxs-lookup"><span data-stu-id="7d1db-128">Instead they should register modules by authoring one or more tables provided by the installer for this purpose.</span></span> <span data-ttu-id="7d1db-129">如需詳細資訊，請參閱登錄 [資料表群組](registry-tables-group.md)。</span><span class="sxs-lookup"><span data-stu-id="7d1db-129">For more information, see [Registry Tables Group](registry-tables-group.md).</span></span> <span data-ttu-id="7d1db-130">擁有集中式安裝程式服務的許多優點會因為自我註冊而遺失，因為自我註冊常式通常會隱藏重要的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="7d1db-130">Many of the benefits of having a central installer service are lost with self registration because self-registration routines tend to hide critical configuration information.</span></span> <span data-ttu-id="7d1db-131">避免自行註冊的原因包括：</span><span class="sxs-lookup"><span data-stu-id="7d1db-131">Reasons for avoiding self registration include:</span></span>

-   <span data-ttu-id="7d1db-132">您無法使用 [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) 來安全地復原具有自我註冊模組的安裝，因為沒有辦法告知是否有其他功能或應用程式使用自行註冊的金鑰。</span><span class="sxs-lookup"><span data-stu-id="7d1db-132">Rollback of an installation with self-registered modules cannot be safely done using [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) because there is no way of telling if the self-registered keys are used by another feature or application.</span></span>
-   <span data-ttu-id="7d1db-133">如果在自我註冊常式內執行類別或延伸模組伺服器註冊，就會降低使用公告的能力。</span><span class="sxs-lookup"><span data-stu-id="7d1db-133">The ability to use advertisement is reduced if Class or extension server registration is performed within self-registration routines.</span></span>
-   <span data-ttu-id="7d1db-134">安裝程式會針對每個使用者或每一部電腦的安裝，自動處理登錄資料表中的 HKCR 機碼。</span><span class="sxs-lookup"><span data-stu-id="7d1db-134">The installer automatically handles HKCR keys in the registry tables for both per-user or per-machine installations.</span></span> <span data-ttu-id="7d1db-135">[**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) 常式目前不支援每個使用者 HKCR 索引鍵的概念。</span><span class="sxs-lookup"><span data-stu-id="7d1db-135">[**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) routines currently do not support the notion of a per-user HKCR key.</span></span>
-   <span data-ttu-id="7d1db-136">如果有多個使用者在同一部電腦上使用自我註冊的應用程式，則每位使用者在第一次執行應用程式時都必須安裝該應用程式。</span><span class="sxs-lookup"><span data-stu-id="7d1db-136">If multiple users are using a self-registered application on the same computer, each user must install the application the first time they run it.</span></span> <span data-ttu-id="7d1db-137">否則，安裝程式無法輕易判斷是否有適當的 HKCU 登錄機碼存在。</span><span class="sxs-lookup"><span data-stu-id="7d1db-137">Otherwise the installer cannot easily determine that the proper HKCU registry keys exist.</span></span>
-   <span data-ttu-id="7d1db-138">如果元件同時指定為從來源執行，而且列于 SelfReg 資料表中，則 [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) 可能會被拒絕存取網路資源（例如類型程式庫）。</span><span class="sxs-lookup"><span data-stu-id="7d1db-138">The [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) can be denied access to network resources such as type libraries if a component is both specified as run-from-source and is listed in the SelfReg table.</span></span> <span data-ttu-id="7d1db-139">這可能會導致元件的安裝在系統管理安裝期間失敗。</span><span class="sxs-lookup"><span data-stu-id="7d1db-139">This can cause the installation of the component to fail to during an administrative installation.</span></span>
-   <span data-ttu-id="7d1db-140">自我註冊 Dll 更容易撰寫程式碼錯誤，因為每個 DLL 的 [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) 所需的新程式碼通常都不同。</span><span class="sxs-lookup"><span data-stu-id="7d1db-140">Self-registering DLLs are more susceptible to coding errors because the new code required for [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) is commonly different for each DLL.</span></span> <span data-ttu-id="7d1db-141">相反地，請使用資料庫中的登錄資料表來利用安裝程式所提供的現有程式碼。</span><span class="sxs-lookup"><span data-stu-id="7d1db-141">Instead use the registry tables in the database to take advantage of existing code provided by the installer.</span></span>
-   <span data-ttu-id="7d1db-142">自我註冊 Dll 有時可以連結至不存在或版本錯誤的輔助 Dll。</span><span class="sxs-lookup"><span data-stu-id="7d1db-142">Self-registering DLLs can sometimes link to auxiliary DLLs that are not present or are the wrong version.</span></span> <span data-ttu-id="7d1db-143">相反地，安裝程式可以使用登錄資料表註冊 Dll，而不會相依于系統目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="7d1db-143">In contrast, the installer can register the DLLs using the registry tables with no dependency on the current state of the system.</span></span>

> [!Note]  
> <span data-ttu-id="7d1db-144">您無法使用 [SelfRegModules](selfregmodules-action.md) 和 [SelfUnRegModules](selfunregmodules-action.md) 動作來指定安裝程式註冊或取消註冊自行註冊 dll 的順序。</span><span class="sxs-lookup"><span data-stu-id="7d1db-144">You cannot specify the order in which the installer registers or unregisters self-registering DLLs by using the [SelfRegModules](selfregmodules-action.md) and [SelfUnRegModules](selfunregmodules-action.md) actions.</span></span> <span data-ttu-id="7d1db-145">請參閱 [指定自行註冊的順序](specifying-the-order-of-self-registration.md)。</span><span class="sxs-lookup"><span data-stu-id="7d1db-145">See [Specifying the Order of Self Registration](specifying-the-order-of-self-registration.md).</span></span>

 

## <a name="validation"></a><span data-ttu-id="7d1db-146">驗證</span><span class="sxs-lookup"><span data-stu-id="7d1db-146">Validation</span></span>

<dl>

[<span data-ttu-id="7d1db-147">ICE03</span><span class="sxs-lookup"><span data-stu-id="7d1db-147">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7d1db-148">ICE06</span><span class="sxs-lookup"><span data-stu-id="7d1db-148">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="7d1db-149">ICE32</span><span class="sxs-lookup"><span data-stu-id="7d1db-149">ICE32</span></span>](ice32.md)  
</dl>

 

 
