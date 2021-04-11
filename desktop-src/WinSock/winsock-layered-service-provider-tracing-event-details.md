---
description: Winsock 目錄變更追蹤詳細資料
ms.assetid: 4C86618D-4E79-486E-997F-9E2509FBF6B6
title: Winsock 目錄變更追蹤詳細資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6258ca87d5d1fba2de9364e5524110bb43c76513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114288"
---
# <a name="winsock-catalog-change-tracing-details"></a><span data-ttu-id="9fd9d-103">Winsock 目錄變更追蹤詳細資料</span><span class="sxs-lookup"><span data-stu-id="9fd9d-103">Winsock Catalog Change Tracing Details</span></span>

> [!Note]  
> <span data-ttu-id="9fd9d-104">已淘汰分層服務提供者。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="9fd9d-105">從 Windows 8 和 Windows Server 2012 開始，請使用 [Windows 篩選平台](../fwp/windows-filtering-platform-start-page.md)。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="9fd9d-106">適用于多層式服務提供者 (Lsp) 的 Winsock 目錄變更事件追蹤，與 LSP 安裝、LSP 移除、LSP 停用和 Winsock 類別目錄重設作業有關。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-106">Winsock Catalog Change event tracing for layered Service providers (LSPs) is related to LSP installation, LSP removal, LSP disable, and Winsock catalog reset operations.</span></span> <span data-ttu-id="9fd9d-107">下列所有事件都會寫入至 *Microsoft windows-Winsock-WS2HELP/Operational* 通道，這與記錄在 Windows Vista 和更新版本上的其他 Winsock 網路事件追蹤不同。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-107">All of the following events are written to the *Microsoft-Windows-Winsock-WS2HELP/Operational* channel which is different from the other Winsock network event tracing logged on Windows Vista and later.</span></span>

<span data-ttu-id="9fd9d-108">以下將詳細說明每個可追蹤的 Winsock LSP 事件，以及描述所記錄的參數和資訊。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-108">The following details each of the Winsock LSP events that can be traced and describes which parameters and information are logged.</span></span>

## <a name="lsp-install"></a><span data-ttu-id="9fd9d-109">LSP 安裝</span><span class="sxs-lookup"><span data-stu-id="9fd9d-109">LSP Install</span></span>

<span data-ttu-id="9fd9d-110">事件識別碼 = 1</span><span class="sxs-lookup"><span data-stu-id="9fd9d-110">Event ID = 1</span></span>

<span data-ttu-id="9fd9d-111">層級 = 4 (資訊) </span><span class="sxs-lookup"><span data-stu-id="9fd9d-111">Level = 4 (Information)</span></span>

<span data-ttu-id="9fd9d-112">針對 LSP 安裝作業，會追蹤下列 Winsock LSP 事件：</span><span class="sxs-lookup"><span data-stu-id="9fd9d-112">The following Winsock LSP events are traced for an LSP install operation:</span></span>

-   <span data-ttu-id="9fd9d-113">通訊協定專案會安裝到 Winsock 目錄。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-113">A protocol entry is installed into the Winsock catalog.</span></span>

<span data-ttu-id="9fd9d-114">系統會針對 LSP 安裝事件記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="9fd9d-114">The following parameters are logged for a LSP install event:</span></span>



