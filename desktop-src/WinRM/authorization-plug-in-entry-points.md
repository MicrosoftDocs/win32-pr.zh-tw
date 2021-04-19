---
title: 授權外掛程式進入點
description: 授權外掛程式進入點
ms.assetid: 6cbfa79a-b57b-44b8-a421-d5e79c1b3757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ee0db76457860106e51bd6c29cead3d0f8227d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "107001085"
---
# <a name="authorization-plug-in-entry-points"></a><span data-ttu-id="1d511-103">授權外掛程式進入點</span><span class="sxs-lookup"><span data-stu-id="1d511-103">Authorization Plug-in Entry Points</span></span>

<span data-ttu-id="1d511-104">授權外掛程式僅針對 Internet Information Services (IIS) 主機進程進行設定。</span><span class="sxs-lookup"><span data-stu-id="1d511-104">Authorization plug-ins are configured only for an Internet Information Services (IIS) host process.</span></span> <span data-ttu-id="1d511-105">每個虛擬目錄只能設定一個授權外掛程式。</span><span class="sxs-lookup"><span data-stu-id="1d511-105">Only one authorization plug-in can be configured per virtual directory.</span></span>

<span data-ttu-id="1d511-106">所有授權外掛程式都必須支援下列進入點：</span><span class="sxs-lookup"><span data-stu-id="1d511-106">All authorization plug-ins must support the following entry points:</span></span>

-   [<span data-ttu-id="1d511-107">**WSManPluginStartup**</span><span class="sxs-lookup"><span data-stu-id="1d511-107">**WSManPluginStartup**</span></span>](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)
-   [<span data-ttu-id="1d511-108">**WSManPluginShutdown**</span><span class="sxs-lookup"><span data-stu-id="1d511-108">**WSManPluginShutdown**</span></span>](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)
-   [<span data-ttu-id="1d511-109">**WSManPluginAuthzUser**</span><span class="sxs-lookup"><span data-stu-id="1d511-109">**WSManPluginAuthzUser**</span></span>](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)
-   [<span data-ttu-id="1d511-110">**WSManPluginAuthzOperation**</span><span class="sxs-lookup"><span data-stu-id="1d511-110">**WSManPluginAuthzOperation**</span></span>](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)

<span data-ttu-id="1d511-111">以下是選擇性的進入點：</span><span class="sxs-lookup"><span data-stu-id="1d511-111">The following entry point is optional:</span></span>

-   [<span data-ttu-id="1d511-112">**WSManPluginAuthzQueryQuota**</span><span class="sxs-lookup"><span data-stu-id="1d511-112">**WSManPluginAuthzQueryQuota**</span></span>](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota)

<span data-ttu-id="1d511-113">下表概要說明 Windows 遠端管理 (WinRM) 外掛程式 API 中的授權外掛程式進入點。</span><span class="sxs-lookup"><span data-stu-id="1d511-113">The following table provides an overview of the authorization plug-in entry points in the Windows Remote Management (WinRM) Plug-in API.</span></span>



| <span data-ttu-id="1d511-114">函式</span><span class="sxs-lookup"><span data-stu-id="1d511-114">Function</span></span>                                                                                      | <span data-ttu-id="1d511-115">描述</span><span class="sxs-lookup"><span data-stu-id="1d511-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d511-116">**WSMAN \_ 外掛程式 \_ 授權 \_ 操作**</span><span class="sxs-lookup"><span data-stu-id="1d511-116">**WSMAN\_PLUGIN\_ AUTHORIZE\_OPERATION**</span></span>](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)              | <span data-ttu-id="1d511-117">呼叫以授權特定的作業。</span><span class="sxs-lookup"><span data-stu-id="1d511-117">Called to authorize a specific operation.</span></span> <br/> <span data-ttu-id="1d511-118">此方法的 DLL 進入點名稱必須是 [**WSManPluginAuthzOperation**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)。</span><span class="sxs-lookup"><span data-stu-id="1d511-118">The DLL entry point name for this method must be [**WSManPluginAuthzOperation**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation).</span></span><br/>                                                                                                                                                                                                       |
| [<span data-ttu-id="1d511-119">**WSMAN \_ 外掛程式 \_ 授權 \_ 查詢 \_ 配額**</span><span class="sxs-lookup"><span data-stu-id="1d511-119">**WSMAN\_PLUGIN\_ AUTHORIZE\_QUERY\_QUOTA**</span></span>](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)           | <span data-ttu-id="1d511-120">在授權連接取得使用者的配額資訊之後呼叫。</span><span class="sxs-lookup"><span data-stu-id="1d511-120">Called after a connection has been authorized to retrieve quota information for the user.</span></span> <br/> <span data-ttu-id="1d511-121">此方法的 DLL 進入點名稱必須是 [**WSManPluginAuthzQueryQuota**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota)。</span><span class="sxs-lookup"><span data-stu-id="1d511-121">The DLL entry point name for this method must be [**WSManPluginAuthzQueryQuota**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota).</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="1d511-122">**WSMAN \_ 外掛程式 \_ 授權 \_ 發行 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="1d511-122">**WSMAN\_PLUGIN\_ AUTHORIZE\_RELEASE\_CONTEXT**</span></span>](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context) | <span data-ttu-id="1d511-123">呼叫以釋放外掛程式在 [**WSManPluginAuthzUserComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete) 或 [**WSManPluginAuthzOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete) 方法中報告的內容。</span><span class="sxs-lookup"><span data-stu-id="1d511-123">Called to release the context that a plug-in reports from either the [**WSManPluginAuthzUserComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete) or [**WSManPluginAuthzOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete) methods.</span></span> <br/> <span data-ttu-id="1d511-124">此方法的 DLL 進入點名稱必須是 [**WSManPluginAuthzReleaseCoNtext**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context)。</span><span class="sxs-lookup"><span data-stu-id="1d511-124">The DLL entry point name for this method must be [**WSManPluginAuthzReleaseContext**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context).</span></span><br/> |
| [<span data-ttu-id="1d511-125">**WSMAN \_ 外掛程式 \_ 授權 \_ 使用者**</span><span class="sxs-lookup"><span data-stu-id="1d511-125">**WSMAN\_PLUGIN\_AUTHORIZE\_USER**</span></span>](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)                         | <span data-ttu-id="1d511-126">呼叫以判斷是否允許使用者執行要求。</span><span class="sxs-lookup"><span data-stu-id="1d511-126">Called to determine whether the user is allowed to carry out a request.</span></span> <br/> <span data-ttu-id="1d511-127">此方法的動態連結程式庫 (DLL) 進入點名稱必須是 [**WSManPluginAuthzUser**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)。</span><span class="sxs-lookup"><span data-stu-id="1d511-127">The dynamic-link library (DLL) entry point name for this method must be [**WSManPluginAuthzUser**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user).</span></span><br/>                                                                                                                                                            |



 

 

