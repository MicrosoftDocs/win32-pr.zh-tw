---
description: 如果您打算將一或多個檔案類型與新的應用程式產生關聯，您必須為要與應用程式建立關聯的每個檔案類型定義 ProgID。
ms.assetid: 997600C9-5264-44EC-BAEC-CB5CEEA0BD14
title: 如何註冊新應用程式的檔案類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728cc48075ab1c2631f0a950059da65ae326ae79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973136"
---
# <a name="how-to-register-a-file-type-for-a-new-application"></a><span data-ttu-id="05ca8-103">如何註冊新應用程式的檔案類型</span><span class="sxs-lookup"><span data-stu-id="05ca8-103">How to Register a File Type for a New Application</span></span>

<span data-ttu-id="05ca8-104">如果您打算將一或多個檔案類型與新的應用程式產生關聯，您必須為要與應用程式建立關聯的每個檔案類型定義 ProgID。</span><span class="sxs-lookup"><span data-stu-id="05ca8-104">If you plan to associate one or more file types with a new application, you must define a ProgID for each file type that you want to associate with the application.</span></span>

<span data-ttu-id="05ca8-105">若要為您的應用程式所處理的每個唯一檔案類型建立 ProgID，請使用下列步驟。</span><span class="sxs-lookup"><span data-stu-id="05ca8-105">To create a ProgID for each unique file type that your application handles, use these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="05ca8-106">指示</span><span class="sxs-lookup"><span data-stu-id="05ca8-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="05ca8-107">步驟 1:</span><span class="sxs-lookup"><span data-stu-id="05ca8-107">Step 1:</span></span>

<span data-ttu-id="05ca8-108">請注意，某些檔案類型有多個指向相同 ProgID 的副檔名;例如：</span><span class="sxs-lookup"><span data-stu-id="05ca8-108">Note that some file types have multiple extensions that point to the same ProgID; for example:</span></span>

-   <span data-ttu-id="05ca8-109">**HKEY \_類別 \_ ROOT** \\ **App** (您的 ProgID) </span><span class="sxs-lookup"><span data-stu-id="05ca8-109">**HKEY\_CLASSES\_ROOT**\\**App.jpeg** (your ProgID)</span></span>
-   <span data-ttu-id="05ca8-110">**HKEY \_類別 \_ ROOT** \\ **.jpg** = app.config (檔案類型對應) </span><span class="sxs-lookup"><span data-stu-id="05ca8-110">**HKEY\_CLASSES\_ROOT**\\ **.jpg** = App.jpeg (the file type mappings)</span></span>
-   <span data-ttu-id="05ca8-111">**HKEY \_類別 \_ ROOT** \\ **. jpeg** = app.config</span><span class="sxs-lookup"><span data-stu-id="05ca8-111">**HKEY\_CLASSES\_ROOT**\\ **.jpeg** = App.jpeg</span></span>

### <a name="step-2"></a><span data-ttu-id="05ca8-112">步驟 2:</span><span class="sxs-lookup"><span data-stu-id="05ca8-112">Step 2:</span></span>

<span data-ttu-id="05ca8-113">當您安裝和卸載程式時，請移除 ProgID 值。</span><span class="sxs-lookup"><span data-stu-id="05ca8-113">Remove the ProgID values when you install and uninstall your program.</span></span>

### <a name="step-3"></a><span data-ttu-id="05ca8-114">步驟 3：</span><span class="sxs-lookup"><span data-stu-id="05ca8-114">Step 3:</span></span>

<span data-ttu-id="05ca8-115">卸載時，將檔案類型對應保持不變。</span><span class="sxs-lookup"><span data-stu-id="05ca8-115">Leave the file type mappings unchanged at uninstall time.</span></span> <span data-ttu-id="05ca8-116">這樣做的運作方式是因為檔案類型對應會儲存在 HKEY 類別根目錄中的每位使用者 \_ \_ \\ ，而且系統會識別缺少 ProgID 值的情況，並忽略它。</span><span class="sxs-lookup"><span data-stu-id="05ca8-116">Doing so works because file type mappings are stored per user in HKEY\_CLASSES\_ROOT\\.ext, and the system identifies the case where the ProgID value is missing and ignores it.</span></span> <span data-ttu-id="05ca8-117">將檔案類型對應保持不變，可避免只有當值仍指向您的 ProgID 時，才需要具有只會移除檔案類型對應的條件式程式碼。</span><span class="sxs-lookup"><span data-stu-id="05ca8-117">Leaving file type mappings unchanged avoids the need to have conditional code that only removes the file type mapping if the value still points to your ProgID.</span></span> <span data-ttu-id="05ca8-118">在其他應用程式可能已變更的情況下，請務必避免這種情況，因此無法輕易地移除值。</span><span class="sxs-lookup"><span data-stu-id="05ca8-118">It is important to avoid doing so in cases where it might have been changed by another application and you thus cannot easily remove the value.</span></span>

### <a name="step-4"></a><span data-ttu-id="05ca8-119">步驟 4：</span><span class="sxs-lookup"><span data-stu-id="05ca8-119">Step 4:</span></span>

<span data-ttu-id="05ca8-120">執行下列其中一項動作，以指定每個檔案類型 ProgID 之檔案類型描述的唯一值：</span><span class="sxs-lookup"><span data-stu-id="05ca8-120">Specify a unique value for the file type description of each file type ProgID by doing one of the following:</span></span>

-   <span data-ttu-id="05ca8-121">將 ProgID 的預設值保留為空白，在此情況下，系統會使用副檔名檔案。</span><span class="sxs-lookup"><span data-stu-id="05ca8-121">Leave the default value of the ProgID empty, in which case the system uses the .ext file.</span></span>
-   <span data-ttu-id="05ca8-122">透過 FriendlyTypeName 提供當地語系化的值，並且與直接讀取登錄的舊應用程式相容，請務必提供 ProgID 的預設值做為檔案類型描述 (也就是使用英文資源) 中的 FriendlyTypeName 所參考的相同值。</span><span class="sxs-lookup"><span data-stu-id="05ca8-122">Provide a localized value via FriendlyTypeName and, for compatibility with old applications that read the registry directly, be sure to provide the default value of the ProgID as the file type description (that is, use the same value that is referred to by the FriendlyTypeName in the English resource).</span></span>

## <a name="remarks"></a><span data-ttu-id="05ca8-123">備註</span><span class="sxs-lookup"><span data-stu-id="05ca8-123">Remarks</span></span>

<span data-ttu-id="05ca8-124">如果您打算將檔案與現有的應用程式建立關聯，請在登錄中找出應用程式 ProgID。</span><span class="sxs-lookup"><span data-stu-id="05ca8-124">If you plan to associate the file with an existing application, locate an application ProgID in the registry.</span></span> <span data-ttu-id="05ca8-125">如需詳細資訊，請參閱 [檔案類型](fa-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="05ca8-125">For more information, see [File Types](fa-file-types.md).</span></span>

 

 



