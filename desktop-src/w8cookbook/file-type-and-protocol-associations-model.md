---
title: 檔案類型和 URI 關聯模型
description: 檔案類型和 URI 關聯模型
ms.assetid: 4DE7DD08-088A-4E09-B1C7-AE9033EA533D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c78540a072405aade01a9f94503999ad105d2078
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104024230"
---
# <a name="file-type-and-uri-associations-model"></a><span data-ttu-id="83b47-103">檔案類型和 URI 關聯模型</span><span class="sxs-lookup"><span data-stu-id="83b47-103">File type and URI associations model</span></span>

## <a name="platforms"></a><span data-ttu-id="83b47-104">平台</span><span class="sxs-lookup"><span data-stu-id="83b47-104">Platforms</span></span>

 <span data-ttu-id="83b47-105">**客戶** 端-Windows 8</span><span class="sxs-lookup"><span data-stu-id="83b47-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="83b47-106">**伺服器** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="83b47-106">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="83b47-107">Description</span><span class="sxs-lookup"><span data-stu-id="83b47-107">Description</span></span>

<span data-ttu-id="83b47-108">Windows 8 中的檔案類型和 URI 關聯模型已變更。</span><span class="sxs-lookup"><span data-stu-id="83b47-108">The file type and URI association model has changed in Windows 8.</span></span> <span data-ttu-id="83b47-109">應用程式無法再以程式設計的方式將自己設定為檔案類型或 URI 的預設處理常式。</span><span class="sxs-lookup"><span data-stu-id="83b47-109">Apps are no longer able to programmatically set themselves as the default handler for a file type or URI.</span></span> <span data-ttu-id="83b47-110">相反地，使用者現在一律會控制檔案類型或 URI 配置的預設處理常式。</span><span class="sxs-lookup"><span data-stu-id="83b47-110">Instead, now the user always controls what the default handler is for a file type or URI scheme.</span></span>

## <a name="manifestation"></a><span data-ttu-id="83b47-111">表現</span><span class="sxs-lookup"><span data-stu-id="83b47-111">Manifestation</span></span>

<span data-ttu-id="83b47-112">這項變更對使用者的呈現方式取決於應用程式的設計方式，例如：</span><span class="sxs-lookup"><span data-stu-id="83b47-112">How this change presents to the user depends upon how the app is designed, for example:</span></span>

-   <span data-ttu-id="83b47-113">許多應用程式會在每次執行時查看它們是否為預設值，如果不是，則會提示使用者將其設定為預設值。</span><span class="sxs-lookup"><span data-stu-id="83b47-113">Many apps check to see if they are the default every time they run and, if they are not, they prompt the user to set them as default.</span></span> <span data-ttu-id="83b47-114">不過，因為應用程式無法再精確地查詢，以判斷哪一個應用程式是檔案類型或 URI 配置的預設處理常式，所以這些作業都無法運作。</span><span class="sxs-lookup"><span data-stu-id="83b47-114">However, because apps can no longer accurately query to determine which app is the default handler for a file type or URI scheme, neither of these operations works.</span></span>
-   <span data-ttu-id="83b47-115">許多應用程式都有內建的對話方塊或功能表，或在其安裝程式中，指定應用程式應作為預設值的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="83b47-115">Many apps have a dialog box or menu built in or in their installer that specifies the file types for which the app should serve as the default.</span></span> <span data-ttu-id="83b47-116">不過，因為應用程式無法再以程式設計的方式，將本身設定為檔案類型或 URI 配置的預設處理常式，所以無法再運作。</span><span class="sxs-lookup"><span data-stu-id="83b47-116">However, because apps can no longer programmatically set themselves as the default handler for a file type or URI scheme, this no longer works.</span></span>

## <a name="mitigation"></a><span data-ttu-id="83b47-117">降低</span><span class="sxs-lookup"><span data-stu-id="83b47-117">Mitigation</span></span>

<span data-ttu-id="83b47-118">使用者可以執行幾項工作來容納這些變更：</span><span class="sxs-lookup"><span data-stu-id="83b47-118">There are several things users can do to accommodate these changes:</span></span>

-   <span data-ttu-id="83b47-119">系統會提示使用者內容選擇預設的應用程式來處理檔案類型、URI 配置，或兩者都未指定時</span><span class="sxs-lookup"><span data-stu-id="83b47-119">Users are prompted contextually to choose a default app to handle file types, URI schemes, or both when one has not been specified</span></span>
-   <span data-ttu-id="83b47-120">使用者可以選擇在安裝可處理檔案類型或 URI 配置的新應用程式之後，變更其預設處理常式。</span><span class="sxs-lookup"><span data-stu-id="83b47-120">Users are offered the option to change their default handler after installing new apps that can handle a file type or URI scheme</span></span>
-   <span data-ttu-id="83b47-121">[預設程式] 控制台可讓使用者設定應用程式的預設值，或為檔案類型、URI 配置或兩者設定：應用程式可以連結至 [控制台]</span><span class="sxs-lookup"><span data-stu-id="83b47-121">The default programs control panel allows users to set defaults for an app, or for a file type, URI scheme, or both; apps can link to the control panel</span></span>
-   <span data-ttu-id="83b47-122">您可以從 Windows 檔案總管變更預設值</span><span class="sxs-lookup"><span data-stu-id="83b47-122">Defaults can be changed from Windows Explorer</span></span>

## <a name="solution"></a><span data-ttu-id="83b47-123">解決方法</span><span class="sxs-lookup"><span data-stu-id="83b47-123">Solution</span></span>

<span data-ttu-id="83b47-124">由於這些變更，我們提供了此 API 指引：</span><span class="sxs-lookup"><span data-stu-id="83b47-124">As a result of these changes, this API guidance is provided:</span></span>