| <span data-ttu-id="9fd9d-115">參數</span><span class="sxs-lookup"><span data-stu-id="9fd9d-115">Parameter</span></span>                                                                                                | <span data-ttu-id="9fd9d-116">Description</span><span class="sxs-lookup"><span data-stu-id="9fd9d-116">Description</span></span>                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd9d-117"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP 名稱</span><span class="sxs-lookup"><span data-stu-id="9fd9d-117"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP Name</span></span><br/>     | <span data-ttu-id="9fd9d-118">從所安裝的 LSP 之 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **SZPROTOCOL** 成員取得的 LSP 名稱。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-118">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span><br/> |
| <span data-ttu-id="9fd9d-119"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>目錄</span><span class="sxs-lookup"><span data-stu-id="9fd9d-119"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/>         | <span data-ttu-id="9fd9d-120">Winsock 目錄 (32 位或64位) 安裝 LSP 的位置。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-120">The Winsock catalog (32-bit or 64-bit) where the LSP is being installed.</span></span> <span data-ttu-id="9fd9d-121">這是一個整數值，也就是32或64。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-121">This is an integer value that is either 32 or 64.</span></span><br/>                                   |
| <span data-ttu-id="9fd9d-122"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>安裝</span><span class="sxs-lookup"><span data-stu-id="9fd9d-122"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer</span></span><br/> | <span data-ttu-id="9fd9d-123">讓 LSP 安裝呼叫的應用程式模組檔案名。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-123">The module filename of the application making the LSP install call.</span></span><br/>                                                                                          |
| <span data-ttu-id="9fd9d-124"><span id="GUID"></span><span id="guid"></span>Guid</span><span class="sxs-lookup"><span data-stu-id="9fd9d-124"><span id="GUID"></span><span id="guid"></span>GUID</span></span><br/>                                            | <span data-ttu-id="9fd9d-125">要在其中安裝 LSP 之 Winsock 傳輸提供者的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-125">The GUID value of the Winsock transport provider that the LSP is being installed under.</span></span><br/>                                                                      |
| <span data-ttu-id="9fd9d-126"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>類別</span><span class="sxs-lookup"><span data-stu-id="9fd9d-126"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span><br/>     | <span data-ttu-id="9fd9d-127">要安裝的 LSP 之 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **dwCatalogEntryId** 成員。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-127">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span><br/>                                |



 

## <a name="lsp-uninstall"></a><span data-ttu-id="9fd9d-128">LSP 卸載</span><span class="sxs-lookup"><span data-stu-id="9fd9d-128">LSP Uninstall</span></span>

<span data-ttu-id="9fd9d-129">事件識別碼 = 2</span><span class="sxs-lookup"><span data-stu-id="9fd9d-129">Event ID = 2</span></span>

<span data-ttu-id="9fd9d-130">層級 = 4 (資訊) </span><span class="sxs-lookup"><span data-stu-id="9fd9d-130">Level = 4 (Information)</span></span>

<span data-ttu-id="9fd9d-131">針對 LSP 卸載作業，會追蹤下列 Winsock LSP 事件：</span><span class="sxs-lookup"><span data-stu-id="9fd9d-131">The following Winsock LSP events are traced for an LSP uninstall operation:</span></span>

-   <span data-ttu-id="9fd9d-132">從 Winsock 目錄移除通訊協定專案。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-132">A protocol entry is removed from the Winsock catalog.</span></span>

<span data-ttu-id="9fd9d-133">系統會針對 LSP 卸載事件記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="9fd9d-133">The following parameters are logged for a LSP uninstall event:</span></span>



