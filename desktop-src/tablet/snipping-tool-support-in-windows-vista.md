---
description: 本主題說明您的應用程式如何指定 Tablet PC 剪取工具在捕捉應用程式時所應取得的 URL。
ms.assetid: e31e63e8-8f6b-41f7-8bd6-afc5ca32456b
title: Windows Vista 中的剪取工具支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046dd6c8a97d1dacc20065dc1f741610fec13865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850979"
---
# <a name="snipping-tool-support-in-windows-vista"></a><span data-ttu-id="63a5f-103">Windows Vista 中的剪取工具支援</span><span class="sxs-lookup"><span data-stu-id="63a5f-103">Snipping Tool Support in Windows Vista</span></span>

<span data-ttu-id="63a5f-104">本主題說明您的應用程式如何指定 Tablet PC 剪取工具在捕捉應用程式時所應取得的 URL。</span><span class="sxs-lookup"><span data-stu-id="63a5f-104">This topic describes how your application can specify what URL the Tablet PC Snipping Tool should obtain when capturing your application.</span></span>

## <a name="specifying-the-url-via-registry-key"></a><span data-ttu-id="63a5f-105">透過登錄機碼指定 URL</span><span class="sxs-lookup"><span data-stu-id="63a5f-105">Specifying the URL via Registry Key</span></span>

<span data-ttu-id="63a5f-106">剪取工具可讓使用者在螢幕上的任何物件 (螢幕擷取畫面) 捕捉剪取，然後加上批註、儲存或共用影像。</span><span class="sxs-lookup"><span data-stu-id="63a5f-106">Snipping Tool allows users to capture a snip (screen shot) of any object on the screen and then annotate, save, or share the image.</span></span> <span data-ttu-id="63a5f-107">當資料儲存為 HTML 格式，或傳送至支援內嵌 HTML 的電子郵件客戶程式時，如果應用程式提供如何取得 URL 的相關資訊，剪取工具可以將 URL 加入至剪取。</span><span class="sxs-lookup"><span data-stu-id="63a5f-107">When the data is saved in HTML format, or when it is sent to an email client that supports inline HTML, Snipping Tool can add a URL to the snip if the application provides information on how to obtain the URL.</span></span>

<span data-ttu-id="63a5f-108">剪取工具透過協助工具物件取得 URL。</span><span class="sxs-lookup"><span data-stu-id="63a5f-108">Snipping Tool obtains the URL via accessibility objects.</span></span> <span data-ttu-id="63a5f-109">應用程式應該在下列登錄機碼底下指定必要的資訊：</span><span class="sxs-lookup"><span data-stu-id="63a5f-109">Applications should specify the necessary information under the following registry keys:</span></span>

<span data-ttu-id="63a5f-110">HKLM \\ Software \\ Microsoft \\ Windows \\ 平板 \\ 剪取工具 \\ LinkFingerprints，</span><span class="sxs-lookup"><span data-stu-id="63a5f-110">HKLM\\Software\\Microsoft\\Windows\\TabletPC\\Snipping Tool\\LinkFingerprints,</span></span>

<span data-ttu-id="63a5f-111">而且應該建立一個子機碼，其名稱與應該從中取得連結的視窗類別相同。</span><span class="sxs-lookup"><span data-stu-id="63a5f-111">And should create a subkey whose name is the same as the window class from which the link should be obtained.</span></span> <span data-ttu-id="63a5f-112">視窗類別名稱應為應用程式的最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="63a5f-112">The window class name should be the topmost window of the application.</span></span>

<span data-ttu-id="63a5f-113">HKLM \\ Software \\ Microsoft \\ Windows \\ 平板 \\ 剪取工具 \\ LinkFingerprints\\<Window Class Name></span><span class="sxs-lookup"><span data-stu-id="63a5f-113">HKLM\\Software\\Microsoft\\Windows\\TabletPC\\Snipping Tool\\LinkFingerprints\\<Window Class Name></span></span>

### <a name="window-class-key-details"></a><span data-ttu-id="63a5f-114">視窗類別索引鍵詳細資料</span><span class="sxs-lookup"><span data-stu-id="63a5f-114">Window Class Key Details</span></span>

