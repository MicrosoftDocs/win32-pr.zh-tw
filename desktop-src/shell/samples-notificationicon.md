---
description: 示範如何使用 Shell \_ NotifyIcon 和 shell \_ NotifyIconGetRect api 來顯示通知圖示。
title: NotificationIcon 範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9F31DB2D-4B12-4f65-AC91-25B4B5B1CB46
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1569d162aef358130910081bee80354cb64f690d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973289"
---
# <a name="notificationicon-sample"></a><span data-ttu-id="d96d5-103">NotificationIcon 範例</span><span class="sxs-lookup"><span data-stu-id="d96d5-103">NotificationIcon Sample</span></span>

<span data-ttu-id="d96d5-104">示範如何使用 [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) 和 [**shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) api 來顯示通知圖示。</span><span class="sxs-lookup"><span data-stu-id="d96d5-104">Demonstrates how to use the [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) and [**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) APIs to display a notification icon.</span></span>

<span data-ttu-id="d96d5-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="d96d5-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d96d5-106">說明</span><span class="sxs-lookup"><span data-stu-id="d96d5-106">Description</span></span>](#description)
-   [<span data-ttu-id="d96d5-107">需求</span><span class="sxs-lookup"><span data-stu-id="d96d5-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="d96d5-108">下載範例</span><span class="sxs-lookup"><span data-stu-id="d96d5-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="d96d5-109">建立範例</span><span class="sxs-lookup"><span data-stu-id="d96d5-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="d96d5-110">執行範例</span><span class="sxs-lookup"><span data-stu-id="d96d5-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="d96d5-111">Description</span><span class="sxs-lookup"><span data-stu-id="d96d5-111">Description</span></span>

<span data-ttu-id="d96d5-112">除了使用 [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) 和 [**shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) 來顯示通知圖示之外，此範例也會示範如何顯示豐富的飛出視窗、操作功能表和批註提示。</span><span class="sxs-lookup"><span data-stu-id="d96d5-112">In addition to the use of [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) and [**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) to display a notification icon, this sample also demonstrates how to display a rich flyout window, context menu, and balloon notification.</span></span>

> [!Note]  
> <span data-ttu-id="d96d5-113">[**Shell \_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) 僅適用于 Windows 7 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="d96d5-113">[**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) is only available on Windows 7 and later versions.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d96d5-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d96d5-114">Requirements</span></span>



| <span data-ttu-id="d96d5-115">產品</span><span class="sxs-lookup"><span data-stu-id="d96d5-115">Product</span></span>                                | <span data-ttu-id="d96d5-116">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="d96d5-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="d96d5-117">Windows</span><span class="sxs-lookup"><span data-stu-id="d96d5-117">Windows</span></span>                                | <span data-ttu-id="d96d5-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d96d5-118">Windows 7</span></span>               |
| <span data-ttu-id="d96d5-119">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="d96d5-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="d96d5-120">7.0</span><span class="sxs-lookup"><span data-stu-id="d96d5-120">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="d96d5-121">下載範例</span><span class="sxs-lookup"><span data-stu-id="d96d5-121">Downloading the Sample</span></span>

| <span data-ttu-id="d96d5-122">Location</span><span class="sxs-lookup"><span data-stu-id="d96d5-122">Location</span></span>      | <span data-ttu-id="d96d5-123">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="d96d5-123">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d96d5-124">GitHub</span><span class="sxs-lookup"><span data-stu-id="d96d5-124">GitHub</span></span>  | [<span data-ttu-id="d96d5-125">NotificationIcon 範例</span><span class="sxs-lookup"><span data-stu-id="d96d5-125">NotificationIcon sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NotificationIcon) |

## <a name="building-the-sample"></a><span data-ttu-id="d96d5-126">建立範例</span><span class="sxs-lookup"><span data-stu-id="d96d5-126">Building the Sample</span></span>

<span data-ttu-id="d96d5-127">若要從命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="d96d5-127">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="d96d5-128">開啟 [命令提示字元] 視窗，並流覽至 **NotificationIcon** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="d96d5-128">Open the command prompt window and navigate to the **NotificationIcon** project directory.</span></span>
2.  <span data-ttu-id="d96d5-129">輸入 `msbuild NotificationIcon.sln`。</span><span class="sxs-lookup"><span data-stu-id="d96d5-129">Enter `msbuild NotificationIcon.sln`.</span></span>

<span data-ttu-id="d96d5-130">若要使用 Microsoft Visual Studio (慣用的) 來建立範例：</span><span class="sxs-lookup"><span data-stu-id="d96d5-130">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="d96d5-131">開啟 Windows 檔案總管，然後流覽至 **NotificationIcon** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="d96d5-131">Open Windows Explorer and navigate to the **NotificationIcon** project directory.</span></span>
2.  <span data-ttu-id="d96d5-132">按兩下 NotificationIcon .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="d96d5-132">Double-click the icon for the NotificationIcon.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="d96d5-133">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="d96d5-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="d96d5-134">執行範例</span><span class="sxs-lookup"><span data-stu-id="d96d5-134">Running the Sample</span></span>

1.  <span data-ttu-id="d96d5-135">使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="d96d5-135">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="d96d5-136">在命令列中，輸入 `NotificationIcon.exe` 。</span><span class="sxs-lookup"><span data-stu-id="d96d5-136">At the command line, enter `NotificationIcon.exe`.</span></span> <span data-ttu-id="d96d5-137">或者，從 Windows 檔案總管按兩下 NotificationIcon.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="d96d5-137">Alternatively, from Windows Explorer double-click the icon for NotificationIcon.exe.</span></span>

> [!Note]  
> <span data-ttu-id="d96d5-138">以 GUID 指定的通知圖示會藉由驗證只有單一應用程式註冊來防止詐騙。</span><span class="sxs-lookup"><span data-stu-id="d96d5-138">Notification icons specified with a GUID are protected against spoofing by validating that only a single application registers them.</span></span> <span data-ttu-id="d96d5-139">這項註冊會在您第一次呼叫 Shell NotifyIcon 時執行 \_ (NIM \_ ADD，... ) ，而且會儲存呼叫應用程式的完整路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="d96d5-139">This registration is performed the first time you call Shell\_NotifyIcon(NIM\_ADD, ...) and the full path name of the calling application is stored.</span></span> <span data-ttu-id="d96d5-140">如果您稍後將二進位檔案移至不同的位置，系統將不會允許重新加入該圖示。</span><span class="sxs-lookup"><span data-stu-id="d96d5-140">If you later move your binary file to a different location, the system will not allow the icon to be added again.</span></span> <span data-ttu-id="d96d5-141">如需詳細資訊，請參閱 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) 。</span><span class="sxs-lookup"><span data-stu-id="d96d5-141">Please see [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) for more information.</span></span>

 

 

 