| <span data-ttu-id="9fd9d-134">參數</span><span class="sxs-lookup"><span data-stu-id="9fd9d-134">Parameter</span></span>                                                                                                | <span data-ttu-id="9fd9d-135">Description</span><span class="sxs-lookup"><span data-stu-id="9fd9d-135">Description</span></span>                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd9d-136"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP 名稱</span><span class="sxs-lookup"><span data-stu-id="9fd9d-136"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP Name</span></span><br/>     | <span data-ttu-id="9fd9d-137">從要移除的 LSP 之 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **SZPROTOCOL** 成員取得的 LSP 名稱。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-137">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span><br/> |
| <span data-ttu-id="9fd9d-138"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>目錄</span><span class="sxs-lookup"><span data-stu-id="9fd9d-138"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/>         | <span data-ttu-id="9fd9d-139">Winsock 目錄 (32 位或64位) ，其中 LSP 正在移除。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-139">The Winsock catalog (32-bit or 64-bit) where the LSP is being removed.</span></span> <span data-ttu-id="9fd9d-140">這是一個整數值，也就是32或64。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-140">This is an integer value that is either 32 or 64.</span></span><br/>                                   |
| <span data-ttu-id="9fd9d-141"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>安裝</span><span class="sxs-lookup"><span data-stu-id="9fd9d-141"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer</span></span><br/> | <span data-ttu-id="9fd9d-142">讓 LSP 移除呼叫的應用程式模組檔案名。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-142">The module filename of the application making the LSP remove call.</span></span><br/>                                                                                         |
| <span data-ttu-id="9fd9d-143"><span id="GUID"></span><span id="guid"></span>Guid</span><span class="sxs-lookup"><span data-stu-id="9fd9d-143"><span id="GUID"></span><span id="guid"></span>GUID</span></span><br/>                                            | <span data-ttu-id="9fd9d-144">將 LSP 移除的 Winsock 傳輸提供者的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-144">The GUID value of the Winsock transport provider that the LSP is removed from.</span></span><br/>                                                                             |
| <span data-ttu-id="9fd9d-145"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>類別</span><span class="sxs-lookup"><span data-stu-id="9fd9d-145"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span><br/>     | <span data-ttu-id="9fd9d-146">要移除的 LSP 之 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **dwCatalogEntryId** 成員。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-146">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span><br/>                                |



 

## <a name="lsp-disable"></a><span data-ttu-id="9fd9d-147">LSP 停用</span><span class="sxs-lookup"><span data-stu-id="9fd9d-147">LSP Disable</span></span>

<span data-ttu-id="9fd9d-148">事件識別碼 = 3</span><span class="sxs-lookup"><span data-stu-id="9fd9d-148">Event ID = 3</span></span>

<span data-ttu-id="9fd9d-149">層級 = 4 (資訊) </span><span class="sxs-lookup"><span data-stu-id="9fd9d-149">Level = 4 (Information)</span></span>

<span data-ttu-id="9fd9d-150">針對 LSP 停用作業，會追蹤下列 Winsock LSP 事件：</span><span class="sxs-lookup"><span data-stu-id="9fd9d-150">The following Winsock LSP events are traced for an LSP disable operation:</span></span>

-   <span data-ttu-id="9fd9d-151">Winsock 目錄中的通訊協定專案已停用。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-151">A protocol entry is disabled in the Winsock catalog.</span></span>

<span data-ttu-id="9fd9d-152">針對 LSP 停用事件，會記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="9fd9d-152">The following parameters are logged for a LSP disable event:</span></span>



| <span data-ttu-id="9fd9d-153">參數</span><span class="sxs-lookup"><span data-stu-id="9fd9d-153">Parameter</span></span>                                                                                                | <span data-ttu-id="9fd9d-154">Description</span><span class="sxs-lookup"><span data-stu-id="9fd9d-154">Description</span></span>                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd9d-155"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP 名稱</span><span class="sxs-lookup"><span data-stu-id="9fd9d-155"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP Name</span></span><br/>     | <span data-ttu-id="9fd9d-156">針對正在停用的 LSP，從 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **SZPROTOCOL** 成員取得的 LSP 名稱。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-156">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span><br/> |
| <span data-ttu-id="9fd9d-157"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>目錄</span><span class="sxs-lookup"><span data-stu-id="9fd9d-157"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/>         | <span data-ttu-id="9fd9d-158">Winsock 目錄 (32 位或64位) 在 LSP 正在停用的位置。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-158">The Winsock catalog (32-bit or 64-bit) where the LSP is being disabled.</span></span> <span data-ttu-id="9fd9d-159">這是一個整數值，也就是32或64。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-159">This is an integer value that is either 32 or 64.</span></span><br/>                                   |
| <span data-ttu-id="9fd9d-160"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>安裝</span><span class="sxs-lookup"><span data-stu-id="9fd9d-160"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer</span></span><br/> | <span data-ttu-id="9fd9d-161">讓 LSP 停用呼叫的應用程式模組檔案名。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-161">The module filename of the application making the LSP disable call.</span></span><br/>                                                                                         |
| <span data-ttu-id="9fd9d-162"><span id="GUID"></span><span id="guid"></span>Guid</span><span class="sxs-lookup"><span data-stu-id="9fd9d-162"><span id="GUID"></span><span id="guid"></span>GUID</span></span><br/>                                            | <span data-ttu-id="9fd9d-163">要停用 LSP 之 Winsock 傳輸提供者的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-163">The GUID value of the Winsock transport provider where the LSP is being disabled.</span></span><br/>                                                                           |
| <span data-ttu-id="9fd9d-164"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>類別</span><span class="sxs-lookup"><span data-stu-id="9fd9d-164"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span><br/>     | <span data-ttu-id="9fd9d-165">正在停用的 LSP 之 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **dwCatalogEntryId** 成員。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-165">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span><br/>                                |



 