<span data-ttu-id="63a5f-115">在視窗類別索引鍵下，應該設定適當的值，以指出剪取工具應該偵測正確的協助工具物件。</span><span class="sxs-lookup"><span data-stu-id="63a5f-115">Under the window class key, the appropriate values should be set in order to indicate Snipping Tool should detect the correct accessibility object.</span></span>



| <span data-ttu-id="63a5f-116">值</span><span class="sxs-lookup"><span data-stu-id="63a5f-116">VALUE</span></span>                        | <span data-ttu-id="63a5f-117">TYPE</span><span class="sxs-lookup"><span data-stu-id="63a5f-117">TYPE</span></span>                  | <span data-ttu-id="63a5f-118">面具</span><span class="sxs-lookup"><span data-stu-id="63a5f-118">MASK</span></span>            | <span data-ttu-id="63a5f-119">儲存的資訊</span><span class="sxs-lookup"><span data-stu-id="63a5f-119">INFORMATION STORED</span></span>                                          |
|------------------------------|-----------------------|-----------------|-------------------------------------------------------------|
| <span data-ttu-id="63a5f-120">Mask</span><span class="sxs-lookup"><span data-stu-id="63a5f-120">Mask</span></span><br/>              | <span data-ttu-id="63a5f-121">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="63a5f-121">REG\_DWORD</span></span><br/> |                 | <span data-ttu-id="63a5f-122">指出下列哪些欄位要檢查</span><span class="sxs-lookup"><span data-stu-id="63a5f-122">Indicates which of the following fields to check</span></span><br/> |
| <span data-ttu-id="63a5f-123">Name</span><span class="sxs-lookup"><span data-stu-id="63a5f-123">Name</span></span><br/>              | <span data-ttu-id="63a5f-124">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="63a5f-124">REG\_SZ</span></span><br/>    | <span data-ttu-id="63a5f-125">0x02</span><span class="sxs-lookup"><span data-stu-id="63a5f-125">0x02</span></span><br/> | <span data-ttu-id="63a5f-126">存取範圍名稱</span><span class="sxs-lookup"><span data-stu-id="63a5f-126">Accessibility name</span></span><br/>                               |
| <span data-ttu-id="63a5f-127">Description</span><span class="sxs-lookup"><span data-stu-id="63a5f-127">Description</span></span><br/>       | <span data-ttu-id="63a5f-128">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="63a5f-128">REG\_SZ</span></span><br/>    | <span data-ttu-id="63a5f-129">0x04</span><span class="sxs-lookup"><span data-stu-id="63a5f-129">0x04</span></span><br/> | <span data-ttu-id="63a5f-130">協助工具描述</span><span class="sxs-lookup"><span data-stu-id="63a5f-130">Accessibility description</span></span><br/>                        |
| <span data-ttu-id="63a5f-131">角色</span><span class="sxs-lookup"><span data-stu-id="63a5f-131">Role</span></span><br/>              | <span data-ttu-id="63a5f-132">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="63a5f-132">REG\_DWORD</span></span><br/> | <span data-ttu-id="63a5f-133">0x08</span><span class="sxs-lookup"><span data-stu-id="63a5f-133">0x08</span></span><br/> | <span data-ttu-id="63a5f-134">協助工具角色</span><span class="sxs-lookup"><span data-stu-id="63a5f-134">Accessibility role</span></span><br/>                               |
| <span data-ttu-id="63a5f-135">ParentName</span><span class="sxs-lookup"><span data-stu-id="63a5f-135">ParentName</span></span><br/>        | <span data-ttu-id="63a5f-136">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="63a5f-136">REG\_SZ</span></span><br/>    | <span data-ttu-id="63a5f-137">0x10</span><span class="sxs-lookup"><span data-stu-id="63a5f-137">0x10</span></span><br/> | <span data-ttu-id="63a5f-138">父系的協助工具名稱</span><span class="sxs-lookup"><span data-stu-id="63a5f-138">Accessibility name of parent</span></span><br/>                     |
| <span data-ttu-id="63a5f-139">ParentValue</span><span class="sxs-lookup"><span data-stu-id="63a5f-139">ParentValue</span></span><br/>       | <span data-ttu-id="63a5f-140">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="63a5f-140">REG\_SZ</span></span><br/>    | <span data-ttu-id="63a5f-141">0x20</span><span class="sxs-lookup"><span data-stu-id="63a5f-141">0x20</span></span><br/> | <span data-ttu-id="63a5f-142">父系的協助工具值</span><span class="sxs-lookup"><span data-stu-id="63a5f-142">Accessibility value of parent</span></span><br/>                    |
| <span data-ttu-id="63a5f-143">ParentRole</span><span class="sxs-lookup"><span data-stu-id="63a5f-143">ParentRole</span></span><br/>        | <span data-ttu-id="63a5f-144">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="63a5f-144">REG\_DWORD</span></span><br/> | <span data-ttu-id="63a5f-145">0x40</span><span class="sxs-lookup"><span data-stu-id="63a5f-145">0x40</span></span><br/> | <span data-ttu-id="63a5f-146">父系的協助工具角色</span><span class="sxs-lookup"><span data-stu-id="63a5f-146">Accessibility role of parent</span></span><br/>                     |
| <span data-ttu-id="63a5f-147">ParentDescription</span><span class="sxs-lookup"><span data-stu-id="63a5f-147">ParentDescription</span></span><br/> | <span data-ttu-id="63a5f-148">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="63a5f-148">REG\_SZ</span></span><br/>    | <span data-ttu-id="63a5f-149">0x80</span><span class="sxs-lookup"><span data-stu-id="63a5f-149">0x80</span></span><br/> | <span data-ttu-id="63a5f-150">父系的協助工具描述</span><span class="sxs-lookup"><span data-stu-id="63a5f-150">Accessibility description of parent</span></span><br/>              |



 

