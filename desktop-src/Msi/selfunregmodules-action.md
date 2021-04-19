---
description: SelfUnregModules 動作會將 SelfReg 資料表中所列的所有模組取消註冊，而這些模組已排程要卸載。 安裝程式不會自行註冊。EXE 檔案。
ms.assetid: fa5a5abb-ecd4-434c-b176-83cdca280a13
title: SelfUnregModules 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3a0d98d8a8afe45b9b78f5c8af8ca2f84b2244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996997"
---
# <a name="selfunregmodules-action"></a><span data-ttu-id="13932-104">SelfUnregModules 動作</span><span class="sxs-lookup"><span data-stu-id="13932-104">SelfUnregModules Action</span></span>

<span data-ttu-id="13932-105">SelfUnregModules 動作會將 [SelfReg 資料表](selfreg-table.md) 中所列的所有模組取消註冊，而這些模組已排程要卸載。</span><span class="sxs-lookup"><span data-stu-id="13932-105">The SelfUnregModules action unregisters all modules listed in the [SelfReg table](selfreg-table.md) that are scheduled to be uninstalled.</span></span> <span data-ttu-id="13932-106">安裝程式不會自行註冊。EXE 檔案。</span><span class="sxs-lookup"><span data-stu-id="13932-106">The installer does not self-register .EXE files.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="13932-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="13932-107">Sequence Restrictions</span></span>

<span data-ttu-id="13932-108">[InstallValidate](installvalidate-action.md)動作必須出現在序列中的 SelfUnregModules 動作之前。</span><span class="sxs-lookup"><span data-stu-id="13932-108">The [InstallValidate](installvalidate-action.md) action must appear before the SelfUnregModules action in the sequence.</span></span> <span data-ttu-id="13932-109">如果使用 [SelfRegModules](selfregmodules-action.md) 動作，它必須出現在序列中的 SelfUnregModules 動作之後。</span><span class="sxs-lookup"><span data-stu-id="13932-109">If a [SelfRegModules](selfregmodules-action.md) action is used it must appear after the SelfUnregModules action in the sequence.</span></span> <span data-ttu-id="13932-110">如果使用 [RemoveFiles 動作](removefiles-action.md) ，它必須出現在序列中的 SelfUnregModules 動作之後。</span><span class="sxs-lookup"><span data-stu-id="13932-110">If a [RemoveFiles action](removefiles-action.md) is used it must appear after the SelfUnregModules action in the sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="13932-111">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="13932-111">ActionData Messages</span></span>



| <span data-ttu-id="13932-112">欄位</span><span class="sxs-lookup"><span data-stu-id="13932-112">Field</span></span> | <span data-ttu-id="13932-113">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="13932-113">Description of action data</span></span>                             |
|-------|--------------------------------------------------------|
| <span data-ttu-id="13932-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="13932-114">\[1\]</span></span> | <span data-ttu-id="13932-115">未註冊的模組檔案識別碼。</span><span class="sxs-lookup"><span data-stu-id="13932-115">Identifier of unregistered module file.</span></span>                |
| <span data-ttu-id="13932-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="13932-116">\[2\]</span></span> | <span data-ttu-id="13932-117">持有未註冊模組檔案的資料夾識別碼。</span><span class="sxs-lookup"><span data-stu-id="13932-117">Identifier of folder holding unregistered module file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="13932-118">備註</span><span class="sxs-lookup"><span data-stu-id="13932-118">Remarks</span></span>

<span data-ttu-id="13932-119">SelfUnregModules 動作會嘗試呼叫要取消註冊之模組的 [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) 函式。</span><span class="sxs-lookup"><span data-stu-id="13932-119">The SelfUnregModules action attempts to call the [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) function of the module that is to be unregistered.</span></span> <span data-ttu-id="13932-120">當以較高的許可權執行安裝時，此動作會以較高的許可權執行，例如在個別電腦安裝期間。</span><span class="sxs-lookup"><span data-stu-id="13932-120">This action runs with elevated privileges when the installation is being run with elevated privileges, such as during a per-machine installation.</span></span> <span data-ttu-id="13932-121">在每一使用者安裝期間，安裝程式會以使用者權限執行此動作。</span><span class="sxs-lookup"><span data-stu-id="13932-121">During a per-user installation, the installer runs this action with user privileges.</span></span>

<span data-ttu-id="13932-122">請注意，您不能指定安裝程式使用 SelfUnRegModules 動作來取消註冊 Dll 的順序。</span><span class="sxs-lookup"><span data-stu-id="13932-122">Note that you cannot specify the order in which the installer unregisters self-registering DLLs by using the SelfUnRegModules action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13932-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="13932-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13932-124">指定自我註冊的順序</span><span class="sxs-lookup"><span data-stu-id="13932-124">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