## <a name="winsock-catalog-reset"></a><span data-ttu-id="9fd9d-166">Winsock 目錄重設</span><span class="sxs-lookup"><span data-stu-id="9fd9d-166">Winsock Catalog Reset</span></span>

<span data-ttu-id="9fd9d-167">事件識別碼 = 4</span><span class="sxs-lookup"><span data-stu-id="9fd9d-167">Event ID = 4</span></span>

<span data-ttu-id="9fd9d-168">層級 = 4 (資訊) </span><span class="sxs-lookup"><span data-stu-id="9fd9d-168">Level = 4 (Information)</span></span>

<span data-ttu-id="9fd9d-169">Winsock 類別目錄重設作業會追蹤下列 Winsock LSP 事件：</span><span class="sxs-lookup"><span data-stu-id="9fd9d-169">The following Winsock LSP events are traced for a Winsock catalog reset operation:</span></span>

-   <span data-ttu-id="9fd9d-170">Winsock 類別目錄已重設。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-170">The Winsock catalog is reset.</span></span>

<span data-ttu-id="9fd9d-171">Winsock 類別目錄重設事件會記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="9fd9d-171">The following parameters are logged for a Winsock catalog reset event:</span></span>



| <span data-ttu-id="9fd9d-172">參數</span><span class="sxs-lookup"><span data-stu-id="9fd9d-172">Parameter</span></span>                                                                                        | <span data-ttu-id="9fd9d-173">Description</span><span class="sxs-lookup"><span data-stu-id="9fd9d-173">Description</span></span>                                                                                                              |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd9d-174"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>目錄</span><span class="sxs-lookup"><span data-stu-id="9fd9d-174"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/> | <span data-ttu-id="9fd9d-175">要重設的 (32 位或64位) 的 Winsock 目錄。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-175">The Winsock catalog (32-bit or 64-bit) that is being reset.</span></span> <span data-ttu-id="9fd9d-176">這是一個整數值，也就是32或64。</span><span class="sxs-lookup"><span data-stu-id="9fd9d-176">This is an integer value that is either 32 or 64.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="9fd9d-177">相關主題</span><span class="sxs-lookup"><span data-stu-id="9fd9d-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fd9d-178">Winsock 追蹤的控制權</span><span class="sxs-lookup"><span data-stu-id="9fd9d-178">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="9fd9d-179">Winsock 追蹤</span><span class="sxs-lookup"><span data-stu-id="9fd9d-179">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="9fd9d-180">Winsock 追蹤層級</span><span class="sxs-lookup"><span data-stu-id="9fd9d-180">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="9fd9d-181">Winsock 網路事件追蹤詳細資料</span><span class="sxs-lookup"><span data-stu-id="9fd9d-181">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> </dl>

 

 
