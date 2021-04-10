---
title: 用於顯示規範的內容功能表
description: Active Directory 系統管理 MMC 嵌入式管理單元和 Windows 2000 shell 提供一種機制，可將專案新增至 Active Directory Domain Services 中物件所顯示的內容功能表。
ms.assetid: 0b0691f5-321d-4f22-b39c-bc528db9e707
ms.tgt_platform: multiple
keywords:
- 顯示規範廣告，內容功能表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f28fbf703f17ea5c0fa7938365d485998be77e8d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933083"
---
# <a name="context-menus-for-use-with-display-specifiers"></a><span data-ttu-id="cafde-104">用於顯示規範的內容功能表</span><span class="sxs-lookup"><span data-stu-id="cafde-104">Context Menus for Use with Display Specifiers</span></span>

<span data-ttu-id="cafde-105">Active Directory 系統管理 MMC 嵌入式管理單元和 Windows 2000 shell 提供一種機制，可將專案新增至 Active Directory Domain Services 中物件所顯示的內容功能表。</span><span class="sxs-lookup"><span data-stu-id="cafde-105">The Active Directory administrative MMC snap-ins and Windows 2000 shell provide a mechanism to add an item to the context menu displayed for objects in Active Directory Domain Services.</span></span> <span data-ttu-id="cafde-106">您可以藉由實作為 *內容功能表延伸* 的 COM 內部進程伺服器來加入內容功能表項目。</span><span class="sxs-lookup"><span data-stu-id="cafde-106">A context menu item can be added by implementing an COM in-proc server known as a *context menu extension*.</span></span> <span data-ttu-id="cafde-107">您也可以新增操作功能表項目，以叫用任何以 [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) API 啟動的檔案，例如應用程式或網頁 URL。</span><span class="sxs-lookup"><span data-stu-id="cafde-107">A context menu item can also be added that invokes any file started with the [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) API, such as an application or webpage URL.</span></span> <span data-ttu-id="cafde-108">這就是所謂的 *靜態內容功能表項目*。</span><span class="sxs-lookup"><span data-stu-id="cafde-108">This is known as a *static context menu item*.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="cafde-109">開發人員讀者</span><span class="sxs-lookup"><span data-stu-id="cafde-109">Developer Audience</span></span>

<span data-ttu-id="cafde-110">本檔假設讀者已熟悉使用 c + + 的 COM 作業和元件開發。</span><span class="sxs-lookup"><span data-stu-id="cafde-110">This documentation assumes that the reader is familiar with COM operation and component development using C++.</span></span> <span data-ttu-id="cafde-111">目前無法使用 Microsoft Visual Basic 來建立 Active Directory Domain Services 內容功能表延伸模組。</span><span class="sxs-lookup"><span data-stu-id="cafde-111">It is not currently possible to create an Active Directory Domain Services context menu extension using Microsoft Visual Basic.</span></span>

## <a name="extending-the-context-menu-with-a-context-menu-extension"></a><span data-ttu-id="cafde-112">使用內容功能表延伸模組擴充內容功能表</span><span class="sxs-lookup"><span data-stu-id="cafde-112">Extending the Context Menu With a Context Menu Extension</span></span>

<span data-ttu-id="cafde-113">內容功能表延伸模組是一種 COM 內伺服器，會執行特定的介面並向 Active Directory Domain Services 註冊。</span><span class="sxs-lookup"><span data-stu-id="cafde-113">A context menu extension is a COM in-proc server that implements certain interfaces and is registered with Active Directory Domain Services.</span></span>

<span data-ttu-id="cafde-114">**建立和安裝內容功能表延伸模組**</span><span class="sxs-lookup"><span data-stu-id="cafde-114">**To create and install a context menu extension**</span></span>

1.  <span data-ttu-id="cafde-115">建立內容功能表延伸模組 DLL。</span><span class="sxs-lookup"><span data-stu-id="cafde-115">Create the context menu extension DLL.</span></span> <span data-ttu-id="cafde-116">內容功能表延伸是 COM 的內部伺服器伺服器，至少會執行 [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) 和 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) 介面。</span><span class="sxs-lookup"><span data-stu-id="cafde-116">A context menu extension is a COM in-proc server that, at a minimum, implements the [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) and [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interfaces.</span></span> <span data-ttu-id="cafde-117">如需詳細資訊，請參閱 [執行內容功能表 COM 物件](implementing-the-context-menu-com-object.md)。</span><span class="sxs-lookup"><span data-stu-id="cafde-117">For more information, see [Implementing the Context Menu COM Object](implementing-the-context-menu-com-object.md).</span></span>
2.  <span data-ttu-id="cafde-118">在使用內容功能表延伸的電腦上安裝內容功能表表擴充功能。</span><span class="sxs-lookup"><span data-stu-id="cafde-118">Install the context menu sheet extension on computers where the context menu extension is used.</span></span> <span data-ttu-id="cafde-119">您可以建立內容功能表延伸模組 DLL 的 Microsoft Windows Installer 套件，並使用群組原則適當地部署封裝，以達成此目的。</span><span class="sxs-lookup"><span data-stu-id="cafde-119">This is accomplished by creating a Microsoft Windows Installer package for the context menu extension DLL and deploying the package appropriately using the group policy.</span></span> <span data-ttu-id="cafde-120">如需詳細資訊，請參閱散發 [消費者介面元件](distributing-user-interface-components.md)。</span><span class="sxs-lookup"><span data-stu-id="cafde-120">For more information, see [Distributing User Interface Components](distributing-user-interface-components.md).</span></span>
3.  <span data-ttu-id="cafde-121">在 Windows 登錄和 Active Directory Domain Services 中註冊內容功能表延伸模組。</span><span class="sxs-lookup"><span data-stu-id="cafde-121">Register the context menu extension in the Windows registry and with Active Directory Domain Services.</span></span> <span data-ttu-id="cafde-122">如需詳細資訊，請參閱 [在顯示規範中註冊內容功能表 COM 物件](registering-the-context-menu-com-object-in-a-display-specifier.md)。</span><span class="sxs-lookup"><span data-stu-id="cafde-122">For more information, see [Registering the Context Menu COM Object in a Display Specifier](registering-the-context-menu-com-object-in-a-display-specifier.md).</span></span>

## <a name="extending-the-context-menu-with-a-static-context-menu-item"></a><span data-ttu-id="cafde-123">使用靜態內容功能表項目擴充內容功能表</span><span class="sxs-lookup"><span data-stu-id="cafde-123">Extending the Context Menu With a Static Context Menu Item</span></span>

<span data-ttu-id="cafde-124">靜態內容功能表項目可用來叫用任何以 [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) API 啟動的檔案，例如應用程式或網頁 URL。</span><span class="sxs-lookup"><span data-stu-id="cafde-124">A static context menu item can be used to invoke any file started with the [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) API, such as an application or webpage URL.</span></span> <span data-ttu-id="cafde-125">若要完成這項作業，必須註冊特定物件類別的靜態內容功能表項目，以便將靜態內容功能表項目加入至該類別之物件的內容功能表。</span><span class="sxs-lookup"><span data-stu-id="cafde-125">To accomplished this, the static context menu item for a particular object class must be registered so that the static context menu item is added to the context menu of objects of that class.</span></span> <span data-ttu-id="cafde-126">如需詳細資訊，請參閱 [註冊靜態內容功能表項目](registering-a-static-context-menu-item.md)。</span><span class="sxs-lookup"><span data-stu-id="cafde-126">For more information, see [Registering a Static Context Menu Item](registering-a-static-context-menu-item.md).</span></span>

 

 