-   <span data-ttu-id="83b47-125">[IApplicationAssociationRegistration](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) API 內某些方法呼叫的功能已變更，因此不應再使用。</span><span class="sxs-lookup"><span data-stu-id="83b47-125">The functionality of some method calls within the [IApplicationAssociationRegistration](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) API has changed, and should no longer be used.</span></span>

    -   <span data-ttu-id="83b47-126">**請勿** 呼叫 [QueryAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) / [QueryAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall)判斷應用程式是否為預設值</span><span class="sxs-lookup"><span data-stu-id="83b47-126">**Do not** call [QueryAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault)/[QueryAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall) to determine if an app is the default</span></span>
    -   <span data-ttu-id="83b47-127">如果有任何) 是目前預設值，**請勿** 呼叫 [QueryCurrentDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault)來判斷哪個應用程式 (</span><span class="sxs-lookup"><span data-stu-id="83b47-127">**Do not** call [QueryCurrentDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault) to determine which app (if any) is the current default</span></span>
    -   <span data-ttu-id="83b47-128">**請勿** 呼叫 [SetAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault) / [SetAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall)來設定預設應用程式</span><span class="sxs-lookup"><span data-stu-id="83b47-128">**Do not** call [SetAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault)/[SetAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall) to set the default app</span></span>

-   <span data-ttu-id="83b47-129">接下來的指引是：</span><span class="sxs-lookup"><span data-stu-id="83b47-129">The guidance going forward is:</span></span>

    -   <span data-ttu-id="83b47-130">**請勿** 查詢以查看哪一個應用程式是檔案類型或 URI 配置的預設處理常式</span><span class="sxs-lookup"><span data-stu-id="83b47-130">**Do not** query to see which app is the default handler for file types or URI schemes</span></span>

    -   <span data-ttu-id="83b47-131">**請勿** 嘗試監視檔案類型或 URI 配置的預設處理常式中的變更</span><span class="sxs-lookup"><span data-stu-id="83b47-131">**Do not** attempt to monitor changes in the default handler for file types or URI schemes</span></span>

    -   <span data-ttu-id="83b47-132">**請勿** 嘗試將應用程式設定為檔案類型或 URI 配置的預設處理常式</span><span class="sxs-lookup"><span data-stu-id="83b47-132">**Do not** attempt to set an app as the default handler for file types or URI schemes</span></span>

    -   <span data-ttu-id="83b47-133">**請勿** 嘗試從應用程式內管理檔案類型或 URI 配置的預設值</span><span class="sxs-lookup"><span data-stu-id="83b47-133">**Do not** attempt to manage defaults for file types or URI schemes from within an app</span></span>

    -   <span data-ttu-id="83b47-134">如果您想要允許您應用程式的使用者存取預設管理 UI (應用程式內的管理 UI 已不再支援，**請** 與 [[設定預設程式](../shell/default-programs.md)] 控制台整合) </span><span class="sxs-lookup"><span data-stu-id="83b47-134">**Do** integrate with the [Set Default Programs](../shell/default-programs.md) control panel if you want to allow users of your app to access the default management UI (the management UI within the app is no longer supported)</span></span>

        -   <span data-ttu-id="83b47-135">呼叫 [IApplicationAssociationRegistrationUI：： LaunchAdvancedAssociationUI](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) 可讓使用者存取指定應用程式的 [[設定預設程式](../shell/default-programs.md)] 控制台頁面</span><span class="sxs-lookup"><span data-stu-id="83b47-135">Calling [IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) allows the user to access the ‘[Set Default Programs](../shell/default-programs.md)’ control panel page for the specified app</span></span>

## <a name="tests"></a><span data-ttu-id="83b47-136">測試</span><span class="sxs-lookup"><span data-stu-id="83b47-136">Tests</span></span>

-   <span data-ttu-id="83b47-137">測試以確認應用程式在 [設定預設程式] 控制台中正確註冊</span><span class="sxs-lookup"><span data-stu-id="83b47-137">Test to verify that apps register properly in Set Default Programs control panel</span></span>
-   <span data-ttu-id="83b47-138">測試以確認應用程式正確註冊，以顯示在其所註冊要處理的檔案類型、URI 配置或兩者的 OpenWith 清單中</span><span class="sxs-lookup"><span data-stu-id="83b47-138">Test to verify that apps register properly to appear in the OpenWith list for the file types, URI schemes, or both, that they register to handle</span></span>
-   <span data-ttu-id="83b47-139">測試以確認應用程式已安裝，且使用者叫用您的應用程式已註冊要處理的檔案類型、URI 配置或兩者時，出現新的代理程式更新</span><span class="sxs-lookup"><span data-stu-id="83b47-139">Test to verify that new app notifications appear after your app is installed and the user invokes a file type, URI scheme, or both, that your app has registered to handle</span></span>

## <a name="resources"></a><span data-ttu-id="83b47-140">資源</span><span class="sxs-lookup"><span data-stu-id="83b47-140">Resources</span></span>

-   <span data-ttu-id="83b47-141">[Windows 8 Desktop 應用程式中檔案類型和 URI 關聯的最佳作法](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="83b47-141">[Best Practices for File Type and URI Associations in Windows 8 Desktop Apps](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))</span></span>
-   [<span data-ttu-id="83b47-142">檔案類型關聯和自動播放組建會議簡報</span><span class="sxs-lookup"><span data-stu-id="83b47-142">File Type Associations and AutoPlay Build Conference Presentation</span></span>](https://channel9.msdn.com/events/BUILD/BUILD2011/PLAT-282T)

 

 