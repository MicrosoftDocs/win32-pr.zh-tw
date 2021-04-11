---
description: IUpdateInstaller 介面會定義下列屬性。
ms.assetid: 876a2150-40a1-42a3-bc9a-05dec94fccd3
title: IUpdateInstaller 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77df235c49e7b6f27b0f93ec3b0c4def12135065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848129"
---
# <a name="iupdateinstaller-properties"></a><span data-ttu-id="38a82-103">IUpdateInstaller 屬性</span><span class="sxs-lookup"><span data-stu-id="38a82-103">IUpdateInstaller Properties</span></span>

<span data-ttu-id="38a82-104">[**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)介面會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="38a82-104">The [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) interface defines the following properties.</span></span>



| <span data-ttu-id="38a82-105">屬性</span><span class="sxs-lookup"><span data-stu-id="38a82-105">Property</span></span>                                                                                      | <span data-ttu-id="38a82-106">描述</span><span class="sxs-lookup"><span data-stu-id="38a82-106">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="38a82-107">**AllowSourcePrompts**</span><span class="sxs-lookup"><span data-stu-id="38a82-107">**AllowSourcePrompts**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_allowsourceprompts)                             | <span data-ttu-id="38a82-108">取得和設定布林值，這個值會指出是否要在安裝更新時，對使用者顯示來源提示。</span><span class="sxs-lookup"><span data-stu-id="38a82-108">Gets and sets a Boolean value that indicates whether to show source prompts to the user when installing the updates.</span></span>                  |
| [<span data-ttu-id="38a82-109">**ClientApplicationID**</span><span class="sxs-lookup"><span data-stu-id="38a82-109">**ClientApplicationID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_clientapplicationid)                           | <span data-ttu-id="38a82-110">取得和設定目前的用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="38a82-110">Gets and sets the current client application.</span></span>                                                                                         |
| [<span data-ttu-id="38a82-111">**System.componentmodel.backgroundworker.isbusy**</span><span class="sxs-lookup"><span data-stu-id="38a82-111">**IsBusy**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isbusy)                                                     | <span data-ttu-id="38a82-112">取得布林值，指出電腦是否在特定時間進行安裝或卸載。</span><span class="sxs-lookup"><span data-stu-id="38a82-112">Gets a Boolean value that indicates whether an installation or uninstallation is in progress on a computer at a specific time.</span></span>        |
| [<span data-ttu-id="38a82-113">**IsForced**</span><span class="sxs-lookup"><span data-stu-id="38a82-113">**IsForced**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isforced)                                                 | <span data-ttu-id="38a82-114">取得或設定布林值，指出是否強制安裝或卸載更新。</span><span class="sxs-lookup"><span data-stu-id="38a82-114">Gets or sets a Boolean value that indicates whether to forcibly install or uninstall an update.</span></span>                                       |
| [<span data-ttu-id="38a82-115">**ParentHwnd**</span><span class="sxs-lookup"><span data-stu-id="38a82-115">**ParentHwnd**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parenthwnd)                                             | <span data-ttu-id="38a82-116">取得和設定可包含對話方塊的父視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="38a82-116">Gets and sets a handle to the parent window that can contain a dialog box.</span></span>                                                            |
| [<span data-ttu-id="38a82-117">**ParentWindow**</span><span class="sxs-lookup"><span data-stu-id="38a82-117">**ParentWindow**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parentwindow)                                         | <span data-ttu-id="38a82-118">取得和設定介面，這個介面表示可以包含對話方塊的父視窗。</span><span class="sxs-lookup"><span data-stu-id="38a82-118">Gets and sets the interface that represents the parent window that can contain a dialog box.</span></span>                                          |
| [<span data-ttu-id="38a82-119">**RebootRequiredBeforeInstallation**</span><span class="sxs-lookup"><span data-stu-id="38a82-119">**RebootRequiredBeforeInstallation**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_rebootrequiredbeforeinstallation) | <span data-ttu-id="38a82-120">取得布林值，這個值表示安裝或卸載更新之前是否需要重新開機系統。</span><span class="sxs-lookup"><span data-stu-id="38a82-120">Gets a Boolean value that indicates whether a system restart is required before installing or uninstalling updates.</span></span>                   |
| [<span data-ttu-id="38a82-121">**更新**</span><span class="sxs-lookup"><span data-stu-id="38a82-121">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_updates)                                                   | <span data-ttu-id="38a82-122">取得和設定介面，其中包含指定用於安裝或卸載之更新的唯讀集合。</span><span class="sxs-lookup"><span data-stu-id="38a82-122">Gets and sets an interface that contains a read-only collection of the updates that are specified for installation or uninstallation.</span></span> |



 

 

 



