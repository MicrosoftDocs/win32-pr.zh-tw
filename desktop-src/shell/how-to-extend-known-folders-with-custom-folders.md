---
description: 獨立軟體廠商 (Isv) 可以藉由註冊自己的已知資料夾，在系統上擴充已知的資料夾集。
ms.assetid: bb2c63e6-7525-4d20-ac50-591b3e53dea2
title: 如何使用自訂資料夾擴充已知資料夾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3556b2e28664c63e7bc3b5fa28cf8696f679bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192686"
---
# <a name="how-to-extend-known-folders-with-custom-folders"></a><span data-ttu-id="53858-103">如何使用自訂資料夾擴充已知資料夾</span><span class="sxs-lookup"><span data-stu-id="53858-103">How to Extend Known Folders with Custom Folders</span></span>

<span data-ttu-id="53858-104">獨立軟體廠商 (Isv) 可以藉由註冊自己的已知資料夾，在系統上擴充已知的資料夾集。</span><span class="sxs-lookup"><span data-stu-id="53858-104">Independent software vendors (ISVs) can extend the set of known folders on a system by registering known folders of their own.</span></span> <span data-ttu-id="53858-105">註冊之後，系統就會知道這些協力廠商資料夾。</span><span class="sxs-lookup"><span data-stu-id="53858-105">Once registered, those third-party folders are known to the system.</span></span> <span data-ttu-id="53858-106">[**IKnownFolderManager：： GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids)的任何呼叫都可以找到它們。</span><span class="sxs-lookup"><span data-stu-id="53858-106">They are found by any call to [**IKnownFolderManager::GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids).</span></span> <span data-ttu-id="53858-107">請注意，已知的資料夾必須是每部電腦的資料夾。</span><span class="sxs-lookup"><span data-stu-id="53858-107">Note that a known folder must be a per-machine folder.</span></span> <span data-ttu-id="53858-108">您無法建立每個使用者的已知資料夾。</span><span class="sxs-lookup"><span data-stu-id="53858-108">You cannot create a per-user known folder.</span></span>

## <a name="instructions"></a><span data-ttu-id="53858-109">指示</span><span class="sxs-lookup"><span data-stu-id="53858-109">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="53858-110">步驟 1:</span><span class="sxs-lookup"><span data-stu-id="53858-110">Step 1:</span></span>

<span data-ttu-id="53858-111">透過 [**KNOWNFOLDER \_ 定義**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition) 結構定義您的已知資料夾。</span><span class="sxs-lookup"><span data-stu-id="53858-111">Define your known folder through a [**KNOWNFOLDER\_DEFINITION**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition) structure.</span></span>

### <a name="step-2"></a><span data-ttu-id="53858-112">步驟 2:</span><span class="sxs-lookup"><span data-stu-id="53858-112">Step 2:</span></span>

<span data-ttu-id="53858-113">透過呼叫 [**IKnownFolderManager：： RegisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder)來註冊已知資料夾。</span><span class="sxs-lookup"><span data-stu-id="53858-113">Register the known folder through a call to [**IKnownFolderManager::RegisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder).</span></span>

## <a name="remarks"></a><span data-ttu-id="53858-114">備註</span><span class="sxs-lookup"><span data-stu-id="53858-114">Remarks</span></span>

<span data-ttu-id="53858-115">如果您在安裝程式中為您的應用程式建立了已知資料夾，您也必須在卸載程式碼中包含 [**IKnownFolderManager：： UnregisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) 。</span><span class="sxs-lookup"><span data-stu-id="53858-115">If you create a known folder for your application as part of your installation procedure, you must also include [**IKnownFolderManager::UnregisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) as part of your uninstallation code.</span></span>

<span data-ttu-id="53858-116">在註冊之前，請考慮您要將資料夾包含在已知資料夾系統中的原因。</span><span class="sxs-lookup"><span data-stu-id="53858-116">Give consideration to why you want your folder to be included in the known folder system before you register it.</span></span> <span data-ttu-id="53858-117">您應具有將資料夾提升至該層級的系統可見度的有效理由。</span><span class="sxs-lookup"><span data-stu-id="53858-117">You should have a valid reason for elevating your folder to that level of system visibility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53858-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="53858-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="53858-119">[已知資料夾範例](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="53858-119">[Known Folders Sample](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span></span>
</dt> </dl>

 

 