<span data-ttu-id="63a5f-151">此外，如果設定了遮罩位值0x1，則 URL 應該取自協助工具名稱;否則，應從存取範圍值取得 URL。</span><span class="sxs-lookup"><span data-stu-id="63a5f-151">Additionally, if the mask bit value 0x1 is set, then the URL should be taken from the accessibility name; otherwise, the URL should be taken from the accessibility value.</span></span>

<span data-ttu-id="63a5f-152">如果應用程式使用上述 REG SZ 值的當地語系化字串 \_ ，則應該使用下列格式，將字串提供為間接字串：</span><span class="sxs-lookup"><span data-stu-id="63a5f-152">If the application uses localized strings for the REG\_SZ values above, the string should be provided as an indirect string by using the following format:</span></span>

<span data-ttu-id="63a5f-153">@filename資源</span><span class="sxs-lookup"><span data-stu-id="63a5f-153">@filename,resource</span></span>

<span data-ttu-id="63a5f-154">此字串會從名為的檔案中解壓縮，並使用資源值做為定位器。</span><span class="sxs-lookup"><span data-stu-id="63a5f-154">The string is extracted from the file named, using the resource value as a locator.</span></span> <span data-ttu-id="63a5f-155">如果資源值為零或大於零，則數位會成為二進位檔案中的字串索引。</span><span class="sxs-lookup"><span data-stu-id="63a5f-155">If the resource value is zero or greater, the number becomes the index of the string in the binary file.</span></span> <span data-ttu-id="63a5f-156">如果數位為負數，則會變成 (識別碼) 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="63a5f-156">If the number is negative, it becomes a resource identifier (ID).</span></span>

> [!Note]  
> <span data-ttu-id="63a5f-157">角色常數可以在 Windows SDK 的 oleacc 中找到。</span><span class="sxs-lookup"><span data-stu-id="63a5f-157">Role constants can be found in oleacc.h in the Windows SDK.</span></span> <span data-ttu-id="63a5f-158">描述的登錄值是 Windows Vista 特有的。</span><span class="sxs-lookup"><span data-stu-id="63a5f-158">The registry values described are specific to Windows Vista.</span></span>

 

 

 




