---
description: 本節說明 Windows Shell 介面。
title: 命令介面
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 05223970-14f5-44c2-937b-07826b8aecf9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 23bd87e86ba9e30ce443616920326bf37aba6d2c
ms.sourcegitcommit: 9a614d8ce23dcca88873148683d9ec7d38be57b9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/12/2020
ms.locfileid: "104383393"
---
# <a name="shell-interfaces"></a><span data-ttu-id="71ab3-103">命令介面</span><span class="sxs-lookup"><span data-stu-id="71ab3-103">Shell Interfaces</span></span>

<span data-ttu-id="71ab3-104">本節說明 Windows Shell 介面。</span><span class="sxs-lookup"><span data-stu-id="71ab3-104">This section describes the Windows Shell interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="71ab3-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="71ab3-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71ab3-106">主題</span><span class="sxs-lookup"><span data-stu-id="71ab3-106">Topic</span></span></th>
<th><span data-ttu-id="71ab3-107">描述</span><span class="sxs-lookup"><span data-stu-id="71ab3-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="71ab3-108"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iaccessibleobject"><strong>IAccessibleObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-108"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iaccessibleobject"><strong>IAccessibleObject</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-109">公開可供協助工具應用程式使用的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-109">Exposes a method that can be used by an accessibility application.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-110"><a href="/previous-versions/windows/desktop/legacy/hh448546(v=vs.85)"><strong>IAccessibilityDockingService</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-110"><a href="/previous-versions/windows/desktop/legacy/hh448546(v=vs.85)"><strong>IAccessibilityDockingService</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-111">將單一協助工具應用程式視窗停駐在螢幕底部。</span><span class="sxs-lookup"><span data-stu-id="71ab3-111">Docks a single accessibility app window to the bottom of a screen.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-112"><a href="/previous-versions/windows/desktop/legacy/hh448547(v=vs.85)"><strong>IAccessibilityDockingServiceCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-112"><a href="/previous-versions/windows/desktop/legacy/hh448547(v=vs.85)"><strong>IAccessibilityDockingServiceCallback</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-113">通知協助工具應用程式其視窗已取消停駐。</span><span class="sxs-lookup"><span data-stu-id="71ab3-113">Informs an accessibility app that its window has been undocked.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-114"><a href="iaclcustommru.md"><strong>IACLCustomMRU</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-114"><a href="iaclcustommru.md"><strong>IACLCustomMRU</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-115">公開方法，這些方法可用來初始化自動完成物件的最近使用 (MRU) 清單。</span><span class="sxs-lookup"><span data-stu-id="71ab3-115">Exposes methods that are used to initialize a most recently used (MRU) list for an autocompletion object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-116"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist"><strong>IACList</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-116"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist"><strong>IACList</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-117">公開在階層中組織候選字串時，改善 <a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete"><strong>自動完成效率的方法</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="71ab3-117">Exposes a method that improves the efficiency of <a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete"><strong>autocompletion</strong></a> when the candidate strings are organized in a hierarchy.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-118"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist2"><strong>IACList2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-118"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist2"><strong>IACList2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-119">擴充 <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist"><strong>IACList</strong></a> 介面，以啟用自動完成物件的用戶端，以抓取和設定選項旗標。</span><span class="sxs-lookup"><span data-stu-id="71ab3-119">Extends the <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist"><strong>IACList</strong></a> interface to enable clients of an autocomplete object to retrieve and set option flags.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-120"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress"><strong>IActionProgress</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-120"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress"><strong>IActionProgress</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-121">表示可從中繼承進度驅動作業的抽象基類。</span><span class="sxs-lookup"><span data-stu-id="71ab3-121">Represents the abstract base class from which progress-driven operations can inherit.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-122"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogressdialog"><strong>IActionProgressDialog</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-122"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogressdialog"><strong>IActionProgressDialog</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-123">公開初始化和停止進度對話方塊的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-123">Exposes methods that initialize and stop a progress dialog.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-124"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationactivationmanager"><strong>IApplicationActivationManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-124"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationactivationmanager"><strong>IApplicationActivationManager</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-125">提供可針對啟動、檔案和通訊協定 <a href="/previous-versions/windows/apps/hh464906(v=win.10)">延伸</a>模組啟用 Windows Store 應用程式的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-125">Provides methods which activate Windows Store apps for the Launch, File, and Protocol <a href="/previous-versions/windows/apps/hh464906(v=win.10)">extensions</a>.</span></span> <span data-ttu-id="71ab3-126">您通常會在偵錯工具和設計工具中使用此介面。</span><span class="sxs-lookup"><span data-stu-id="71ab3-126">You will normally use this interface in debuggers and design tools.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-127"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>IApplicationAssociationRegistration</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-127"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>IApplicationAssociationRegistration</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-128">公開方法，以查詢及設定特定檔案 <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype"><strong>關聯類型</strong></a>的預設應用程式，以及特定 <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel"><strong>關聯層級</strong></a>的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="71ab3-128">Exposes methods that query and set default applications for specific file <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype"><strong>Association Type</strong></a>, and protocols at a specific <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel"><strong>Association Level</strong></a>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="71ab3-129">從 Windows 8，此介面唯一支援的功能是 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault"><strong>QueryCurrentDefault</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="71ab3-129">As of Windows 8, the only functionality of this interface that is supported is <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault"><strong>QueryCurrentDefault</strong></a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-130"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui"><strong>IApplicationAssociationRegistrationUI</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-130"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui"><strong>IApplicationAssociationRegistrationUI</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-131">公開一個方法，此方法會啟動 [高級關聯] 對話方塊，讓使用者可以自訂其關聯。</span><span class="sxs-lookup"><span data-stu-id="71ab3-131">Exposes a method that launches an advanced association dialog box through which the user can customize their associations.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-132"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings"><strong>IApplicationDesignModeSettings</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-132"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings"><strong>IApplicationDesignModeSettings</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-133">讓開發工具應用程式能動態地詐騙系統和使用者狀態，例如原生顯示器解析度、裝置縮放比例和應用程式檢視狀態，以測試在設計模式中執行的 Windows Store 應用程式是否有各式各樣的外型規格，而不需要實際硬體。</span><span class="sxs-lookup"><span data-stu-id="71ab3-133">Enables development tool applications to dynamically spoof system and user states, such as native display resolution, device scale factor, and application view state, for the purpose of testing Windows Store apps running in design mode for a wide range of form factors without the need for the actual hardware.</span></span> <span data-ttu-id="71ab3-134">也可讓您測試一般使用者控制狀態的變更，以便在各種案例下測試 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-134">Also enables testing of changes in normally user-controlled state to test Windows Store apps under a variety of scenarios.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-135"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings2"><strong>IApplicationDesignModeSettings2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-135"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings2"><strong>IApplicationDesignModeSettings2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-136">可讓開發工具應用程式以動態方式控制系統和使用者狀態，例如原生顯示器解析度、裝置縮放因素和應用程式視圖配置，回報給 Windows Store 應用程式，以測試在設計模式下針對各種外型規格執行的 Windows Store 應用程式，而不需要實際硬體。</span><span class="sxs-lookup"><span data-stu-id="71ab3-136">Enables development tool applications to dynamically control system and user states, such as native display resolution, device scale factor, and application view layout, reported to Windows Store apps for the purpose of testing Windows Store apps running in design mode for a wide range of form factors without the need for the actual hardware.</span></span> <span data-ttu-id="71ab3-137">也可讓您測試一般使用者控制狀態的變更，以便在各種案例下測試 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-137">Also enables testing of changes in normally user-controlled state to test Windows Store apps under a variety of scenarios.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-138"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations"><strong>IApplicationDestinations</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-138"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations"><strong>IApplicationDestinations</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-139">公開方法，以允許應用程式從捷徑清單中 <strong>最新</strong> 或 <strong>經常</strong> 的類別中移除一個或多個目的地。</span><span class="sxs-lookup"><span data-stu-id="71ab3-139">Exposes methods that allow an application to remove one or all destinations from the <strong>Recent</strong> or <strong>Frequent</strong> categories in a Jump List.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-140"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists"><strong>IApplicationDocumentLists</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-140"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists"><strong>IApplicationDocumentLists</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-141">公開方法，以允許應用程式抓取捷徑清單中 <strong>最新</strong> 或 <strong>頻繁</strong> 類別目錄的內容。</span><span class="sxs-lookup"><span data-stu-id="71ab3-141">Exposes methods that allow an application to retrieve the contents of the <strong>Recent</strong> or <strong>Frequent</strong> categories in a Jump List.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-142"><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher"><strong>IAppPublisher</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-142"><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher"><strong>IAppPublisher</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-143">公開透過主控台中的 [ <strong>新增/移除程式</strong> ] 來發佈應用程式的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-143">Exposes methods for publishing applications through <strong>Add/Remove Programs</strong> in Control Panel.</span></span> <span data-ttu-id="71ab3-144">這是針對此用途所執行的主要介面。</span><span class="sxs-lookup"><span data-stu-id="71ab3-144">This is the principal interface implemented for this purpose.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-145"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibility"><strong>IAppVisibility</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-145"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibility"><strong>IAppVisibility</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-146">提供用來判斷顯示是否顯示 Windows Store 應用程式的功能。</span><span class="sxs-lookup"><span data-stu-id="71ab3-146">Provides functionality to determine whether the display is showing Windows Store apps.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-147"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibilityevents"><strong>IAppVisibilityEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-147"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibilityevents"><strong>IAppVisibilityEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-148">可讓應用程式在開始畫面可見度的顯示和變更中，接收狀態變更的通知。</span><span class="sxs-lookup"><span data-stu-id="71ab3-148">Enables applications to receive notifications of state changes in a display and of changes in Start screen visibility.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-149"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler"><strong>IAssocHandler</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-149"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler"><strong>IAssocHandler</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-150">使用檔案關聯對話方塊或功能表公開作業的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-150">Exposes methods for operations with a file association dialog box or menu.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-151"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandlerinvoker"><strong>IAssocHandlerInvoker</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-151"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandlerinvoker"><strong>IAssocHandlerInvoker</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-152">公開方法，以叫用相關聯的應用程式處理常式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-152">Exposes methods that invoke an associated application handler.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-153"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute"><strong>IAttachmentExecute</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-153"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute"><strong>IAttachmentExecute</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-154">公開可與用戶端應用程式搭配使用的方法，以呈現可透過電子郵件和郵件附件安全地下載和交換檔案的使用者環境。</span><span class="sxs-lookup"><span data-stu-id="71ab3-154">Exposes methods that work with client applications to present a user environment that provides safe download and exchange of files through email and messaging attachments.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-155"><a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete"><strong>IAutoComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-155"><a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete"><strong>IAutoComplete</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-156">由自動完成物件公開 (CLSID_AutoComplete) 。</span><span class="sxs-lookup"><span data-stu-id="71ab3-156">Exposed by the autocomplete object (CLSID_AutoComplete).</span></span> <span data-ttu-id="71ab3-157">這個介面可讓應用程式初始化、啟用和停用物件。</span><span class="sxs-lookup"><span data-stu-id="71ab3-157">This interface allows applications to initialize, enable, and disable the object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-158"><a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete2"><strong>IAutoComplete2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-158"><a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete2"><strong>IAutoComplete2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-159">擴充 <a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete"><strong>IAutoComplete</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="71ab3-159">Extends <a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete"><strong>IAutoComplete</strong></a>.</span></span> <span data-ttu-id="71ab3-160">這個介面可讓自動完成物件的用戶端抓取和設定許多選項，以控制自動完成的運作方式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-160">This interface enables clients of the autocomplete object to retrieve and set a number of options that control how autocompletion operates.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-161"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iautocompletedropdown"><strong>IAutoCompleteDropDown</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-161"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iautocompletedropdown"><strong>IAutoCompleteDropDown</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-162">公開方法，讓用戶端可以重設或查詢 [自動完成] 下拉式清單的顯示狀態，其中包含使用者在編輯控制項中輸入之字串的可能完成。</span><span class="sxs-lookup"><span data-stu-id="71ab3-162">Exposes methods that allow clients to reset or query the display state of the autocomplete drop-down list, which contains possible completions to a string entered by the user in an edit control.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-163"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ibandhost"><strong>IBandHost</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-163"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ibandhost"><strong>IBandHost</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-164">公開建立和終結群組並指定其可用性的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-164">Exposes methods that create and destroy bands and specifiy their availability.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-165"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ibandsite"><strong>IBandSite</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-165"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ibandsite"><strong>IBandSite</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-166">公開控制頻外物件的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-166">Exposes methods that control band objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-167"><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ibrowserframeoptions"><strong>IBrowserFrameOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-167"><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ibrowserframeoptions"><strong>IBrowserFrameOptions</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-168">允許瀏覽器或主機要求 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a> 支援何種視圖行為。</span><span class="sxs-lookup"><span data-stu-id="71ab3-168">Allows a browser or host to ask <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a> what kind of view behavior is supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-169"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icategorizer"><strong>ICategorizer</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-169"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icategorizer"><strong>ICategorizer</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-170">公開用來取得專案識別碼清單相關資訊的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-170">Exposes methods that are used to obtain information about item identifier lists.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-171"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icategoryprovider"><strong>ICategoryProvider</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-171"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icategoryprovider"><strong>ICategoryProvider</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-172">公開在 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a>上註冊的 categorizers 清單。</span><span class="sxs-lookup"><span data-stu-id="71ab3-172">Exposes a list of categorizers registered on an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-173"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-icdburn"><strong>ICDBurn</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-173"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-icdburn"><strong>ICDBurn</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-174">公開的方法可判斷系統是否有硬體可寫入 CD、CD 寫入器裝置的磁碟機號，以及以程式設計方式起始 CD 寫入會話。</span><span class="sxs-lookup"><span data-stu-id="71ab3-174">Exposes methods that determine whether a system has hardware for writing to CD, the drive letter of a CD writer device, and programmatically initiate a CD writing session.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-175"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>IColumnManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-175"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>IColumnManager</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-176">公開方法，以啟用 Windows 檔案總管詳細資料檢視中的資料行檢查和操作。</span><span class="sxs-lookup"><span data-stu-id="71ab3-176">Exposes methods that enable inspection and manipulation of columns in the Windows Explorer Details view.</span></span> <span data-ttu-id="71ab3-177">每個資料行都是由命名屬性的 <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> 結構所參考。</span><span class="sxs-lookup"><span data-stu-id="71ab3-177">Each column is referenced by a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> structure, which names a property.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-178"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser"><strong>ICommDlgBrowser</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-178"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser"><strong>ICommDlgBrowser</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-179">由一般檔案對話方塊公開，以供它們在裝載 Shell 瀏覽器時使用。</span><span class="sxs-lookup"><span data-stu-id="71ab3-179">Exposed by the common file dialog boxes to be used when they host a Shell browser.</span></span> <span data-ttu-id="71ab3-180">如果支援， <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser"><strong>ICommDlgBrowser</strong></a> 會公開方法，以允許 Shell 視圖處理在對話方塊中需要不同行為的幾個案例，而不是在一般 Shell 視圖中。</span><span class="sxs-lookup"><span data-stu-id="71ab3-180">If supported, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser"><strong>ICommDlgBrowser</strong></a> exposes methods that allow a Shell view to handle several cases that require different behavior in a dialog box than in a normal Shell view.</span></span> <span data-ttu-id="71ab3-181">您可以藉由在<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser"><strong>IShellBrowser</strong></a>物件上呼叫<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a>來取得<strong>ICommDlgBrowser</strong>介面指標。</span><span class="sxs-lookup"><span data-stu-id="71ab3-181">You obtain an <strong>ICommDlgBrowser</strong> interface pointer by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> on the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser"><strong>IShellBrowser</strong></a> object.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-182"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2"><strong>ICommDlgBrowser2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-182"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2"><strong>ICommDlgBrowser2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-183">擴充 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser"><strong>ICommDlgBrowser</strong></a>的功能。</span><span class="sxs-lookup"><span data-stu-id="71ab3-183">Extends the capabilities of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser"><strong>ICommDlgBrowser</strong></a>.</span></span> <span data-ttu-id="71ab3-184">這些介面是在裝載 Shell 瀏覽器時，由一般檔案對話方塊所公開。</span><span class="sxs-lookup"><span data-stu-id="71ab3-184">This interface is exposed by the common file dialog boxes when they host a Shell browser.</span></span> <span data-ttu-id="71ab3-185">您可以藉由在<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser"><strong>IShellBrowser</strong></a>物件上呼叫<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a>來取得<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2"><strong>ICommDlgBrowser2</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="71ab3-185">A pointer to <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2"><strong>ICommDlgBrowser2</strong></a> can be obtained by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> on the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser"><strong>IShellBrowser</strong></a> object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-186"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-icommdlgbrowser3"><strong>ICommDlgBrowser3</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-186"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-icommdlgbrowser3"><strong>ICommDlgBrowser3</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-187">擴充 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2"><strong>ICommDlgBrowser2</strong></a>的功能，並在裝載 Shell 瀏覽器時由一般檔案對話方塊使用。</span><span class="sxs-lookup"><span data-stu-id="71ab3-187">Extends the capabilities of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2"><strong>ICommDlgBrowser2</strong></a>, and used by the common file dialog boxes when they host a Shell browser.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-188"><a href="/windows/desktop/api/shobjidl/nn-shobjidl-icomputerinfochangenotify"><strong>IComputerInfoChangeNotify</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-188"><a href="/windows/desktop/api/shobjidl/nn-shobjidl-icomputerinfochangenotify"><strong>IComputerInfoChangeNotify</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-189">這個介面可能在較新版本的 Windows 中不存在。</span><span class="sxs-lookup"><span data-stu-id="71ab3-189">This interface may be absent in later versions of Windows.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-190"><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-iconnectablecredentialprovidercredential"><strong>IConnectableCredentialProviderCredential</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-190"><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-iconnectablecredentialprovidercredential"><strong>IConnectableCredentialProviderCredential</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-191">公開連接和中斷連接 <a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-iconnectablecredentialprovidercredential"><strong>IConnectableCredentialProviderCredential</strong></a> 物件的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-191">Exposes methods for connecting and disconnecting <a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-iconnectablecredentialprovidercredential"><strong>IConnectableCredentialProviderCredential</strong></a> objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-192"><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-icontactmanagerinterop"><strong>IContactManagerInterop</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-192"><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-icontactmanagerinterop"><strong>IContactManagerInterop</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-193">可存取管理多個視窗的應用程式中的 <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-icontactmanagerinterop"><strong>ContactManager</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-193">Enables access to <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-icontactmanagerinterop"><strong>ContactManager</strong></a> methods in an app that manages multiple windows.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-194"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu"><strong>ICoNtextMenu</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-194"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu"><strong>IContextMenu</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-195">公開方法，以建立或合併與 Shell 物件相關聯的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="71ab3-195">Exposes methods that either create or merge a shortcut menu associated with a Shell object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-196"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2"><strong>ICoNtextMenu2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-196"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2"><strong>IContextMenu2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-197">公開方法，以建立或合併與 Shell 物件相關聯的快捷方式 (內容) 功能表。</span><span class="sxs-lookup"><span data-stu-id="71ab3-197">Exposes methods that either create or merge a shortcut (context) menu associated with a Shell object.</span></span> <span data-ttu-id="71ab3-198">藉由新增方法來擴充 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu"><strong>ICoNtextMenu</strong></a> ，以允許用戶端物件處理與主控描繪功能表項目相關聯的訊息。</span><span class="sxs-lookup"><span data-stu-id="71ab3-198">Extends <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu"><strong>IContextMenu</strong></a> by adding a method that allows client objects to handle messages associated with owner-drawn menu items.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-199"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3"><strong>ICoNtextMenu3</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-199"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3"><strong>IContextMenu3</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-200">公開方法，以建立或合併與 Shell 物件相關聯的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="71ab3-200">Exposes methods that either create or merge a shortcut menu associated with a Shell object.</span></span> <span data-ttu-id="71ab3-201">允許用戶端物件處理與主控描繪功能表項目相關聯的訊息，並接受來自該訊息處理的傳回值來擴充 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2"><strong>ICoNtextMenu2</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="71ab3-201">Allows client objects to handle messages associated with owner-drawn menu items and extends <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2"><strong>IContextMenu2</strong></a> by accepting a return value from that message handling.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-202"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb"><strong>ICoNtextMenuCB</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-202"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb"><strong>IContextMenuCB</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-203">公開啟用內容功能表回呼的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-203">Exposes a method that enables the callback of a context menu.</span></span> <span data-ttu-id="71ab3-204">例如，在需要提高許可權的 <strong>menuItem</strong> 中加入盾牌圖示。</span><span class="sxs-lookup"><span data-stu-id="71ab3-204">For example, to add a shield icon to a <strong>menuItem</strong> that requires elevation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-205"><a href="/previous-versions/windows/desktop/legacy/bb776063(v=vs.85)"><strong>IControlMarkup</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-205"><a href="/previous-versions/windows/desktop/legacy/bb776063(v=vs.85)"><strong>IControlMarkup</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-206"><a href="/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)"><strong>ICopyHook</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-206"><a href="/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)"><strong>ICopyHook</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-207">公開建立 <em>複製勾點處理常式</em>的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-207">Exposes a method that creates a <em>copy hook handler</em>.</span></span> <span data-ttu-id="71ab3-208">複製勾點處理常式是一個 Shell 延伸模組，可決定是否可以移動、複製、重新命名或刪除 Shell 資料夾或印表機物件。</span><span class="sxs-lookup"><span data-stu-id="71ab3-208">A copy hook handler is a Shell extension that determines if a Shell folder or printer object can be moved, copied, renamed, or deleted.</span></span> <span data-ttu-id="71ab3-209">Shell 會在執行這些作業的其中一項之前呼叫 <a href="/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)"><strong>ICopyHook：： CopyCallback</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-209">The Shell calls the <a href="/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)"><strong>ICopyHook::CopyCallback</strong></a> method prior to performing one of these operations.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-210"><a href="/windows/desktop/api/Propsys/nn-propsys-icreateobject"><strong>ICreateObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-210"><a href="/windows/desktop/api/Propsys/nn-propsys-icreateobject"><strong>ICreateObject</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-211">公開建立指定類別之物件的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-211">Exposes a method that creates an object of a specified class.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-212"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreatingprocess"><strong>ICreatingProcess</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-212"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreatingprocess"><strong>ICreatingProcess</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-213">由 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu"><strong>ICoNtextMenu</strong></a> 使用，可讓呼叫者改變正在建立之進程的某些參數。</span><span class="sxs-lookup"><span data-stu-id="71ab3-213">Used by <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu"><strong>IContextMenu</strong></a> to allow the caller to alter some parameters of the process being created.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-214"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreateprocessinputs"><strong>ICreateProcessInputs</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-214"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreateprocessinputs"><strong>ICreateProcessInputs</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-215">供 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreatingprocess"><strong>ICreatingProcess</strong></a> 介面用來改變正在建立之進程的某些參數。</span><span class="sxs-lookup"><span data-stu-id="71ab3-215">Used by the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreatingprocess"><strong>ICreatingProcess</strong></a> interface to alter some parameters of the process that is being created.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-216"><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovider"><strong>ICredentialProvider</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-216"><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovider"><strong>ICredentialProvider</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-217">公開用於設定和操作認證提供者的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-217">Exposes methods used in the setup and manipulation of a credential provider.</span></span> <span data-ttu-id="71ab3-218">所有認證提供者都必須執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="71ab3-218">All credential providers must implement this interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-219"><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredential"><strong>ICredentialProviderCredential</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-219"><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredential"><strong>ICredentialProviderCredential</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-220">公開可讓您處理認證的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-220">Exposes methods that enable the handling of a credential.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-221"><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidercredential2"><strong>ICredentialProviderCredential2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-221"><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidercredential2"><strong>ICredentialProviderCredential2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-222">藉由新增方法來擴充 <a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredential"><strong>ICredentialProviderCredential</strong></a> 介面，以抓取使用者的安全識別碼 (SID) 。</span><span class="sxs-lookup"><span data-stu-id="71ab3-222">Extends the <a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredential"><strong>ICredentialProviderCredential</strong></a> interface by adding a method that retrieves the security identifier (SID) of a user.</span></span> <span data-ttu-id="71ab3-223">認證會與該使用者相關聯，並可在使用者的磚下分組。</span><span class="sxs-lookup"><span data-stu-id="71ab3-223">The credential is associated with that user and can be grouped under the user's tile.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-224"><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents"><strong>ICredentialProviderCredentialEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-224"><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents"><strong>ICredentialProviderCredentialEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-225">提供一種非同步回呼機制，可讓認證用來通知其登入 UI 或認證 UI 中的狀態或文字變更事件。</span><span class="sxs-lookup"><span data-stu-id="71ab3-225">Provides an asynchronous callback mechanism used by a credential to notify it of state or text change events in the Logon UI or Credential UI.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-226"><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidercredentialevents2"><strong>ICredentialProviderCredentialEvents2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-226"><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidercredentialevents2"><strong>ICredentialProviderCredentialEvents2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-227">藉由新增可在 theLogon UI 或認證 UI 中啟用欄位批次更新的方法，擴充 <a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents"><strong>ICredentialProviderCredentialEvents</strong></a> 介面。</span><span class="sxs-lookup"><span data-stu-id="71ab3-227">Extends the <a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents"><strong>ICredentialProviderCredentialEvents</strong></a> interface by adding methods that enable batch updating of fields in theLogon UI or Credential UI.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-228"><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidercredentialwithfieldoptions"><strong>ICredentialProviderCredentialWithFieldOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-228"><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidercredentialwithfieldoptions"><strong>ICredentialProviderCredentialWithFieldOptions</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-229">提供一種方法，可讓認證提供者架構判斷您是否已在登入或認證 UI 中對欄位的選項進行自訂。</span><span class="sxs-lookup"><span data-stu-id="71ab3-229">Provides a method that enables the credential provider framework to determine whether you've made a customization to a field's option in a logon or credential UI.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-230"><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialproviderevents"><strong>ICredentialProviderEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-230"><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialproviderevents"><strong>ICredentialProviderEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-231">提供由認證提供者使用的非同步回呼機制，以通知其認證清單或其欄位的變更。</span><span class="sxs-lookup"><span data-stu-id="71ab3-231">Provides an asynchronous callback mechanism used by a credential provider to notify it of changes in the list of credentials or their fields.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-232"><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialproviderfilter"><strong>ICredentialProviderFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-232"><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialproviderfilter"><strong>ICredentialProviderFilter</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-233">用來根據執行時間可用的資訊，動態篩選認證提供者。</span><span class="sxs-lookup"><span data-stu-id="71ab3-233">Used to dynamically filter credential providers based on information available at runtime.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-234"><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidersetuserarray"><strong>ICredentialProviderSetUserArray</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-234"><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidersetuserarray"><strong>ICredentialProviderSetUserArray</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-235">提供一種方法，可讓認證提供者接收將在登入或認證 UI 中顯示的使用者集合。</span><span class="sxs-lookup"><span data-stu-id="71ab3-235">Provides a method that enables a credential provider to receive the set of users that will be shown in the logon or credential UI.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-236"><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovideruser"><strong>ICredentialProviderUser</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-236"><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovideruser"><strong>ICredentialProviderUser</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-237">提供方法，用來抓取登入或認證 UI 中所包含之個別使用者的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="71ab3-237">Provides methods used to retrieve certain properties of an individual user included in a logon or credential UI.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-238"><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovideruserarray"><strong>ICredentialProviderUserArray</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-238"><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovideruserarray"><strong>ICredentialProviderUserArray</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-239">代表將出現在登入或認證 UI 中的使用者集合。</span><span class="sxs-lookup"><span data-stu-id="71ab3-239">Represents the set of users that will appear in the logon or credential UI.</span></span> <span data-ttu-id="71ab3-240">這項資訊可讓認證提供者列舉集合，以抓取每個使用者的相關屬性資訊，以填入欄位或篩選集合。</span><span class="sxs-lookup"><span data-stu-id="71ab3-240">This information enables the credential provider to enumerate the set to retrieve property information about each user to populate fields or filter the set.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-241"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icurrentitem"><strong>ICurrentItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-241"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icurrentitem"><strong>ICurrentItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-242">藉由呼叫專案的 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder：： BindToObject</strong></a> 來取得。</span><span class="sxs-lookup"><span data-stu-id="71ab3-242">Obtained by calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a> for an item.</span></span> <span data-ttu-id="71ab3-243">如果專案在先前的時間代表專案的快照集，這個介面會取得專案的目前版本。</span><span class="sxs-lookup"><span data-stu-id="71ab3-243">If the item represents a snapshot of an item at a previous time, this interface will obtain the current version of the item.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-244"><a href="/windows/desktop/api/shlobj/nn-shlobj-icurrentworkingdirectory"><strong>ICurrentWorkingDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-244"><a href="/windows/desktop/api/shlobj/nn-shlobj-icurrentworkingdirectory"><strong>ICurrentWorkingDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-245">公開方法，讓用戶端可以取得或設定物件的目前工作目錄。</span><span class="sxs-lookup"><span data-stu-id="71ab3-245">Exposes methods that enable a client to retrieve or set an object's current working directory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-246"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist"><strong>ICustomDestinationList</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-246"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist"><strong>ICustomDestinationList</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-247">公開方法，以允許應用程式提供可在工作列中顯示的自訂捷徑清單（包括目的地和工作）。</span><span class="sxs-lookup"><span data-stu-id="71ab3-247">Exposes methods that allow an application to provide a custom Jump List, including destinations and tasks, for display in the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-248"><a href="/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability"><strong>IDataObjectAsyncCapability</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-248"><a href="/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability"><strong>IDataObjectAsyncCapability</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-249">啟用通常同步以非同步方式運作的介面。</span><span class="sxs-lookup"><span data-stu-id="71ab3-249">Enables interfaces that are usually synchronous to function asynchronously.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="71ab3-250">此介面是目前的重新命名 <a href="/previous-versions//bb776309(v=vs.85)"><strong>iasyncoperation<tresult>HTTP</strong></a>版本。</span><span class="sxs-lookup"><span data-stu-id="71ab3-250">This interface is the current, renamed version of <a href="/previous-versions//bb776309(v=vs.85)"><strong>IAsyncOperation</strong></a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-251"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idataobjectprovider"><strong>IDataObjectProvider</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-251"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idataobjectprovider"><strong>IDataObjectProvider</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-252">提供可讓您設定或抓取 <a href="/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage?view=winrt-19041">DataPackage</a> 物件之 <a href="/windows/desktop/api/objidl/nn-objidl-idataobject"><strong>IDataObject 介面</strong></a>的方法，DataPackage 會使用此介面來支援互通性。</span><span class="sxs-lookup"><span data-stu-id="71ab3-252">Provides methods that enable you to set or retrieve a <a href="/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage?view=winrt-19041">DataPackage</a> object's <a href="/windows/desktop/api/objidl/nn-objidl-idataobject"><strong>IDataObject interface</strong></a>, which the DataPackage uses to support interoperability.</span></span> <span data-ttu-id="71ab3-253">應用程式會使用 DataPackage 物件來提供資料給另一個應用程式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-253">The DataPackage object is used by an app to provide data to another app.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-254"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idatatransfermanagerinterop"><strong>IDataTransferManagerInterop</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-254"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idatatransfermanagerinterop"><strong>IDataTransferManagerInterop</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-255">可在管理多個視窗的 Windows Store 應用程式中，存取 <a href="/uwp/api/Windows.ApplicationModel.DataTransfer.DataTransferManager"><strong>DataTransferManager</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-255">Enables access to <a href="/uwp/api/Windows.ApplicationModel.DataTransfer.DataTransferManager"><strong>DataTransferManager</strong></a> methods in a Windows Store app that manages multiple windows.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-256"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultextracticoninit"><strong>IDefaultExtractIconInit</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-256"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultextracticoninit"><strong>IDefaultExtractIconInit</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-257">公開方法，以設定與物件相關聯的預設圖示。</span><span class="sxs-lookup"><span data-stu-id="71ab3-257">Exposes methods to set default icons associated with an object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-258"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultfoldermenuinitialize"><strong>IDefaultFolderMenuInitialize</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-258"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultfoldermenuinitialize"><strong>IDefaultFolderMenuInitialize</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-259">提供用來取得及設定快捷方式功能表資訊的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-259">Provides methods used to get and set shortcut menu information.</span></span> <span data-ttu-id="71ab3-260">這項資訊與透過<a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu"><strong>DEFCONTEXTMENU</strong></a>結構提供給<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>SHCreateDefaultCoNtextMenu</strong></a>的資訊相同。</span><span class="sxs-lookup"><span data-stu-id="71ab3-260">This information is the same as that provided to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>SHCreateDefaultContextMenu</strong></a> through the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu"><strong>DEFCONTEXTMENU</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-261"><a href="/windows/desktop/api/Propsys/nn-propsys-idelayedpropertystorefactory"><strong>IDelayedPropertyStoreFactory</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-261"><a href="/windows/desktop/api/Propsys/nn-propsys-idelayedpropertystorefactory"><strong>IDelayedPropertyStoreFactory</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-262">公開方法，以在屬性存取可能很慢的情況下，建立指定的 <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="71ab3-262">Exposes a method to create a specified <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> object in circumstances where property access is potentially slow.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-263"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idelegatefolder"><strong>IDelegateFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-263"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idelegatefolder"><strong>IDelegateFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-264">公開方法，透過這個方法，會為委派資料夾提供配置和釋放專案識別碼所需的 <a href="/windows/desktop/api/objidl/nn-objidl-imalloc"><strong>IMalloc</strong></a> 介面。</span><span class="sxs-lookup"><span data-stu-id="71ab3-264">Exposes a method through which a delegate folder is given the <a href="/windows/desktop/api/objidl/nn-objidl-imalloc"><strong>IMalloc</strong></a> interface required to allocate and free item IDs.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-265"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idelegateitem"><strong>IDelegateItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-265"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idelegateitem"><strong>IDelegateItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-266">用來取得專案路徑的立即基礎標記法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-266">Used to obtain the immediately underlying representation of an item's path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-267"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-idesktopgadget"><strong>IDesktopGadget</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-267"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-idesktopgadget"><strong>IDesktopGadget</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-268">公開一種方法，可讓您以程式設計方式將已安裝的小工具加入使用者的桌面。</span><span class="sxs-lookup"><span data-stu-id="71ab3-268">Exposes a method that allows the programmatic addition of an installed gadget to the user's desktop.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-269"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idesktopwallpaper"><strong>IDesktopWallpaper</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-269"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idesktopwallpaper"><strong>IDesktopWallpaper</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-270"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory"><strong>IDestinationStreamFactory</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-270"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory"><strong>IDestinationStreamFactory</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-271">公開在將變更套用至屬性之前，手動複製資料流程或檔案的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-271">Exposes a method for manually copying a stream or file before applying changes to properties.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-272"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idisplayitem"><strong>IDisplayItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-272"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idisplayitem"><strong>IDisplayItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-273">公開方法，這些方法會尋找要用來取得顯示內容（例如專案名稱）的目前專案版本，此專案會顯示在 UI 中。</span><span class="sxs-lookup"><span data-stu-id="71ab3-273">Exposes methods that find a version of the current item to be used to get display properties, such as the item name, that will be displayed in the UI.</span></span> <span data-ttu-id="71ab3-274">供複製引擎對話方塊用來提供 UI，以顯示適當的專案。</span><span class="sxs-lookup"><span data-stu-id="71ab3-274">Used by the copy engine dialogs to provide the UI with an appropriate item to display.</span></span> <span data-ttu-id="71ab3-275">如果找不到其他版本，會使用目前的專案。</span><span class="sxs-lookup"><span data-stu-id="71ab3-275">If no other version can be found, the current item is used.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-276"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow"><strong>IDockingWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-276"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow"><strong>IDockingWindow</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-277">公開通知停駐視窗物件變更的方法，包括顯示、隱藏和即將移除。</span><span class="sxs-lookup"><span data-stu-id="71ab3-277">Exposes methods that notify the docking window object of changes, including showing, hiding, and impending removal.</span></span> <span data-ttu-id="71ab3-278">這個介面是由視窗物件所執行，這些物件可以停駐在 Windows 檔案總管視窗的框線空間內。</span><span class="sxs-lookup"><span data-stu-id="71ab3-278">This interface is implemented by window objects that can be docked within the border space of a Windows Explorer window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-279"><a href="/windows/desktop/api/shlobj/nn-shlobj-idockingwindowframe"><strong>IDockingWindowFrame</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-279"><a href="/windows/desktop/api/shlobj/nn-shlobj-idockingwindowframe"><strong>IDockingWindowFrame</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-280">公開支援將 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow"><strong>IDockingWindow</strong></a> 物件新增至框架的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-280">Exposes methods that support the addition of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow"><strong>IDockingWindow</strong></a> objects to a frame.</span></span> <span data-ttu-id="71ab3-281">由瀏覽器所執行。</span><span class="sxs-lookup"><span data-stu-id="71ab3-281">Implemented by the browser.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-282"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-idockingwindowsite"><strong>IDockingWindowSite</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-282"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-idockingwindowsite"><strong>IDockingWindowSite</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-283">公開管理一或多個 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow"><strong>IDockingWindow</strong></a> 物件之框線空間的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-283">Exposes methods that manage the border space for one or more <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow"><strong>IDockingWindow</strong></a> objects.</span></span> <span data-ttu-id="71ab3-284">此介面是由瀏覽器所執行，類似于 <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceuiwindow"><strong>IOleInPlaceUIWindow</strong></a> 介面。</span><span class="sxs-lookup"><span data-stu-id="71ab3-284">This interface is implemented by the browser and is similar to the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceuiwindow"><strong>IOleInPlaceUIWindow</strong></a> interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-285"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper"><strong>IDragSourceHelper</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-285"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper"><strong>IDragSourceHelper</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-286">由 Shell 公開，以允許應用程式指定將在 Shell 拖放作業期間顯示的影像。</span><span class="sxs-lookup"><span data-stu-id="71ab3-286">Exposed by the Shell to allow an application to specify the image that will be displayed during a Shell drag-and-drop operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-287"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-idragsourcehelper2"><strong>IDragSourceHelper2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-287"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-idragsourcehelper2"><strong>IDragSourceHelper2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-288">公開將功能新增至 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper"><strong>IDragSourceHelper</strong></a>的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-288">Exposes a method that adds functionality to <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper"><strong>IDragSourceHelper</strong></a>.</span></span> <span data-ttu-id="71ab3-289">這個方法會設定 <strong>IDragSourceHelper</strong> 物件上拖放作業的特性。</span><span class="sxs-lookup"><span data-stu-id="71ab3-289">This method sets the characteristics of a drag-and-drop operation over an <strong>IDragSourceHelper</strong> object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-290"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper"><strong>IDropTargetHelper</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-290"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper"><strong>IDropTargetHelper</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-291">公開方法，以在影像在目標視窗上時，讓卸載目標顯示拖曳影像。</span><span class="sxs-lookup"><span data-stu-id="71ab3-291">Exposes methods that allow drop targets to display a drag image while the image is over the target window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-292"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-idynamichwhandler"><strong>IDynamicHWHandler</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-292"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-idynamichwhandler"><strong>IDynamicHWHandler</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-293">由自動播放所呼叫。</span><span class="sxs-lookup"><span data-stu-id="71ab3-293">Called by AutoPlay.</span></span> <span data-ttu-id="71ab3-294">公開方法，這些方法會在向使用者顯示已註冊的處理常式之前，取得相關動態資訊。</span><span class="sxs-lookup"><span data-stu-id="71ab3-294">Exposes methods that get dynamic information regarding a registered handler prior to displaying it to the user.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-295"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumassochandlers"><strong>IEnumAssocHandlers</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-295"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumassochandlers"><strong>IEnumAssocHandlers</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-296">公開方法，這個方法允許列舉與特定副檔名相關聯的處理常式集合。</span><span class="sxs-lookup"><span data-stu-id="71ab3-296">Exposes a method that allows enumeration of a collection of handlers associated with particular file name extensions.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-297"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ienumerableview"><strong>IEnumerableView</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-297"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ienumerableview"><strong>IEnumerableView</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-298">公開列舉視圖內容的方法，並在列舉完成時接收回呼的通知。</span><span class="sxs-lookup"><span data-stu-id="71ab3-298">Exposes methods that enumerate the contents of a view and receive notification from callback upon enumeration completion.</span></span> <span data-ttu-id="71ab3-299">此介面可讓視圖的用戶端嘗試共用資料夾內容的視圖清單。</span><span class="sxs-lookup"><span data-stu-id="71ab3-299">This interface enables clients of a view to attempt to share the view's list of folder contents.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-300"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumexplorercommand"><strong>IEnumExplorerCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-300"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumexplorercommand"><strong>IEnumExplorerCommand</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-301">由 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a>所提供。</span><span class="sxs-lookup"><span data-stu-id="71ab3-301">Provided by an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a>.</span></span> <span data-ttu-id="71ab3-302">此介面包含要放入命令列的命令列舉。</span><span class="sxs-lookup"><span data-stu-id="71ab3-302">This interface contains the enumeration of commands to be put into the command bar.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-303"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumextrasearch"><strong>IEnumExtraSearch</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-303"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumextrasearch"><strong>IEnumExtraSearch</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-304">用戶端用來判斷資料夾之可用搜尋物件的標準 OLE 列舉值。</span><span class="sxs-lookup"><span data-stu-id="71ab3-304">A standard OLE enumerator used by a client to determine the available search objects for a folder.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-305"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumfullidlist"><strong>IEnumFullIDList</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-305"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumfullidlist"><strong>IEnumFullIDList</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-306">公開一組標準的方法，這些方法會列舉 Shell 資料夾中專案 (Pidl) 專案識別碼清單的指標。</span><span class="sxs-lookup"><span data-stu-id="71ab3-306">Exposes a standard set of methods that enumerate the pointers to item identifier lists (PIDLs) of the items in a Shell folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-307"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist"><strong>IEnumIDList</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-307"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist"><strong>IEnumIDList</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-308">公開一組標準的方法，這些方法可用來列舉 Shell 資料夾中專案的 Pidl。</span><span class="sxs-lookup"><span data-stu-id="71ab3-308">Exposes a standard set of methods used to enumerate the PIDLs of the items in a Shell folder.</span></span> <span data-ttu-id="71ab3-309">當呼叫資料夾的 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>IShellFolder：： EnumObjects</strong></a> 方法時，它會建立列舉物件，並將物件的 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist"><strong>IEnumIDList</strong></a> 介面指標傳回給呼叫的應用程式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-309">When a folder's <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>IShellFolder::EnumObjects</strong></a> method is called, it creates an enumeration object and passes a pointer to the object's <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist"><strong>IEnumIDList</strong></a> interface back to the calling application.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-310"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumobjects"><strong>IEnumObjects</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-310"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumobjects"><strong>IEnumObjects</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-311">公開方法以列舉未知的物件。</span><span class="sxs-lookup"><span data-stu-id="71ab3-311">Exposes methods to enumerate unknown objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-312"><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps"><strong>IEnumPublishedApps</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-312"><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps"><strong>IEnumPublishedApps</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-313">公開列舉已發佈應用程式以在主控台中新增/移除程式的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-313">Exposes methods that enumerate published applications to Add/Remove Programs in the Control Panel.</span></span> <span data-ttu-id="71ab3-314">公開此介面的物件是透過 <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-iapppublisher-enumapps"><strong>IAppPublisher：： EnumApps</strong></a>要求。</span><span class="sxs-lookup"><span data-stu-id="71ab3-314">The object exposing this interface is requested through <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-iapppublisher-enumapps"><strong>IAppPublisher::EnumApps</strong></a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-315"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ienumreadycallback"><strong>IEnumReadyCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-315"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ienumreadycallback"><strong>IEnumReadyCallback</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-316">公開方法，這種方法可讓您在列舉完成時，通知實施者。</span><span class="sxs-lookup"><span data-stu-id="71ab3-316">Exposes methods that enable the view to notify the implementer when the enumeration has completed.</span></span> <span data-ttu-id="71ab3-317">此視圖會呼叫這個方法，告訴實施者可以透過 <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-ienumerableview-createenumidlistfromcontents"><strong>IEnumerableView：： CreateEnumIDListFromContents</strong></a>抓取列舉。</span><span class="sxs-lookup"><span data-stu-id="71ab3-317">The view calls this method to tell the implementer that the enumeration can be retrieved via <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-ienumerableview-createenumidlistfromcontents"><strong>IEnumerableView::CreateEnumIDListFromContents</strong></a>.</span></span> <span data-ttu-id="71ab3-318">回呼可讓實施者共用 views 列舉。</span><span class="sxs-lookup"><span data-stu-id="71ab3-318">The callback allows the implementer to share the views enumeration.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-319"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumresources"><strong>IEnumResources</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-319"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumresources"><strong>IEnumResources</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-320">公開資源列舉方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-320">Exposes resource enumeration methods.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-321"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems"><strong>IEnumShellItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-321"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems"><strong>IEnumShellItems</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-322">公開 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> 介面的列舉。</span><span class="sxs-lookup"><span data-stu-id="71ab3-322">Exposes enumeration of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> interfaces.</span></span> <span data-ttu-id="71ab3-323">這個介面通常是藉由呼叫 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems"><strong>IEnumShellItems</strong></a> 方法來取得。</span><span class="sxs-lookup"><span data-stu-id="71ab3-323">This interface is typically obtained by calling the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems"><strong>IEnumShellItems</strong></a> method.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-324"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrconflict"><strong>IEnumSyncMgrConflict</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-324"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrconflict"><strong>IEnumSyncMgrConflict</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-325">公開衝突列舉方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-325">Exposes conflict enumeration methods.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-326"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrevents"><strong>IEnumSyncMgrEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-326"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrevents"><strong>IEnumSyncMgrEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-327">公開同步事件列舉方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-327">Exposes sync event enumeration methods.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-328"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems"><strong>IEnumSyncMgrSyncItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-328"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems"><strong>IEnumSyncMgrSyncItems</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-329">公開列舉處理常式所管理之同步處理專案物件的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-329">Exposes methods that enumerate the sync item objects managed by the handler.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-330"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-330"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-331">公開方法，以設定與命令動詞相關的指定狀態或參數，以及叫用該動詞命令的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-331">Exposes methods that set a given state or parameter related to the command verb, as well as a method to invoke that verb.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-332"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommandapplicationhostenvironment"><strong>IExecuteCommandApplicationHostEnvironment</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-332"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommandapplicationhostenvironment"><strong>IExecuteCommandApplicationHostEnvironment</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-333">提供單一方法，可讓應用程式判斷其主機是否為桌面或沉浸式模式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-333">Provides a single method that enables an application to determine whether its host is in desktop or immersive mode.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-334"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommandhost"><strong>IExecuteCommandHost</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-334"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommandhost"><strong>IExecuteCommandHost</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-335">提供方法，可讓以 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a>為基礎的 Shell 動詞命令處理常式查詢叫用應用程式的主控制群組件的 UI 模式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-335">Provides a method that enables an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a>-based Shell verb handler to query the UI mode of the host component from which the application was invoked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-336"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser"><strong>IExplorerBrowser</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-336"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser"><strong>IExplorerBrowser</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-337"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser"><strong>IExplorerBrowser</strong></a> 是瀏覽器物件，可以導覽或可裝載資料物件的視圖。</span><span class="sxs-lookup"><span data-stu-id="71ab3-337"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser"><strong>IExplorerBrowser</strong></a> is a browser object that can be either navigated or that can host a view of a data object.</span></span> <span data-ttu-id="71ab3-338">它是功能完整的瀏覽器物件，它也支援自動移動記錄檔。</span><span class="sxs-lookup"><span data-stu-id="71ab3-338">As a full-featured browser object, it also supports an automatic travel log.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-339"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowserevents"><strong>IExplorerBrowserEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-339"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowserevents"><strong>IExplorerBrowserEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-340">公開 Explorer 瀏覽器流覽和觀看建立事件的通知方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-340">Exposes methods for notification of Explorer browser navigation and view creation events.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-341"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-341"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-342">公開取得命令外觀、列舉子命令或叫用命令的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-342">Exposes methods that get the command appearance, enumerate subcommands, or invoke the command.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-343"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-343"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-344">公開方法來建立瀏覽器命令和命令列舉值。</span><span class="sxs-lookup"><span data-stu-id="71ab3-344">Exposes methods to create Explorer commands and command enumerators.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-345"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate"><strong>IExplorerCommandState</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-345"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate"><strong>IExplorerCommandState</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-346">公開允許抓取命令狀態的單一方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-346">Exposes a single method that allows retrieval of the command state.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-347"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility"><strong>IExplorerPaneVisibility</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-347"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility"><strong>IExplorerPaneVisibility</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-348">用於 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> 的執行 Windows 檔案總管，以提供有關可見窗格的建議。</span><span class="sxs-lookup"><span data-stu-id="71ab3-348">Used in Windows Explorer by an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> implementation to give suggestions to the view about what panes are visible.</span></span> <span data-ttu-id="71ab3-349">此外， <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser"><strong>IExplorerBrowser</strong></a> 主控制項可以使用這個介面來提供有關窗格可見度的資訊。</span><span class="sxs-lookup"><span data-stu-id="71ab3-349">Additionally, an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser"><strong>IExplorerBrowser</strong></a> host can use this interface to provide information about pane visibility.</span></span> <span data-ttu-id="71ab3-350">主機應該使用<strong>SID_ExplorerPaneVisibility</strong>作為服務識別碼來執行<a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="71ab3-350">The host should implement <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a> with <strong>SID_ExplorerPaneVisibility</strong> as the service ID.</span></span> <span data-ttu-id="71ab3-351">主機必須在網站鏈中。</span><span class="sxs-lookup"><span data-stu-id="71ab3-351">The host must be in the site chain.</span></span> <br/> <span data-ttu-id="71ab3-352">從 Shell 資料夾抓取 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility"><strong>IExplorerPaneVisibility</strong></a> 的執行。</span><span class="sxs-lookup"><span data-stu-id="71ab3-352">The <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility"><strong>IExplorerPaneVisibility</strong></a> implementation is retrieved from the Shell folder.</span></span> <span data-ttu-id="71ab3-353">然後，Shell 資料夾會從 view 中取出。</span><span class="sxs-lookup"><span data-stu-id="71ab3-353">The Shell folder, in turn, is retrieved from the view.</span></span> <span data-ttu-id="71ab3-354">命名空間延伸可以選擇提供自訂視圖 (<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a>) ，而不是使用系統資料夾 view 物件 (DefView) 。</span><span class="sxs-lookup"><span data-stu-id="71ab3-354">A namespace extension can elect to provide a custom view (<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a>) rather than using the system folder view object (DefView).</span></span> <span data-ttu-id="71ab3-355">在這種情況下， <strong>IShellView</strong> 的執行必須包含 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getfolder"><strong>IFolderView：： GetFolder</strong></a> 的執行，以傳回 <strong>IExplorerPaneVisibility</strong> 物件。</span><span class="sxs-lookup"><span data-stu-id="71ab3-355">In that case, the <strong>IShellView</strong> implementation must include an implementation of <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getfolder"><strong>IFolderView::GetFolder</strong></a> to return the <strong>IExplorerPaneVisibility</strong> object.</span></span><br/> <span data-ttu-id="71ab3-356">命名空間延伸模組可以藉由實 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a> 本身來提供自訂視圖，而不是使用系統資料夾 view 物件 (DefView) 。</span><span class="sxs-lookup"><span data-stu-id="71ab3-356">A namespace extension can provide a custom view by implementing <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a> itself rather than using the system folder view object (DefView).</span></span> <span data-ttu-id="71ab3-357">在此情況下， <strong>IShellView</strong> 的執行必須包含 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getfolder"><strong>IFolderView：： GetFolder</strong></a> 的實作為使用 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility"><strong>IExplorerPaneVisibility</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="71ab3-357">In that case, the <strong>IShellView</strong> implementation must include an implementation of <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getfolder"><strong>IFolderView::GetFolder</strong></a> to make use of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility"><strong>IExplorerPaneVisibility</strong></a> .</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-358"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona"><strong>IExtractIcon</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-358"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona"><strong>IExtractIcon</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-359">公開方法，以允許用戶端取得與資料夾中其中一個物件相關聯的圖示。</span><span class="sxs-lookup"><span data-stu-id="71ab3-359">Exposes methods that allow a client to retrieve the icon that is associated with one of the objects in a folder.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-360"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage"><strong>IExtractImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-360"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage"><strong>IExtractImage</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-361">公開從 Shell 資料夾要求縮圖影像的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-361">Exposes methods that request a thumbnail image from a Shell folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-362"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2"><strong>IExtractImage2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-362"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2"><strong>IExtractImage2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-363">擴充 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage"><strong>IExtractImage</strong></a>的功能。</span><span class="sxs-lookup"><span data-stu-id="71ab3-363">Extends the capabilities of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage"><strong>IExtractImage</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-364"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-364"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-365">公開從 [一般檔案] 對話方塊初始化、顯示和取得結果的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-365">Exposes methods that initialize, show, and get results from the common file dialog.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-366"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialog2"><strong>IFileDialog2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-366"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialog2"><strong>IFileDialog2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-367">藉由提供方法，讓呼叫端命名可在 [一般檔案] 對話方塊中流覽的特定、受限位置，以及指定要在 [<strong>取消</strong>] 按鈕上顯示為標籤的替代文字，來擴充<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a>介面。</span><span class="sxs-lookup"><span data-stu-id="71ab3-367">Extends the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a> interface by providing methods that allow the caller to name a specific, restricted location that can be browsed in the common file dialog as well as to specify alternate text to display as a label on the <strong>Cancel</strong> button.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-368"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents"><strong>IFileDialogControlEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-368"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents"><strong>IFileDialogControlEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-369">公開方法，這些方法可讓應用程式收到事件的通知，這些事件與應用程式已新增至一般檔案對話方塊的控制項相關。</span><span class="sxs-lookup"><span data-stu-id="71ab3-369">Exposes methods that allow an application to be notified of events that are related to controls that the application has added to a common file dialog.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-370"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize"><strong>IFileDialogCustomize</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-370"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize"><strong>IFileDialogCustomize</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-371">公開可讓應用程式將控制項加入至一般檔案對話方塊的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-371">Exposes methods that allow an application to add controls to a common file dialog.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-372"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents"><strong>IFileDialogEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-372"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents"><strong>IFileDialogEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-373">公開允許一般檔案對話方塊內的事件通知的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-373">Exposes methods that allow notification of events within a common file dialog.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-374"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileisinuse"><strong>IFileIsInUse</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-374"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileisinuse"><strong>IFileIsInUse</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-375">公開可呼叫的方法，以取得或關閉另一個應用程式正在使用的檔案的資訊。</span><span class="sxs-lookup"><span data-stu-id="71ab3-375">Exposes methods that can be called to get information on or close a file that is in use by another application.</span></span> <span data-ttu-id="71ab3-376">當應用程式嘗試存取檔案，並找到已在使用中的檔案時，可以使用這個介面的方法，在對話方塊中收集要呈現給使用者的資訊。</span><span class="sxs-lookup"><span data-stu-id="71ab3-376">When an application attempts to access a file and finds that file already in use, it can use the methods of this interface to gather information to present to the user in a dialog box.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-377"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog"><strong>IFileOpenDialog</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-377"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog"><strong>IFileOpenDialog</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-378">藉由新增 [開啟] 對話方塊專屬的方法來擴充 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a> 介面。</span><span class="sxs-lookup"><span data-stu-id="71ab3-378">Extends the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a> interface by adding methods specific to the open dialog.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-379"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-379"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-380">公開方法來複製、移動、重新命名、建立及刪除 Shell 專案以及提供進度和錯誤對話方塊的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-380">Exposes methods to copy, move, rename, create, and delete Shell items as well as methods to provide progress and error dialogs.</span></span> <span data-ttu-id="71ab3-381">這個介面會取代 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-381">This interface replaces the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-382"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink"><strong>IFileOperationProgressSink</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-382"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink"><strong>IFileOperationProgressSink</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-383">公開方法，以提供 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a> 呼叫端所使用的豐富通知系統，來監視透過該介面所執行之作業的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="71ab3-383">Exposes methods that provide a rich notification system used by callers of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a> to monitor the details of the operations they are performing through that interface.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-384"><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog"><strong>IFileSaveDialog</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-384"><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog"><strong>IFileSaveDialog</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-385">藉由新增 [儲存] 對話方塊專屬的方法來擴充 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a> 介面，其中包括支援要與檔案保存之元資料集合的支援。</span><span class="sxs-lookup"><span data-stu-id="71ab3-385">Extends the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a> interface by adding methods specific to the save dialog, which include those that provide support for the collection of metadata to be persisted with the file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-386"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesyncmergehandler"><strong>IFileSyncMergeHandler</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-386"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesyncmergehandler"><strong>IFileSyncMergeHandler</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-387"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>IFileSystemBindData</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-387"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>IFileSystemBindData</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-388">公開儲存檔案系統資訊的方法，以優化對 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder 的呼叫：:P arsedisplayname</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="71ab3-388">Exposes methods that store file system information for optimizing calls to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::ParseDisplayName</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-389"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata2"><strong>IFileSystemBindData2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-389"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata2"><strong>IFileSystemBindData2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-390">擴充 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>IFileSystemBindData</strong></a>，它會儲存檔案系統資訊，以優化對 IShellFolder 的呼叫 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>：:P arsedisplayname</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="71ab3-390">Extends <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>IFileSystemBindData</strong></a>, which stores file system information for optimizing calls to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::ParseDisplayName</strong></a>.</span></span> <span data-ttu-id="71ab3-391">這個介面會將設定的功能，或取得檔案識別碼或連接類別識別碼 (CLSID) 。</span><span class="sxs-lookup"><span data-stu-id="71ab3-391">This interface adds the ability set or get file ID or junction class identifier (CLSID).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-392"><a href="/windows/desktop/shell/schema-library-iconreference"><strong>IFileViewer</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-392"><a href="/windows/desktop/shell/schema-library-iconreference"><strong>IFileViewer</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-393">公開方法，這些方法會指定介面，讓註冊的檔案檢視器必須顯示或列印檔案時，才會收到通知。</span><span class="sxs-lookup"><span data-stu-id="71ab3-393">Exposes methods that designate an interface that allows a registered file viewer to be notified when it must show or print a file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-394"><a href="/windows/desktop/api/shlobj/nn-shlobj-ifileviewersite"><strong>IFileViewerSite</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-394"><a href="/windows/desktop/api/shlobj/nn-shlobj-ifileviewersite"><strong>IFileViewerSite</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-395">公開方法，以指定允許檔案檢視器抓取目前釘選視窗控制碼的介面，或設定新的固定視窗。</span><span class="sxs-lookup"><span data-stu-id="71ab3-395">Exposes methods that designate an interface that allows a file viewer to retrieve the handle to the current pinned window, or to set a new pinned window.</span></span> <span data-ttu-id="71ab3-396">固定的視窗是目前檔案檢視器顯示檔案的視窗。</span><span class="sxs-lookup"><span data-stu-id="71ab3-396">The pinned window is the window in which the current file viewer displays a file.</span></span> <span data-ttu-id="71ab3-397">當使用者選取要查看的新檔案時，命令介面會指示檔案檢視器在釘選的視窗中顯示新檔案，而不是建立新的視窗。</span><span class="sxs-lookup"><span data-stu-id="71ab3-397">When the user selects a new file to view, the Shell directs the file viewer to display the new file in the pinned window rather than create a new window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-398"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfilter"><strong>IFolderFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-398"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfilter"><strong>IFolderFilter</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-399">由用戶端公開，以指定如何透過伺服器應用程式篩選 Shell 資料夾的列舉。</span><span class="sxs-lookup"><span data-stu-id="71ab3-399">Exposed by a client to specify how to filter the enumeration of a Shell folder by a server application.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-400"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfiltersite"><strong>IFolderFilterSite</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-400"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfiltersite"><strong>IFolderFilterSite</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-401">由主機匯出，以允許用戶端指定如何篩選 Shell 資料夾列舉。</span><span class="sxs-lookup"><span data-stu-id="71ab3-401">Exported by a host to allow clients to specify how to filter a Shell folder enumeration.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-402"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview"><strong>IFolderView</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-402"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview"><strong>IFolderView</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-403">公開方法，以取得資料夾顯示選項的相關資訊、選取該資料夾中的指定專案，以及設定資料夾的視圖模式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-403">Exposes methods that retrieve information about a folder's display options, select specified items in that folder, and set the folder's view mode.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-404"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview2"><strong>IFolderView2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-404"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview2"><strong>IFolderView2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-405">公開方法，以取得資料夾顯示選項的相關資訊、選取該資料夾中的指定專案，以及設定資料夾的視圖模式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-405">Exposes methods that retrieve information about a folder's display options, select specified items in that folder, and set the folder's view mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-406"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifolderviewhost"><strong>IFolderViewHost</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-406"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifolderviewhost"><strong>IFolderViewHost</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-407">公開在視窗中裝載 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview"><strong>IFolderView</strong></a> 物件的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-407">Exposes a method that hosts an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview"><strong>IFolderView</strong></a> object in a window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-408"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifolderviewoptions"><strong>IFolderViewOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-408"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifolderviewoptions"><strong>IFolderViewOptions</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-409">公開方法，以允許控制 Windows 7 和更新版本的特定資料夾檢視選項。</span><span class="sxs-lookup"><span data-stu-id="71ab3-409">Exposes methods that allow control of folder view options specific to the Windows 7 and later views.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-410"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderviewsettings"><strong>IFolderViewSettings</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-410"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderviewsettings"><strong>IFolderViewSettings</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-411">公開取得資料夾檢視設定的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-411">Exposes methods to obtain folder view settings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-412"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iframeworkinputpane"><strong>IFrameworkInputPane</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-412"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iframeworkinputpane"><strong>IFrameworkInputPane</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-413">提供的方法可讓應用程式知道狀態變更和輸入窗格的位置。</span><span class="sxs-lookup"><span data-stu-id="71ab3-413">Provides methods that enable apps to be informed of state changes and location for the input pane.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-414"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iframeworkinputpanehandler"><strong>IFrameworkInputPaneHandler</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-414"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iframeworkinputpanehandler"><strong>IFrameworkInputPaneHandler</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-415">可讓應用程式在顯示或隱藏 [螢幕小鍵盤] 或 [手寫面板]) 的輸入窗格 (時收到通知。</span><span class="sxs-lookup"><span data-stu-id="71ab3-415">Enables an app to be notified when the input pane (the on-screen keyboard or handwriting panel) is being shown or hidden.</span></span> <span data-ttu-id="71ab3-416">這可讓應用程式視窗調整其顯示，如此一來，輸入窗格就不會 (例如文字方塊) 的輸入區域。</span><span class="sxs-lookup"><span data-stu-id="71ab3-416">This allows the app window to adjust its display so that no input areas (such as a text box) are obscured by the input pane.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-417"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandleractivationhost"><strong>IHandlerActivationHost</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-417"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandleractivationhost"><strong>IHandlerActivationHost</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-418"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandlerinfo"><strong>IHandlerInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-418"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandlerinfo"><strong>IHandlerInfo</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-419">提供方法，提供 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandleractivationhost"><strong>IHandlerActivationHost</strong></a> 介面方法的處理常式相關資訊。</span><span class="sxs-lookup"><span data-stu-id="71ab3-419">Supplies methods that provide information about the handler to methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandleractivationhost"><strong>IHandlerActivationHost</strong></a> interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-420"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihomegroup"><strong>IHomeGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-420"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihomegroup"><strong>IHomeGroup</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-421">公開決定電腦的家用電腦成員資格狀態，並顯示共用嚮導的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-421">Exposes methods that determine a computer's HomeGroup membership status and display the sharing wizard.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-422"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler"><strong>IHWEventHandler</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-422"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler"><strong>IHWEventHandler</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-423">由自動播放呼叫以執行已註冊媒體類型的處理。</span><span class="sxs-lookup"><span data-stu-id="71ab3-423">Called by AutoPlay to implement the handling of registered media types.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-424"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler2"><strong>IHWEventHandler2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-424"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler2"><strong>IHWEventHandler2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-425">擴充 <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler"><strong>IHWEventHandler</strong></a> 介面，以處理使用者帳戶控制 (UAC) 提高裝置處理常式的許可權。</span><span class="sxs-lookup"><span data-stu-id="71ab3-425">Extends the <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler"><strong>IHWEventHandler</strong></a> interface to address User Account Control (UAC) elevation for device handlers.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-426"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iidentityname"><strong>IIdentityName</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-426"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iidentityname"><strong>IIdentityName</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-427">公開方法來比較兩個專案，看看它們是否相同。</span><span class="sxs-lookup"><span data-stu-id="71ab3-427">Exposes methods to compare two items to see if they are the same.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-428"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iimagerecompress"><strong>IImageRecompress</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-428"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iimagerecompress"><strong>IImageRecompress</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-429">公開重新壓縮影像的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-429">Exposes a method that recompress images.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-430"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-430"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-431">公開用來初始化物件的單一方法，該物件會使用應用程式指定的命令名稱及其註冊的屬性來執行 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate"><strong>IExplorerCommandState</strong></a>、 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> 或 <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="71ab3-431">Exposes a single method used to initialize objects that implement <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate"><strong>IExplorerCommandState</strong></a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> or <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> with the application-specified command name and its registered properties.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-432"><a href="/windows/win32/api/shobjidl/nn-shobjidl-iinitializenetworkfolder"><strong>IInitializeNetworkFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-432"><a href="/windows/win32/api/shobjidl/nn-shobjidl-iinitializenetworkfolder"><strong>IInitializeNetworkFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-433">公開初始化網路資料來源 CLSID_NetworkPlaces （如指定）的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-433">Exposes a method that initializes the network data source CLSID_NetworkPlaces as specified.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-434"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithbindctx"><strong>IInitializeWithBindCtx</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-434"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithbindctx"><strong>IInitializeWithBindCtx</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-435">公開使用系結內容初始化處理常式的方法，例如屬性處理常式、縮圖處理常式或預覽處理常式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-435">Exposes a method that initializes a handler, such as a property handler, thumbnail handler, or preview handler, with a bind context.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-436"><a href="/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile"><strong>IInitializeWithFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-436"><a href="/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile"><strong>IInitializeWithFile</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-437">公開方法，以使用檔案路徑初始化處理常式，例如屬性處理常式、縮圖處理常式或預覽處理常式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-437">Exposes a method to initialize a handler, such as a property handler, thumbnail handler, or preview handler, with a file path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-438"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem"><strong>IInitializeWithItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-438"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem"><strong>IInitializeWithItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-439">使用 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>公開用來初始化處理常式的方法，例如屬性處理常式、縮圖處理常式或預覽處理常式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-439">Exposes a method used to initialize a handler, such as a property handler, thumbnail handler, or preview handler, with an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-440"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithpropertystore"><strong>IInitializeWithPropertyStore</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-440"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithpropertystore"><strong>IInitializeWithPropertyStore</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-441">公開以屬性存放區初始化處理常式的方法，例如屬性處理常式、縮圖處理常式或預覽處理常式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-441">Exposes a method that initializes a handler, such as a property handler, thumbnail handler, or preview handler, with a property store.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-442"><a href="/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream"><strong>IInitializeWithStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-442"><a href="/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream"><strong>IInitializeWithStream</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-443">公開使用資料流程初始化處理常式的方法，例如屬性處理常式、縮圖處理常式或預覽處理常式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-443">Exposes a method that initializes a handler, such as a property handler, thumbnail handler, or preview handler, with a stream.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-444"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithwindow"><strong>IInitializeWithWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-444"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithwindow"><strong>IInitializeWithWindow</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-445">公開一種方法，用戶端可以透過此方法將擁有者視窗提供給桌面應用程式中所使用的 Windows 執行階段物件。</span><span class="sxs-lookup"><span data-stu-id="71ab3-445">Exposes a method through which a client can provide an owner window to a Windows Runtime object used in a desktop application.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-446"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobject"><strong>IInputObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-446"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobject"><strong>IInputObject</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-447">公開方法，以變更 Shell 中所含使用者輸入物件的 UI 啟用和流程加速器。</span><span class="sxs-lookup"><span data-stu-id="71ab3-447">Exposes methods that change UI activation and process accelerators for a user input object contained in the Shell.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-448"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobject2"><strong>IInputObject2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-448"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobject2"><strong>IInputObject2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-449">公開透過處理全域快速鍵來擴充 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobject"><strong>IInputObject</strong></a> 的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-449">Exposes a method that extends <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobject"><strong>IInputObject</strong></a> by handling global accelerators.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-450"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite"><strong>IInputObjectSite</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-450"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite"><strong>IInputObjectSite</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-451">公開方法，這個方法用來針對 Shell 中包含的使用者輸入物件傳達焦點變更。</span><span class="sxs-lookup"><span data-stu-id="71ab3-451">Exposes a method that is used to communicate focus changes for a user input object contained in the Shell.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-452"><a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration"><strong>IInputPanelConfiguration</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-452"><a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration"><strong>IInputPanelConfiguration</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-453">提供適用于桌面應用程式的功能，以加入宣告 Windows Store 應用程式中使用的焦點追蹤機制。</span><span class="sxs-lookup"><span data-stu-id="71ab3-453">Provides functionality for desktop apps to opt in to the focus tracking mechanism used in Windows Store apps.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-454"><a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelinvocationconfiguration"><strong>IInputPanelInvocationConfiguration</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-454"><a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelinvocationconfiguration"><strong>IInputPanelInvocationConfiguration</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-455">讓 Windows Store 應用程式退出自動調用行為。</span><span class="sxs-lookup"><span data-stu-id="71ab3-455">Enables Windows Store apps to opt out of the automatic invocation behavior.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-456"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iiocancelinformation"><strong>IIOCancelInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-456"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iiocancelinformation"><strong>IIOCancelInformation</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-457">公開從進度對話方塊將取消視窗訊息張貼至進程執行緒的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-457">Exposes methods for posting a cancel window message to the process thread from the Progress Dialog.</span></span> <br/> <span data-ttu-id="71ab3-458">此介面可讓進度對話方塊透過 <a href="/windows/desktop/api/winuser/nf-winuser-postthreadmessagea"><strong>PostThreadMessage</strong></a> 將執行緒訊息張貼至背景工作執行緒，以取消其作業。</span><span class="sxs-lookup"><span data-stu-id="71ab3-458">This interface enables the progress dialog to post a thread message through <a href="/windows/desktop/api/winuser/nf-winuser-postthreadmessagea"><strong>PostThreadMessage</strong></a> to the worker thread to cancel its operations.</span></span> <span data-ttu-id="71ab3-459">背景工作執行緒必須透過 <a href="/windows/desktop/api/winuser/nf-winuser-getmessage"><strong>GetMessage</strong></a>、 <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea"><strong>PeekMessage</strong></a> 或 <a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex"><strong>MsgWaitForMultipleObjectsEx</strong></a>定期檢查訊息佇列。</span><span class="sxs-lookup"><span data-stu-id="71ab3-459">The worker thread must periodically check the message queue through <a href="/windows/desktop/api/winuser/nf-winuser-getmessage"><strong>GetMessage</strong></a>, <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea"><strong>PeekMessage</strong></a> or <a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex"><strong>MsgWaitForMultipleObjectsEx</strong></a>.</span></span><br/> <span data-ttu-id="71ab3-460"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iiocancelinformation-setcancelinformation"><strong>IIOCancelInformation：： SetCancelInformation</strong></a>方法會告知進度對話方塊，在使用者按一下 [<strong>取消</strong>] 時，執行緒識別碼和要<a href="/windows/desktop/api/winuser/nf-winuser-postthreadmessagea"><strong>PostThreadMessage</strong></a>的訊息。</span><span class="sxs-lookup"><span data-stu-id="71ab3-460">The <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iiocancelinformation-setcancelinformation"><strong>IIOCancelInformation::SetCancelInformation</strong></a> method tells the progress dialog which thread ID and what message to <a href="/windows/desktop/api/winuser/nf-winuser-postthreadmessagea"><strong>PostThreadMessage</strong></a> when the user clicks <strong>Cancel</strong>.</span></span> <span data-ttu-id="71ab3-461">執行緒識別碼為 &quot; 零會 &quot; 停用取消訊息的傳送作業。</span><span class="sxs-lookup"><span data-stu-id="71ab3-461">A thread ID of &quot;zero&quot; disables the sending operation for the cancel message.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-462"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iitemnamelimits"><strong>IItemNameLimits</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-462"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iitemnamelimits"><strong>IItemNameLimits</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-463">抓取命名空間中有效和不正確字元清單，或名稱的最大長度。</span><span class="sxs-lookup"><span data-stu-id="71ab3-463">Retrieves a list of valid and invalid characters or the maximum length of a name in the namespace.</span></span> <span data-ttu-id="71ab3-464">使用這個介面進行驗證剖析和轉譯。</span><span class="sxs-lookup"><span data-stu-id="71ab3-464">Use this interface for validation parsing and translation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-465"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder"><strong>IKnownFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-465"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder"><strong>IKnownFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-466">公開方法，讓應用程式取得已知資料夾的類別、類型、GUID、PIDL 值、重新導向功能和定義的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="71ab3-466">Exposes methods that allow an application to retrieve information about a known folder's category, type, GUID, PIDL value, redirection capabilities, and definition.</span></span> <span data-ttu-id="71ab3-467">它提供擷取已知資料夾 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> 物件的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-467">It provides a method for the retrival of a known folder's <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> object.</span></span> <span data-ttu-id="71ab3-468">它也提供方法來取得或設定已知資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="71ab3-468">It also provides methods to get or set the path of the known folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-469"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager"><strong>IKnownFolderManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-469"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager"><strong>IKnownFolderManager</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-470">公開方法，以建立、列舉或管理現有的已知資料夾。</span><span class="sxs-lookup"><span data-stu-id="71ab3-470">Exposes methods that create, enumerate or manage existing known folders.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-471"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchsourceappusermodelid"><strong>ILaunchSourceAppUserModelId</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-471"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchsourceappusermodelid"><strong>ILaunchSourceAppUserModelId</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-472">提供用來取得 <a href="appids.md">AppUserModelId</a>的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-472">Provides a method for retrieving an <a href="appids.md">AppUserModelId</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-473"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchsourceviewsizepreference"><strong>ILaunchSourceViewSizePreference</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-473"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchsourceviewsizepreference"><strong>ILaunchSourceViewSizePreference</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-474">提供用來取得來源應用程式相關資訊的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-474">Provides methods for retrieving information about the source application.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-475"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchtargetmonitor"><strong>ILaunchTargetMonitor</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-475"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchtargetmonitor"><strong>ILaunchTargetMonitor</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-476"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchtargetviewsizepreference"><strong>ILaunchTargetViewSizePreference</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-476"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchtargetviewsizepreference"><strong>ILaunchTargetViewSizePreference</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-477">提供方法來為新的應用程式視窗抓取慣用的視圖大小。</span><span class="sxs-lookup"><span data-stu-id="71ab3-477">Provides a method for retrieving the preferred view size for a new application window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-478"><a href="/windows/desktop/shell/shell-extensibility-bumper"><strong>IMarkupCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-478"><a href="/windows/desktop/shell/shell-extensibility-bumper"><strong>IMarkupCallback</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-479"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imenupopup"><strong>IMenuPopup</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-479"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imenupopup"><strong>IMenuPopup</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-480"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imenupopup"><strong>IMenuPopup</strong></a> 可能已變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="71ab3-480"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imenupopup"><strong>IMenuPopup</strong></a> may be altered or unavailable.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-481"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow"><strong>IModalWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-481"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow"><strong>IModalWindow</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-482">公開表示強制回應視窗的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-482">Exposes a method that represents a modal window.</span></span> <span data-ttu-id="71ab3-483">此介面是在 Windows XP Passport Wizard 中使用。</span><span class="sxs-lookup"><span data-stu-id="71ab3-483">This interface is used in the Windows XP Passport Wizard.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-484"><a href="imultimonitordockingsite.md"><strong>IMultiMonitorDockingSite</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-484"><a href="imultimonitordockingsite.md"><strong>IMultiMonitorDockingSite</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-485">由瀏覽器所執行。</span><span class="sxs-lookup"><span data-stu-id="71ab3-485">Implemented by the browser.</span></span> <span data-ttu-id="71ab3-486">公開管理哪些監視在多個監視器系統上包含 Windows 工作列的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-486">Exposes methods that manage which monitor contains the Windows taskbar on a multiple monitor system.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-487"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-inamedpropertybag"><strong>INamedPropertyBag</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-487"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-inamedpropertybag"><strong>INamedPropertyBag</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-488">公開方法，這些方法會提供具有指定屬性包的物件，而物件可以在其中儲存其屬性。</span><span class="sxs-lookup"><span data-stu-id="71ab3-488">Exposes methods that provide an object with a specified property bag in which the object can save its properties.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-489"><a href="/windows/desktop/api/Propsys/nn-propsys-inamedpropertystore"><strong>INamedPropertyStore</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-489"><a href="/windows/desktop/api/Propsys/nn-propsys-inamedpropertystore"><strong>INamedPropertyStore</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-490">公開取得和設定命名屬性的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-490">Exposes methods that get and set named properties.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-491"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreeaccessible"><strong>INameSpaceTreeAccessible</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-491"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreeaccessible"><strong>INameSpaceTreeAccessible</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-492">公開方法，以從命名空間樹狀目錄控制項執行 Shell 專案的協助工具動作。</span><span class="sxs-lookup"><span data-stu-id="71ab3-492">Exposes methods that perform accessibility actions on a Shell item from a namespace tree control.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-493"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>INameSpaceTreeControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-493"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>INameSpaceTreeControl</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-494">公開用來在 Shell 專案樹狀結構中，用來查看和操作節點的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-494">Exposes methods used to view and manipulate nodes in a tree of Shell items.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-495"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrol2"><strong>INameSpaceTreeControl2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-495"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrol2"><strong>INameSpaceTreeControl2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-496">藉由提供取得和設定 treeview 控制項顯示樣式的方法來擴充 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>INameSpaceTreeControl</strong></a> 介面，以搭配 Shell 命名空間專案使用。</span><span class="sxs-lookup"><span data-stu-id="71ab3-496">Extends the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>INameSpaceTreeControl</strong></a> interface by providing methods that get and set the display styles of treeview controls for use with Shell namespace items.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-497"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw"><strong>INameSpaceTreeControlCustomDraw</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-497"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw"><strong>INameSpaceTreeControlCustomDraw</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-498">公開方法，讓使用者能夠繪製自訂命名空間樹狀結構控制項和其專案。</span><span class="sxs-lookup"><span data-stu-id="71ab3-498">Exposes methods that enable the user to draw a custom namespace tree control and its items.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-499"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontroldrophandler"><strong>INameSpaceTreeControlDropHandler</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-499"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontroldrophandler"><strong>INameSpaceTreeControlDropHandler</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-500">公開拖放的處理常式方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-500">Exposes handler methods for drag-and-drop.</span></span> <span data-ttu-id="71ab3-501">由命名空間樹狀目錄控制項用來通知用戶端在控制項中發生的任何拖放作業。</span><span class="sxs-lookup"><span data-stu-id="71ab3-501">Used by the namespace tree control to notify the client of any drag-and-drop operation happening within the control.</span></span> <span data-ttu-id="71ab3-502">提供一種方式，讓用戶端攔截卸載作業並執行自己的動作，或傳回所需的卸載效果。</span><span class="sxs-lookup"><span data-stu-id="71ab3-502">Provides a way for a client to intercept a drop operation and perform its own action, or to return the desired drop effect.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-503"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolevents"><strong>INameSpaceTreeControlEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-503"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolevents"><strong>INameSpaceTreeControlEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-504">公開處理 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>INameSpaceTreeControl</strong></a> 事件的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-504">Exposes methods for handling <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>INameSpaceTreeControl</strong></a> events.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-505"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrolfoldercapabilities"><strong>INameSpaceTreeControlFolderCapabilities</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-505"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrolfoldercapabilities"><strong>INameSpaceTreeControlFolderCapabilities</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-506">公開單一方法，以抓取資料夾系統的狀態 <a href="/windows/desktop/properties/props-system-ispinnedtonamespacetree">。 IsPinnedToNameSpaceTree</a> 篩選支援。</span><span class="sxs-lookup"><span data-stu-id="71ab3-506">Exposes a single method that retrieves the status of a folder's <a href="/windows/desktop/properties/props-system-ispinnedtonamespacetree">System.IsPinnedToNameSpaceTree</a> filtering support.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-507"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalk"><strong>INamespaceWalk</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-507"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalk"><strong>INamespaceWalk</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-508">公開方法，以從指定的根節點引導命名空間。</span><span class="sxs-lookup"><span data-stu-id="71ab3-508">Exposes methods that walk a namespace from a given root node.</span></span> <span data-ttu-id="71ab3-509">系統會指定此逐步解說的深度，並傳回包含所有已行走節點之識別碼的選擇性陣列。</span><span class="sxs-lookup"><span data-stu-id="71ab3-509">The depth of the walk is specified and an optional array is returned containing the IDs of all nodes walked.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-510"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb"><strong>INamespaceWalkCB</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-510"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb"><strong>INamespaceWalkCB</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-511">回呼介面，此介面會公開與 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalk"><strong>INamespaceWalk</strong></a>搭配使用的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-511">A callback interface exposing methods used with <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalk"><strong>INamespaceWalk</strong></a>.</span></span> <span data-ttu-id="71ab3-512">使用 <strong>INamespaceWalk</strong>執行「逐步解說」之後，代表已執行之節點的 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> 物件會傳遞至 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb"><strong>INamespaceWalkCB</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-512">After performing a walk with <strong>INamespaceWalk</strong>, an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> object representing the walked nodes is passed to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb"><strong>INamespaceWalkCB</strong></a> methods.</span></span> <span data-ttu-id="71ab3-513">這些方法對資訊有何用途取決於正在執行的物件。</span><span class="sxs-lookup"><span data-stu-id="71ab3-513">What those methods do with the information depends on the object that is implementing them.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-514"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb2"><strong>INamespaceWalkCB2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-514"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb2"><strong>INamespaceWalkCB2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-515">使用需要的方法來擴充 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb"><strong>INamespaceWalkCB</strong></a> ，才能完成命名空間的逐步解說。</span><span class="sxs-lookup"><span data-stu-id="71ab3-515">Extends <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb"><strong>INamespaceWalkCB</strong></a> with a method that is required in order to complete a namespace walk.</span></span> <span data-ttu-id="71ab3-516">這個方法會移除在此逐步解說中所收集的資料。</span><span class="sxs-lookup"><span data-stu-id="71ab3-516">This method removes data collected during the walk.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-517"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inewmenuclient"><strong>INewMenuClient</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-517"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inewmenuclient"><strong>INewMenuClient</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-518">公開允許操作 Windows 7 功能表中專案的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-518">Exposes methods that allow manipulation of items in a Windows 7 menu.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-519"><a href="/windows/desktop/api/shlobj/nn-shlobj-inewshortcuthooka"><strong>INewShortcutHook</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-519"><a href="/windows/desktop/api/shlobj/nn-shlobj-inewshortcuthooka"><strong>INewShortcutHook</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-520">公開方法以建立新的網際網路快捷方式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-520">Exposes methods to create a new Internet shortcut.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-521"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inewwindowmanager"><strong>INewWindowManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-521"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inewwindowmanager"><strong>INewWindowManager</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-522">公開方法，這個方法會判斷是否應顯示或封鎖由另一個視窗啟動的視窗，以允許控制項快顯視窗。</span><span class="sxs-lookup"><span data-stu-id="71ab3-522">Exposes a method that determines whether a window that is launched by another window should be displayed or blocked, allowing control of pop-up windows.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-523"><a href="/windows/desktop/api/reconcil/nn-reconcil-inotifyreplica"><strong>INotifyReplica</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-523"><a href="/windows/desktop/api/reconcil/nn-reconcil-inotifyreplica"><strong>INotifyReplica</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-524">公開方法，該方法會提供物件的建立者，其方法為通知物件可能會受到後續的對帳。</span><span class="sxs-lookup"><span data-stu-id="71ab3-524">Exposes a method that provides an object's creator with the means to notify the object that it may be subject to subsequent reconciliation.</span></span> <span data-ttu-id="71ab3-525">公事包調整器負責執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="71ab3-525">The briefcase reconciler is responsible for implementing this interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-526"><a href="/windows/desktop/api/Objectarray/nn-objectarray-iobjectarray"><strong>IObjectArray</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-526"><a href="/windows/desktop/api/Objectarray/nn-objectarray-iobjectarray"><strong>IObjectArray</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-527">公開方法，這些方法可讓用戶端存取支援 <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>的物件集合中的專案。</span><span class="sxs-lookup"><span data-stu-id="71ab3-527">Exposes methods that enable clients to access items in a collection of objects that support <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-528"><a href="/windows/desktop/api/objectarray/nn-objectarray-iobjectcollection"><strong>IObjectCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-528"><a href="/windows/desktop/api/objectarray/nn-objectarray-iobjectcollection"><strong>IObjectCollection</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-529">藉由提供可讓用戶端加入和移除集合中支援<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>之物件的方法，來擴充<a href="/windows/desktop/api/Objectarray/nn-objectarray-iobjectarray"><strong>IObjectArray</strong></a>介面。</span><span class="sxs-lookup"><span data-stu-id="71ab3-529">Extends the <a href="/windows/desktop/api/Objectarray/nn-objectarray-iobjectarray"><strong>IObjectArray</strong></a> interface by providing methods that enable clients to add and remove objects that support <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> in a collection.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-530"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectprovider"><strong>IObjectProvider</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-530"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectprovider"><strong>IObjectProvider</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-531">公開方法，以探索以另一個物件的 <strong>GUID</strong> 命名的物件。</span><span class="sxs-lookup"><span data-stu-id="71ab3-531">Exposes a method to discover objects that are named with a <strong>GUID</strong> from another object.</span></span> <span data-ttu-id="71ab3-532">不同于 <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a> ，此介面不會將其功能委派給其他物件。</span><span class="sxs-lookup"><span data-stu-id="71ab3-532">Unlike <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a> this interface will not delegate its functionality on to other objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-533"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithappusermodelid"><strong>IObjectWithAppUserModelID</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-533"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithappusermodelid"><strong>IObjectWithAppUserModelID</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-534">公開方法，以允許自訂 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler"><strong>IAssocHandler</strong></a> 物件的實作者提供其明確應用程式使用者模型識別碼的存取 (AppUserModelID) 。</span><span class="sxs-lookup"><span data-stu-id="71ab3-534">Exposes methods that allow implementers of a custom <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler"><strong>IAssocHandler</strong></a> object to provide access to its explicit Application User Model ID (AppUserModelID).</span></span> <span data-ttu-id="71ab3-535">這項資訊是用來判斷特定檔案類型是否可以加入至應用程式的捷徑清單。</span><span class="sxs-lookup"><span data-stu-id="71ab3-535">This information is used to determine whether a particular file type can be added to an application's Jump List.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-536"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithbackreferences"><strong>IObjectWithBackReferences</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-536"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithbackreferences"><strong>IObjectWithBackReferences</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-537">提供與物件所持有之反向參考互動的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-537">Provides a method for interacting with back references held by an object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-538"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithcancelevent"><strong>IObjectWithCancelEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-538"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithcancelevent"><strong>IObjectWithCancelEvent</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-539">提供具有事件的呼叫端，該事件將由被呼叫的物件發出信號以表示取消工作。</span><span class="sxs-lookup"><span data-stu-id="71ab3-539">Supplies a caller with an event that will be signaled by the called object to denote cancellation of a task.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-540"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithfolderenummode"><strong>IObjectWithFolderEnumMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-540"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithfolderenummode"><strong>IObjectWithFolderEnumMode</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-541">公開方法，以取得和設定剖析專案的列舉模式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-541">Exposes methods that get and set enumeration modes of a parsed item.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-542"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithprogid"><strong>IObjectWithProgID</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-542"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithprogid"><strong>IObjectWithProgID</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-543">公開方法，以提供與物件相關聯之 ProgID 的存取權。</span><span class="sxs-lookup"><span data-stu-id="71ab3-543">Exposes methods that provide access to the ProgID associated with an object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-544"><a href="/windows/desktop/api/Propsys/nn-propsys-iobjectwithpropertykey"><strong>IObjectWithPropertyKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-544"><a href="/windows/desktop/api/Propsys/nn-propsys-iobjectwithpropertykey"><strong>IObjectWithPropertyKey</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-545">公開取得和設定屬性索引鍵的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-545">Exposes methods for getting and setting the property key.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-546"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-546"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-547">公開方法，以取得或設定由 Shell 專案陣列所表示的選取專案。</span><span class="sxs-lookup"><span data-stu-id="71ab3-547">Exposes methods that get or set selected items represented by a Shell item array.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-548"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iobjmgr"><strong>IObjMgr</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-548"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iobjmgr"><strong>IObjMgr</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-549">公開方法，以允許用戶端從伺服器物件所管理的物件集合中附加或移除物件。</span><span class="sxs-lookup"><span data-stu-id="71ab3-549">Exposes methods that allow a client to append or remove an object from a collection of objects managed by a server object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-550"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel"><strong>IOpenControlPanel</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-550"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel"><strong>IOpenControlPanel</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-551">公開方法，以取得主控台的檢視狀態、個別主控台專案的路徑，以及開啟主控台本身或個別的主控台專案。</span><span class="sxs-lookup"><span data-stu-id="71ab3-551">Exposes methods that retrieve the view state of the Control Panel, the path of individual Control Panel items, and that open either the Control Panel itself or an individual Control Panel item.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-552"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopensearchsource"><strong>IOpenSearchSource</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-552"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopensearchsource"><strong>IOpenSearchSource</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-553">公開方法，以從自訂用戶端的 OpenSearch 資料來源取得搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="71ab3-553">Exposes a method to get search results from a custom client-side OpenSearch data source.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-554"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ioperationsprogressdialog"><strong>IOperationsProgressDialog</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-554"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ioperationsprogressdialog"><strong>IOperationsProgressDialog</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-555">公開方法以取得、設定和查詢進度對話方塊。</span><span class="sxs-lookup"><span data-stu-id="71ab3-555">Exposes methods to get, set, and query a progress dialog.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-556"><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ipackagedebugsettings"><strong>IPackageDebugSettings</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-556"><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ipackagedebugsettings"><strong>IPackageDebugSettings</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-557">可讓偵錯工具開發人員控制 Windows Store 應用程式的生命週期，例如暫停或繼續。</span><span class="sxs-lookup"><span data-stu-id="71ab3-557">Enables debugger developers to control the life cycle of a Windows Store app, such as suspending or resuming.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-558"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackageexecutionstatechangenotification"><strong>IPackageExecutionStateChangeNotification</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-558"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackageexecutionstatechangenotification"><strong>IPackageExecutionStateChangeNotification</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-559">啟用在 Windows Store 應用程式偵錯工具期間接收封裝狀態變更通知。</span><span class="sxs-lookup"><span data-stu-id="71ab3-559">Enables receiving package state-change notifications during Windows Store app debugging.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-560"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>IParentAndItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-560"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>IParentAndItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-561">公開取得和設定父系和父系之子系識別碼的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-561">Exposes methods that get and set the parent and the parent's child ID.</span></span> <span data-ttu-id="71ab3-562">雖然 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>IParentAndItem</strong></a> 通常是在 IShellItems 上執行，但它並不是特定的 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="71ab3-562">While <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>IParentAndItem</strong></a> is typically implemented on IShellItems, it is not specific to <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-563"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparseandcreateitem"><strong>IParseAndCreateItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-563"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparseandcreateitem"><strong>IParseAndCreateItem</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-564"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder"><strong>IPersistFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-564"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder"><strong>IPersistFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-565">公開初始化 Shell 資料夾物件的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-565">Exposes a method that initializes Shell folder objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-566"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2"><strong>IPersistFolder2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-566"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2"><strong>IPersistFolder2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-567">公開從 Shell 資料夾物件取得資訊的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-567">Exposes methods that obtain information from Shell folder objects.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-568"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3"><strong>IPersistFolder3</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-568"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3"><strong>IPersistFolder3</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-569">藉由允許資料夾物件執行資料夾快捷方式的非預設處理，擴充 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder"><strong>IPersistFolder</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2"><strong>IPersistFolder2</strong></a> 介面。</span><span class="sxs-lookup"><span data-stu-id="71ab3-569">Extends the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder"><strong>IPersistFolder</strong></a> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2"><strong>IPersistFolder2</strong></a> interfaces by allowing a folder object to implement nondefault handling of folder shortcuts.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-570"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistidlist"><strong>IPersistIDList</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-570"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistidlist"><strong>IPersistIDList</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-571">公開用來保存專案識別碼清單的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-571">Exposes methods that are used to persist item identifier lists.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-572"><a href="/windows/desktop/api/Propsys/nn-propsys-ipersistserializedpropstorage"><strong>IPersistSerializedPropStorage</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-572"><a href="/windows/desktop/api/Propsys/nn-propsys-ipersistserializedpropstorage"><strong>IPersistSerializedPropStorage</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-573">公開方法以保存序列化屬性儲存體資料以供稍後使用，以及將保存的資料還原至新的屬性存放區實例。</span><span class="sxs-lookup"><span data-stu-id="71ab3-573">Exposes methods to persist serialized property storage data for later use and to restore persisted data to a new property store instance.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-574"><a href="/windows/desktop/api/Propsys/nn-propsys-ipersistserializedpropstorage2"><strong>IPersistSerializedPropStorage2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-574"><a href="/windows/desktop/api/Propsys/nn-propsys-ipersistserializedpropstorage2"><strong>IPersistSerializedPropStorage2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-575">公開方法以保存序列化屬性儲存體資料以供稍後使用，以及將保存的資料還原至新的屬性存放區實例。</span><span class="sxs-lookup"><span data-stu-id="71ab3-575">Exposes methods to persist serialized property storage data for later use and to restore persisted data to a new property store instance.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-576"><a href="/previous-versions/windows/desktop/legacy/hh707033(v=vs.85)"><strong>IPlaybackManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-576"><a href="/previous-versions/windows/desktop/legacy/hh707033(v=vs.85)"><strong>IPlaybackManager</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-577">提供可讓媒體應用程式與 Windows 播放管理員進行通訊的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-577">Provides methods that allow media applications to communicate with the Windows playback manager.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-578"><a href="/previous-versions/windows/desktop/legacy/hh707034(v=vs.85)"><strong>IPlaybackManagerEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-578"><a href="/previous-versions/windows/desktop/legacy/hh707034(v=vs.85)"><strong>IPlaybackManagerEvents</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-579"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler"><strong>IPreviewHandler</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-579"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler"><strong>IPreviewHandler</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-580">公開顯示豐富預覽的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-580">Exposes methods for the display of rich previews.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-581"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe"><strong>IPreviewHandlerFrame</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-581"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe"><strong>IPreviewHandlerFrame</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-582">啟用預覽處理常式，以將鍵盤快速鍵傳遞給主機。</span><span class="sxs-lookup"><span data-stu-id="71ab3-582">Enables preview handlers to pass keyboard shortcuts to the host.</span></span> <span data-ttu-id="71ab3-583">這個介面會抓取鍵盤快速鍵的清單，並引導主機處理鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="71ab3-583">This interface retrieves a list of keyboard shortcuts and directs the host to handle a keyboard shortcut.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-584"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals"><strong>IPreviewHandlerVisuals</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-584"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals"><strong>IPreviewHandlerVisuals</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-585">公開將色彩和字型資訊套用至預覽處理常式的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-585">Exposes methods for applying color and font information to preview handlers.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-586"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewitem"><strong>IPreviewItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-586"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewitem"><strong>IPreviewItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-587">識別將在預覽窗格中顯示的專案。</span><span class="sxs-lookup"><span data-stu-id="71ab3-587">Identifies an item that will be shown in the preview pane.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-588"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ipreviousversionsinfo"><strong>IPreviousVersionsInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-588"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ipreviousversionsinfo"><strong>IPreviousVersionsInfo</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-589">公開一種方法，該方法會檢查先前版本的伺服器檔案或資料夾，這些檔案或資料夾是由 Windows Server 2003 提供的 <em>陰影複製</em> 技術所儲存的回復用途。</span><span class="sxs-lookup"><span data-stu-id="71ab3-589">Exposes a method that checks for previous versions of server files or folders, stored for the purpose of reversion by the <em>shadow copies</em> technology provided with Windows Server 2003.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-590"><a href="iprivateidentitymanager.md"><strong>IPrivateIdentityManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-590"><a href="iprivateidentitymanager.md"><strong>IPrivateIdentityManager</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-591"><a href="iprivateidentitymanager2.md"><strong>IPrivateIdentityManager2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-591"><a href="iprivateidentitymanager2.md"><strong>IPrivateIdentityManager2</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-592"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iprofferservice"><strong>IProfferService</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-592"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iprofferservice"><strong>IProfferService</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-593">公開物件的一般機制，以提供服務給相同主機上的其他物件。</span><span class="sxs-lookup"><span data-stu-id="71ab3-593">Exposes a general mechanism for objects to offer services to other objects on the same host.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-594"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iprogressdialog"><strong>IProgressDialog</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-594"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iprogressdialog"><strong>IProgressDialog</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-595">公開提供應用程式選項以顯示進度對話方塊的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-595">Exposes methods that provide options for an application to display a progress dialog box.</span></span> <span data-ttu-id="71ab3-596">此介面是由進度對話方塊物件所匯出 (CLSID_ProgressDialog) 。</span><span class="sxs-lookup"><span data-stu-id="71ab3-596">This interface is exported by the progress dialog box object (CLSID_ProgressDialog).</span></span> <span data-ttu-id="71ab3-597">此物件是向使用者顯示操作進度的一般方式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-597">This object is a generic way to show a user how an operation is progressing.</span></span> <span data-ttu-id="71ab3-598">在刪除、上傳、複製、移動或下載大量檔案時，通常會使用此值。</span><span class="sxs-lookup"><span data-stu-id="71ab3-598">It is typically used when deleting, uploading, copying, moving, or downloading large numbers of files.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-599"><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp"><strong>IPublishedApp</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-599"><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp"><strong>IPublishedApp</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-600">公開方法，這些方法代表在主控台中新增/移除程式的應用程式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-600">Exposes methods that represent applications to Add/Remove Programs in Control Panel.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-601"><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp2"><strong>IPublishedApp2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-601"><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp2"><strong>IPublishedApp2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-602">藉由提供額外的安裝方法來擴充 <a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp"><strong>IPublishedApp</strong></a> 介面。</span><span class="sxs-lookup"><span data-stu-id="71ab3-602">Extends the <a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp"><strong>IPublishedApp</strong></a> interface by providing an additional installation method.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-603"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ipublishingwizard"><strong>IPublishingWizard</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-603"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ipublishingwizard"><strong>IPublishingWizard</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-604">公開使用線上列印嚮導、Web 發佈嚮導和「新增網路位置嚮導」的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-604">Exposes methods for working with the Online Print Wizard, the Web Publishing Wizard, and the Add Network Place Wizard.</span></span> <span data-ttu-id="71ab3-605">在 Windows Vista 中， <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ipublishingwizard"><strong>IPublishingWizard</strong></a> 不再支援 Web 發佈嚮導或線上列印嚮導。</span><span class="sxs-lookup"><span data-stu-id="71ab3-605">In Windows Vista, <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ipublishingwizard"><strong>IPublishingWizard</strong></a> no longer supports the Web Publishing Wizard or Online Print Wizard.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-606"><a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-606"><a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-607">公開方法，以簡化與定義檔案類型或通訊協定並將其與應用程式產生關聯之登錄中儲存的資訊的處理常式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-607">Exposes methods that simplify the process of retrieving information stored in the registry in association with defining a file type or protocol and associating it with an application.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-608"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iquerycancelautoplay"><strong>IQueryCancelAutoPlay</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-608"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iquerycancelautoplay"><strong>IQueryCancelAutoPlay</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-609">公開以程式設計方式覆寫 <a href="autorun2k-intro.md">自動播放</a> 或 <a href="autoplay.md">自動</a>播放的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-609">Exposes a method that programmatically overrides <a href="autorun2k-intro.md">AutoPlay</a> or <a href="autoplay.md">AutoRun</a>.</span></span> <span data-ttu-id="71ab3-610">這可讓您自訂插入媒體時所啟動的位置和內容類型。</span><span class="sxs-lookup"><span data-stu-id="71ab3-610">This allows you to customize the location and type of content that is launched when media is inserted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-611"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iquerycodepage"><strong>IQueryCodePage</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-611"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iquerycodepage"><strong>IQueryCodePage</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-612">取得和設定 ANSI 字碼頁 (字碼頁識別碼) 的數值。</span><span class="sxs-lookup"><span data-stu-id="71ab3-612">Gets and sets the numeric value (Code Page identifier) of the ANSI code page.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-613"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iquerycontinue"><strong>IQueryContinue</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-613"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iquerycontinue"><strong>IQueryContinue</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-614">公開方法，這個方法會為物件提供簡單的標準機制，以查詢用戶端以取得繼續作業的許可權。</span><span class="sxs-lookup"><span data-stu-id="71ab3-614">Exposes a method that provides a simple, standard mechanism for objects to query a client for permission to continue an operation.</span></span> <span data-ttu-id="71ab3-615">例如， <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a>的用戶端必須將 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iquerycontinue"><strong>IQueryContinue</strong></a> 的執行傳遞至 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iusernotification-show"><strong>IUserNotification：： Show</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-615">Clients of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a>, for example, must pass an implementation of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iquerycontinue"><strong>IQueryContinue</strong></a> to the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iusernotification-show"><strong>IUserNotification::Show</strong></a> method.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-616"><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-iquerycontinuewithstatus"><strong>IQueryContinueWithStatus</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-616"><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-iquerycontinuewithstatus"><strong>IQueryContinueWithStatus</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-617">公開方法，這些方法會提供標準機制，讓認證提供者在嘗試連接到網路時呼叫 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iquerycontinue-querycontinue"><strong>QueryContinue</strong></a> ，以判斷是否應該繼續進行這些嘗試。</span><span class="sxs-lookup"><span data-stu-id="71ab3-617">Exposes methods that provide a standard mechanism for credential providers to call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iquerycontinue-querycontinue"><strong>QueryContinue</strong></a> while attempting to connect to the network to determine if they should continue these attempts.</span></span> <span data-ttu-id="71ab3-618">認證提供者也可以使用此介面，在嘗試建立網路連線時向使用者顯示訊息。</span><span class="sxs-lookup"><span data-stu-id="71ab3-618">Credential providers can also use this interface to display messages to the user while attempting to establish a network connection.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-619"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iqueryinfo"><strong>IQueryInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-619"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iqueryinfo"><strong>IQueryInfo</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-620">公開方法，以供 Shell 用來取得位於 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> 執行中之專案的旗標和資訊提示資訊。</span><span class="sxs-lookup"><span data-stu-id="71ab3-620">Exposes methods that the Shell uses to retrieve flags and info tip information for an item that resides in an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> implementation.</span></span> <span data-ttu-id="71ab3-621">資訊提示通常會顯示在 <a href="/windows/desktop/Controls/tooltip-controls">工具提示</a> 控制項內。</span><span class="sxs-lookup"><span data-stu-id="71ab3-621">Info tips are usually displayed inside a <a href="/windows/desktop/Controls/tooltip-controls">tooltip</a> control.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-622"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irelateditem"><strong>IRelatedItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-622"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irelateditem"><strong>IRelatedItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-623">公開衍生具有特定關聯性之相關專案的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-623">Exposes methods that derive related items with specific relationships.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-624"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer"><strong>IRemoteComputer</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-624"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer"><strong>IRemoteComputer</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-625">公開方法，該方法會在遠端物件上叫用時，列舉或初始化命名空間延伸模組。</span><span class="sxs-lookup"><span data-stu-id="71ab3-625">Exposes a method that enumerates or initializes a namespace extension when it is invoked on a remote object.</span></span> <span data-ttu-id="71ab3-626">例如，會使用此介面來初始化遠端印表機虛擬資料夾。</span><span class="sxs-lookup"><span data-stu-id="71ab3-626">This interface is used, for example, to initialize the remote printers virtual folder.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-627"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iresolveshelllink"><strong>IResolveShellLink</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-627"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iresolveshelllink"><strong>IResolveShellLink</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-628">公開方法，這個方法可讓應用程式要求 Shell 資料夾物件解析其其中一個專案的連結。</span><span class="sxs-lookup"><span data-stu-id="71ab3-628">Exposes a method that enables an application to request that a Shell folder object resolve a link for one of its items.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-629"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iresultsfolder"><strong>IResultsFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-629"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iresultsfolder"><strong>IResultsFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-630">公開保存資料物件中專案的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-630">Exposes methods that hold items from a data object.</span></span><br/> <span data-ttu-id="71ab3-631"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iresultsfolder"><strong>IResultsFolder</strong></a>是一個資料夾，可保存所有命名空間的專案，並將其代表單一資料夾中的使用者。</span><span class="sxs-lookup"><span data-stu-id="71ab3-631">An <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iresultsfolder"><strong>IResultsFolder</strong></a> is a folder that can hold items from all over the namespace and represent them to the user in a single folder.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-632"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irunnabletask"><strong>IRunnableTask</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-632"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irunnabletask"><strong>IRunnableTask</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-633">可由物件公開的自由執行緒介面，可讓您在背景執行緒上執行作業。</span><span class="sxs-lookup"><span data-stu-id="71ab3-633">A free-threaded interface that can be exposed by an object to allow operations to be performed on a background thread.</span></span> <span data-ttu-id="71ab3-634">例如，如果 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iextractimage-getlocation"><strong>IExtractImage：： GetLocation</strong></a> 方法傳回 E_PENDING，則會允許呼叫的應用程式在背景執行緒上解壓縮影像。</span><span class="sxs-lookup"><span data-stu-id="71ab3-634">For example, if the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iextractimage-getlocation"><strong>IExtractImage::GetLocation</strong></a> method returns E_PENDING, the calling application is permitted to extract the image on a background thread.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-635"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-isearchboxinfo"><strong>ISearchBoxInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-635"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-isearchboxinfo"><strong>ISearchBoxInfo</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-636">公開方法，可讓呼叫者取出輸入至搜尋方塊中的資訊。</span><span class="sxs-lookup"><span data-stu-id="71ab3-636">Exposes methods that allow the caller to retrieve information entered into a search box.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-637"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-isearchcontext"><strong>ISearchCoNtext</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-637"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-isearchcontext"><strong>ISearchContext</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-638">公開將自訂資訊通道至搜尋攔截的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-638">Exposes methods that channel customization information to the search hooks.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-639"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory"><strong>ISearchFolderItemFactory</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-639"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory"><strong>ISearchFolderItemFactory</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-640">公開建立和修改搜尋資料夾的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-640">Exposes methods that create and modify search folders.</span></span> <span data-ttu-id="71ab3-641">系統會先呼叫 Set 方法，以設定搜尋的參數。</span><span class="sxs-lookup"><span data-stu-id="71ab3-641">The Set methods are called first to set up the parameters of the search.</span></span> <span data-ttu-id="71ab3-642">若未呼叫，則會改用預設值。</span><span class="sxs-lookup"><span data-stu-id="71ab3-642">When not called, default values will be used instead.</span></span> <span data-ttu-id="71ab3-643"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-getidlist"><strong>ISearchFolderItemFactory：： GetIDList</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-getshellitem"><strong>ISearchFolderItemFactory：： GetShellItem</strong></a> 會傳回這些參數所指定的兩個搜尋形式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-643"><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-getidlist"><strong>ISearchFolderItemFactory::GetIDList</strong></a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-getshellitem"><strong>ISearchFolderItemFactory::GetShellItem</strong></a> return the two forms of the search specified by these parameters.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-644"><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-isharedbitmap"><strong>ISharedBitmap</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-644"><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-isharedbitmap"><strong>ISharedBitmap</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-645">公開記憶體有效率的方法來存取點陣圖。</span><span class="sxs-lookup"><span data-stu-id="71ab3-645">Exposes memory-efficient methods for accessing bitmaps.</span></span> <span data-ttu-id="71ab3-646">此介面是用來做為 HBITMAP 物件周圍的精簡型包裝函式，可讓這些物件的參考計數和保護，使其基礎資料變更。</span><span class="sxs-lookup"><span data-stu-id="71ab3-646">This interface is used as a thin wrapper around HBITMAP objects, allowing those objects to be reference counted and protected from having their underlying data changed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-647"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isharingconfigurationmanager"><strong>ISharingConfigurationManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-647"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isharingconfigurationmanager"><strong>ISharingConfigurationManager</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-648">公開方法，以針對 <strong>使用者</strong> (<code>C:\Users</code>) 或 <strong>公用</strong> () 資料夾，設定和抓取電腦預設共用設定的相關資訊 <code>C:\Users\Public</code> 。</span><span class="sxs-lookup"><span data-stu-id="71ab3-648">Exposes methods that set and retrieve information about a computer's default sharing settings for the <strong>Users</strong> (<code>C:\Users</code>) or <strong>Public</strong> (<code>C:\Users\Public</code>) folder.</span></span> <span data-ttu-id="71ab3-649">也會公開一組允許控制印表機共用的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-649">Also exposes a set of methods that allow control of printer sharing.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-650"><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ishellapp"><strong>IShellApp</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-650"><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ishellapp"><strong>IShellApp</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-651">公開方法，以將應用程式的一般資訊提供給「新增/移除程式」應用程式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-651">Exposes methods that provide general information about an application to the Add/Remove Programs Application.</span></span> <span data-ttu-id="71ab3-652">您無法在 [新增/移除程式] 應用程式之外使用它。</span><span class="sxs-lookup"><span data-stu-id="71ab3-652">You cannot use it outside the Add/Remove Programs application.</span></span> <span data-ttu-id="71ab3-653">此介面所提供的資訊包括支援的管理動作清單，以及應用程式目前是否已安裝。</span><span class="sxs-lookup"><span data-stu-id="71ab3-653">The information given by this interface includes a list of supported management actions and whether the application is currently installed.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-654"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser"><strong>IShellBrowser</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-654"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser"><strong>IShellBrowser</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-655">由 Shell 視圖的主機所執行， (可執行 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a>) 的物件。</span><span class="sxs-lookup"><span data-stu-id="71ab3-655">Implemented by hosts of Shell views (objects that implement <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a>).</span></span> <span data-ttu-id="71ab3-656">公開方法，這些方法會為其所裝載的視圖提供服務，以及在 Explorer 視窗的內容中執行的其他物件。</span><span class="sxs-lookup"><span data-stu-id="71ab3-656">Exposes methods that provide services for the view it is hosting and other objects that run in the context of the Explorer window.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-657"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishellchangenotify"><strong>IShellChangeNotify</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-657"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishellchangenotify"><strong>IShellChangeNotify</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-658">公開方法，這個方法會在專案的識別碼變更時通知 Shell 命名空間延伸。</span><span class="sxs-lookup"><span data-stu-id="71ab3-658">Exposes a method that notifies a Shell namespace extension when the ID of an item has changed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-659"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelldetails"><strong>IShellDetails</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-659"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelldetails"><strong>IShellDetails</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-660">由 Shell 資料夾公開，以提供資料夾中專案的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="71ab3-660">Exposed by Shell folders to provide detailed information about the items in a folder.</span></span> <span data-ttu-id="71ab3-661">當資料夾的視圖設定為 [詳細資料] 時，Windows 檔案總管所顯示的相同資訊。</span><span class="sxs-lookup"><span data-stu-id="71ab3-661">This is the same information that is displayed by the Windows Explorer when the view of the folder is set to Details.</span></span> <span data-ttu-id="71ab3-662">若為 Windows 2000 和更新版本的系統， <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelldetails"><strong>IShellDetails</strong></a> 會被 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2"><strong>IShellFolder2</strong></a>取代。</span><span class="sxs-lookup"><span data-stu-id="71ab3-662">For Windows 2000 and later systems, <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelldetails"><strong>IShellDetails</strong></a> is superseded by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2"><strong>IShellFolder2</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-663"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellextinit"><strong>IShellExtInit</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-663"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellextinit"><strong>IShellExtInit</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-664">公開方法，這個方法會初始化屬性工作表、快捷方式功能表和拖放處理常式的 Shell 延伸模組， (在非預設拖放作業期間將專案新增至快捷方式功能表的延伸模組) 。</span><span class="sxs-lookup"><span data-stu-id="71ab3-664">Exposes a method that initializes Shell extensions for property sheets, shortcut menus, and drag-and-drop handlers (extensions that add items to shortcut menus during nondefault drag-and-drop operations).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-665"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-665"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-666">由所有 Shell 命名空間資料夾物件公開，其方法是用來管理資料夾。</span><span class="sxs-lookup"><span data-stu-id="71ab3-666">Exposed by all Shell namespace folder objects, its methods are used to manage folders.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-667"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2"><strong>IShellFolder2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-667"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2"><strong>IShellFolder2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-668">擴充 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a>的功能。</span><span class="sxs-lookup"><span data-stu-id="71ab3-668">Extends the capabilities of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a>.</span></span> <span data-ttu-id="71ab3-669">其方法提供 Shell 資料夾內容的各種相關資訊。</span><span class="sxs-lookup"><span data-stu-id="71ab3-669">Its methods provide a variety of information about the contents of a Shell folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-670"><a href="ishellfoldersearchable.md"><strong>IShellFolderSearchable</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-670"><a href="ishellfoldersearchable.md"><strong>IShellFolderSearchable</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-671">公開允許 Shell 延伸模組提供可搜尋的命名空間的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-671">Exposes methods that allow a Shell extension to provide a searchable namespace.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-672"><a href="ishellfoldersearchablecallback.md"><strong>IShellFolderSearchableCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-672"><a href="ishellfoldersearchablecallback.md"><strong>IShellFolderSearchableCallback</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-673">公開回呼常式來監視搜尋處理常式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-673">Exposes callback routines to monitor the search process.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-674"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishellfolderviewcb"><strong>IShellFolderViewCB</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-674"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishellfolderviewcb"><strong>IShellFolderViewCB</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-675">公開一種方法，這個方法可讓 Windows 檔案總管和使用系統資料夾 view 物件所執行的資料夾檢視， (透過) <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a>所傳回的<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a>物件，讓資料夾檢視可以收到事件的通知，並據以修改其觀點。</span><span class="sxs-lookup"><span data-stu-id="71ab3-675">Exposes a method that allows communication between Windows Explorer and a folder view implemented using the system folder view object (the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a> object returned through <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a>) so that the folder view can be notified of events and modify its view accordingly.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-676"><a href="/windows/desktop/api/Shldisp/nn-shldisp-ishellfolderviewdual"><strong>IShellFolderViewDual</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-676"><a href="/windows/desktop/api/Shldisp/nn-shldisp-ishellfolderviewdual"><strong>IShellFolderViewDual</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-677">公開修改視圖並選取目前資料夾中專案的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-677">Exposes methods that modify the view and select items in the current folder.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-678"><a href="/windows/desktop/api/Shldisp/nn-shldisp-ishellfolderviewdual2"><strong>IShellFolderViewDual2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-678"><a href="/windows/desktop/api/Shldisp/nn-shldisp-ishellfolderviewdual2"><strong>IShellFolderViewDual2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-679">公開修改視圖並選取目前資料夾中專案的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-679">Exposes methods that modify the view and select items in the current folder.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-680"><a href="/windows/desktop/api/Shldisp/nn-shldisp-ishellfolderviewdual3"><strong>IShellFolderViewDual3</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-680"><a href="/windows/desktop/api/Shldisp/nn-shldisp-ishellfolderviewdual3"><strong>IShellFolderViewDual3</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-681">公開修改目前資料夾檢視的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-681">Exposes methods that modify the current folder view.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-682"><a href="ishellfolderviewtype.md"><strong>IShellFolderViewType</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-682"><a href="ishellfolderviewtype.md"><strong>IShellFolderViewType</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-683">公開方法，讓 Shell 資料夾可在其內容上支援不同的視圖， (其資料) 的不同階層式版面配置。</span><span class="sxs-lookup"><span data-stu-id="71ab3-683">Exposes methods that enable a Shell folder to support different views on its content (different hierarchical layouts of its data).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-684"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellicon"><strong>IShellIcon</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-684"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellicon"><strong>IShellIcon</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-685">公開方法，以取得 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> 物件的圖示索引。</span><span class="sxs-lookup"><span data-stu-id="71ab3-685">Exposes a method that obtains an icon index for an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> object.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-686"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelliconoverlay"><strong>IShellIconOverlay</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-686"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelliconoverlay"><strong>IShellIconOverlay</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-687">公開命名空間延伸模組所使用的方法，以指定其包含之物件的圖示重迭。</span><span class="sxs-lookup"><span data-stu-id="71ab3-687">Exposes methods that are used by a namespace extension to specify icon overlays for the objects it contains.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-688"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelliconoverlayidentifier"><strong>IShellIconOverlayIdentifier</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-688"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelliconoverlayidentifier"><strong>IShellIconOverlayIdentifier</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-689">公開處理圖示重迭處理常式和 Shell 之間所有通訊的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-689">Exposes methods that handle all communication between icon overlay handlers and the Shell.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-690"><a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedataabort"><strong>IShellImageDataAbort</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-690"><a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedataabort"><strong>IShellImageDataAbort</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-691">公開用來中止 <a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedata"><strong>IShellImageData</strong></a> 進程的單一方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-691">Exposes a single method used to abort <a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedata"><strong>IShellImageData</strong></a> processes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-692"><a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedatafactory"><strong>IShellImageDataFactory</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-692"><a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedatafactory"><strong>IShellImageDataFactory</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-693">公開方法，以根據各種影像來源來建立 <a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedata"><strong>IShellImageData</strong></a> 實例。</span><span class="sxs-lookup"><span data-stu-id="71ab3-693">Exposes methods that create <a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedata"><strong>IShellImageData</strong></a> instances based on various image sources.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-694"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-694"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-695">公開取得 Shell 專案相關資訊的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-695">Exposes methods that retrieve information about a Shell item.</span></span> <span data-ttu-id="71ab3-696"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2"><strong>IShellItem2</strong></a> 是任何新程式碼中專案的慣用標記法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-696"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2"><strong>IShellItem2</strong></a> are the preferred representations of items in any new code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-697"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2"><strong>IShellItem2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-697"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2"><strong>IShellItem2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-698">使用可取得專案之各種屬性值的方法來擴充 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="71ab3-698">Extends <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> with methods that retrieve various property values of the item.</span></span> <span data-ttu-id="71ab3-699"><strong>IShellItem</strong> 和 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2"><strong>IShellItem2</strong></a> 是任何新程式碼中專案的慣用標記法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-699"><strong>IShellItem</strong> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2"><strong>IShellItem2</strong></a> are the preferred representations of items in any new code.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-700"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray"><strong>IShellItemArray</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-700"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray"><strong>IShellItemArray</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-701">公開建立和操作 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>Shell 專案</strong></a> 陣列的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-701">Exposes methods that create and manipulate <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>Shell item</strong></a> arrays.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-702"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemfilter"><strong>IShellItemFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-702"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemfilter"><strong>IShellItemFilter</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-703">由用戶端公開，以指定如何透過伺服器應用程式篩選 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>Shell 專案</strong></a> 的列舉。</span><span class="sxs-lookup"><span data-stu-id="71ab3-703">Exposed by a client to specify how to filter the enumeration of a <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>Shell item</strong></a> by a server application.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-704"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemimagefactory"><strong>IShellItemImageFactory</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-704"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemimagefactory"><strong>IShellItemImageFactory</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-705">公開方法，以傳回 Shell 專案的圖示或縮圖。</span><span class="sxs-lookup"><span data-stu-id="71ab3-705">Exposes a method to return either icons or thumbnails for Shell items.</span></span> <span data-ttu-id="71ab3-706">如果要求的專案沒有可用的縮圖或圖示，則可以從 Shell 提供個別類別的圖示。</span><span class="sxs-lookup"><span data-stu-id="71ab3-706">If no thumbnail or icon is available for the requested item, a per-class icon may be provided from the Shell.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-707"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemresources"><strong>IShellItemResources</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-707"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemresources"><strong>IShellItemResources</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-708">公開操作和查詢 Shell 專案資源的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-708">Exposes methods to manipulate and query Shell item resources.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-709"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary"><strong>IShellLibrary</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-709"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary"><strong>IShellLibrary</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-710">公開用來建立和管理程式庫的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-710">Exposes methods for creating and managing libraries.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-711"><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-711"><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-712">公開建立、修改和解析 Shell 連結的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-712">Exposes methods that create, modify, and resolve Shell links.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-713"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-713"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-714">公開可讓應用程式將額外的資料區塊附加至 <a href="/windows/desktop/shell/links">Shell 連結</a>的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-714">Exposes methods that allow an application to attach extra data blocks to a <a href="/windows/desktop/shell/links">Shell link</a>.</span></span> <span data-ttu-id="71ab3-715">這些方法會新增、複製或移除資料區塊。</span><span class="sxs-lookup"><span data-stu-id="71ab3-715">These methods add, copy, or remove data blocks.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-716"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu"><strong>IShellMenu</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-716"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu"><strong>IShellMenu</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-717">公開與 Shell 功能表互動的方法，例如 [ <strong>開始</strong> ] 功能表和 [我的最愛 <strong>]</strong> 功能表。</span><span class="sxs-lookup"><span data-stu-id="71ab3-717">Exposes methods that interact with Shell menus such as the <strong>Start</strong> menu, and the <strong>Favorites</strong> menu.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-718"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback"><strong>IShellMenuCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-718"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback"><strong>IShellMenuCallback</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-719">回呼介面，這個介面會公開從功能表區中接收訊息的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-719">A callback interface that exposes a method that receives messages from a menu band.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-720"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext"><strong>IShellPropSheetExt</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-720"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext"><strong>IShellPropSheetExt</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-721">公開方法，這些方法可讓屬性工作表處理常式新增或取代針對檔案物件所顯示之屬性工作表中的頁面。</span><span class="sxs-lookup"><span data-stu-id="71ab3-721">Exposes methods that allow a property sheet handler to add or replace pages in the property sheet displayed for a file object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-722"><a href="/windows/desktop/api/shobjidl/nn-shobjidl-ishellrundll"><strong>IShellRunDll</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-722"><a href="/windows/desktop/api/shobjidl/nn-shobjidl-ishellrundll"><strong>IShellRunDll</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-723"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-723"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-724">公開在 Windows 檔案總管或資料夾視窗中顯示視圖的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-724">Exposes methods that present a view in the Windows Explorer or folder windows.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-725"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2"><strong>IShellView2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-725"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2"><strong>IShellView2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-726">擴充 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a>的功能。</span><span class="sxs-lookup"><span data-stu-id="71ab3-726">Extends the capabilities of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-727"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ishellview3"><strong>IShellView3</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-727"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ishellview3"><strong>IShellView3</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-728">藉由提供取代<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-createviewwindow2"><strong>IShellView2：： CreateViewWindow2</strong></a>的方法，擴充<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2"><strong>IShellView2</strong></a>的功能。</span><span class="sxs-lookup"><span data-stu-id="71ab3-728">Extends the capabilities of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2"><strong>IShellView2</strong></a> by providing a method to replace <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-createviewwindow2"><strong>IShellView2::CreateViewWindow2</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-729"><a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-729"><a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-730">提供開啟 Shell 視窗集合的存取權。</span><span class="sxs-lookup"><span data-stu-id="71ab3-730">Provides access to the collection of open Shell windows.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-731"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-istartmenupinnedlist"><strong>IStartMenuPinnedList</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-731"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-istartmenupinnedlist"><strong>IStartMenuPinnedList</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-732">公開從 [ <strong>開始</strong> ] 功能表或工作列取消固定應用程式快捷方式的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-732">Exposes a method that unpins an application shortcut from the <strong>Start</strong> menu or the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-733"><a href="nn-shobjidl-istorageprovidercopyhook.md"><strong>IStorageProviderCopyHook</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-733"><a href="nn-shobjidl-istorageprovidercopyhook.md"><strong>IStorageProviderCopyHook</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-734">公開方法，這個方法會判斷是否允許 Shell 移動、複製、刪除或重新命名雲端提供者的同步根中的資料夾。</span><span class="sxs-lookup"><span data-stu-id="71ab3-734">Exposes a method that determines whether the Shell will be allowed to move, copy, delete, or rename a folder in a cloud provider's sync root.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-735"><a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderhandler"><strong>IStorageProviderHandler</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-735"><a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderhandler"><strong>IStorageProviderHandler</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-736">捕獲與特定檔案或資料夾相關聯的 <a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderpropertyhandler"><strong>IStorageProviderPropertyHandler</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="71ab3-736">Retrieves the <a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderpropertyhandler"><strong>IStorageProviderPropertyHandler</strong></a> associated with a specific file or folder.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-737"><a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderpropertyhandler"><strong>IStorageProviderPropertyHandler</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-737"><a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderpropertyhandler"><strong>IStorageProviderPropertyHandler</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-738">提供與檔案或資料夾相關聯的屬性集合。</span><span class="sxs-lookup"><span data-stu-id="71ab3-738">Provides a collection of properties associated with a file or folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-739"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-istreamasync"><strong>IStreamAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-739"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-istreamasync"><strong>IStreamAsync</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-740">公開方法，以管理非同步資料流程) 的輸入/輸出 (i/o。</span><span class="sxs-lookup"><span data-stu-id="71ab3-740">Exposes methods to manage input/outpout (I/O) to an asynchronous stream.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-741"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-istreamunbufferedinfo"><strong>IStreamUnbufferedInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-741"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-istreamunbufferedinfo"><strong>IStreamUnbufferedInfo</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-742">公開方法，以將磁區大小判斷為位元組對齊的輔助。</span><span class="sxs-lookup"><span data-stu-id="71ab3-742">Exposes a method that determines the sector size as an aid to byte alignment.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-743"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isuspensiondependencymanager"><strong>ISuspensionDependencyManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-743"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isuspensiondependencymanager"><strong>ISuspensionDependencyManager</strong></a></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-744"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflict"><strong>ISyncMgrConflict</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-744"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflict"><strong>ISyncMgrConflict</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-745">公開方法，以提供從衝突存放區抓取之衝突的相關資訊，並允許解決衝突。</span><span class="sxs-lookup"><span data-stu-id="71ab3-745">Exposes methods that provide information about a conflict retrieved from a conflict store, and allows the conflict to be resolved.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-746"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>ISyncMgrConflictFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-746"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>ISyncMgrConflictFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-747">公開方法，以取得衝突物件的衝突 ID 清單。</span><span class="sxs-lookup"><span data-stu-id="71ab3-747">Exposes a method that gets the conflict ID list for a conflict object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-748"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictitems"><strong>ISyncMgrConflictItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-748"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictitems"><strong>ISyncMgrConflictItems</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-749">公開取得衝突專案資料和專案計數的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-749">Exposes methods that get conflict item data and item count.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-750"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictpresenter"><strong>ISyncMgrConflictPresenter</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-750"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictpresenter"><strong>ISyncMgrConflictPresenter</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-751">公開向使用者呈現衝突的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-751">Exposes a method that presents a conflict to the user.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-752"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictresolutionitems"><strong>ISyncMgrConflictResolutionItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-752"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictresolutionitems"><strong>ISyncMgrConflictResolutionItems</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-753">公開取得專案資訊和專案計數的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-753">Exposes methods that get item info and item count.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-754"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictresolveinfo"><strong>ISyncMgrConflictResolveInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-754"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictresolveinfo"><strong>ISyncMgrConflictResolveInfo</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-755">公開取得和設定同步管理員衝突解決相關資訊的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-755">Exposes methods that get and set information about sync manager conflict resolution.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-756"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictstore"><strong>ISyncMgrConflictStore</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-756"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictstore"><strong>ISyncMgrConflictStore</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-757">公開方法，讓處理常式能夠提供出現在衝突資料夾中的衝突。</span><span class="sxs-lookup"><span data-stu-id="71ab3-757">Exposes methods that allow a handler to provide conflicts that appear in the Conflicts folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-758"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrcontrol"><strong>ISyncMgrControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-758"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrcontrol"><strong>ISyncMgrControl</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-759">公開方法，以允許應用程式或處理常式啟動或停止同步處理、通知同步中心一組處理常式或專案的變更，或通知屬性值的變更。</span><span class="sxs-lookup"><span data-stu-id="71ab3-759">Exposes methods that allow an application or handler to start or stop a synchronization, notify Sync Center of changes to the set of handlers or items, or notify of changes to property values.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-760"><a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>ISyncMgrEnumItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-760"><a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>ISyncMgrEnumItems</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-761">公開列舉 <a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>SYNCMGRITEM</strong></a> 結構陣列的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-761">Exposes methods that enumerate through an array of <a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>SYNCMGRITEM</strong></a> structures.</span></span> <span data-ttu-id="71ab3-762">上述每一個結構都會提供可同步處理之專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="71ab3-762">Each of these structures provides information about an item that can be synchronized.</span></span> <span data-ttu-id="71ab3-763"><a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>ISyncMgrEnumItems</strong></a> 具有與所有標準列舉值介面相同的方法：下一步、略過、重設和複製。</span><span class="sxs-lookup"><span data-stu-id="71ab3-763"><a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>ISyncMgrEnumItems</strong></a> has the same methods as all standard enumerator interfaces: Next, Skip, Reset, and Clone.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-764"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrevent"><strong>ISyncMgrEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-764"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrevent"><strong>ISyncMgrEvent</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-765">公開從事件存放區取出資料的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-765">Exposes methods that retrieve data from an event store.</span></span> <span data-ttu-id="71ab3-766">事件存放區可讓同步中心取得存放區中所有事件的列舉值，以及取得個別事件。</span><span class="sxs-lookup"><span data-stu-id="71ab3-766">An event store allows Sync Center to get an enumerator of all events in the store, as well as to retrieve individual events.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-767"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgreventlinkuioperation"><strong>ISyncMgrEventLinkUIOperation</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-767"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgreventlinkuioperation"><strong>ISyncMgrEventLinkUIOperation</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-768">提供當按一下 [同步結果] 資料夾中的事件連結時，所呼叫的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-768">Provides a method that is called when event links are clicked in the sync results folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-769"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgreventstore"><strong>ISyncMgrEventStore</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-769"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgreventstore"><strong>ISyncMgrEventStore</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-770">公開的方法可讓處理常式提供自己的事件存放區，並管理它自己的同步事件，而不是使用預設的同步中心事件存放區。</span><span class="sxs-lookup"><span data-stu-id="71ab3-770">Exposes methods that allow a handler to provide its own event store and manage its own sync events, instead of using the default Sync Center event store.</span></span> <span data-ttu-id="71ab3-771">這些事件會顯示在 [同步處理結果] 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="71ab3-771">These events are displayed in the Sync Results folder.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-772"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler"><strong>ISyncMgrHandler</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-772"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler"><strong>ISyncMgrHandler</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-773">公開組成同步處理處理常式所執行之主要介面的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-773">Exposes methods that make up the primary interface implemented by a sync handler.</span></span> <span data-ttu-id="71ab3-774">同步中心透過這個介面建立一個處理常式的實例，以取得屬性、列舉同步專案，以及修改狀態。</span><span class="sxs-lookup"><span data-stu-id="71ab3-774">Sync Center creates one instance of the handler through this interface to get properties, enumerate sync items, and modify state.</span></span> <span data-ttu-id="71ab3-775">同步中心會在個別的執行緒上建立個別處理常式的實例，以執行同步處理或 UI 操作。</span><span class="sxs-lookup"><span data-stu-id="71ab3-775">Sync Center creates a separate instance of the handler on a separate thread to perform a synchronization or a UI operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-776"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlercollection"><strong>ISyncMgrHandlerCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-776"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlercollection"><strong>ISyncMgrHandlerCollection</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-777">公開提供同步處理處理常式識別碼列舉值的方法，並將這些同步處理處理常式具現化。</span><span class="sxs-lookup"><span data-stu-id="71ab3-777">Exposes methods that provide an enumerator of sync handler IDs and instantiate those sync handlers.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-778"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo"><strong>ISyncMgrHandlerInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-778"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo"><strong>ISyncMgrHandlerInfo</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-779">公開可讓處理常式將屬性和狀態資訊提供給同步中心的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-779">Exposes methods that allow a handler to provide property and state information to Sync Center.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-780"><a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrregister"><strong>ISyncMgrRegister</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-780"><a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrregister"><strong>ISyncMgrRegister</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-781">公開方法，讓應用程式可以向同步處理管理員註冊。</span><span class="sxs-lookup"><span data-stu-id="71ab3-781">Exposes methods so that an application can register with the synchronization manager.</span></span> <span data-ttu-id="71ab3-782">這可以透過 <a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrregister"><strong>ISyncMgrRegister</strong></a> 介面或直接在登錄中註冊來達成。</span><span class="sxs-lookup"><span data-stu-id="71ab3-782">This can be achieved either through the <a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrregister"><strong>ISyncMgrRegister</strong></a> interface or by registering directly in the registry.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-783"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrresolutionhandler"><strong>ISyncMgrResolutionHandler</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-783"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrresolutionhandler"><strong>ISyncMgrResolutionHandler</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-784">公開管理同步處理衝突的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-784">Exposes methods that manage synchronizing conflicts.</span></span> <span data-ttu-id="71ab3-785">執行此介面來建立同步衝突處理常式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-785">Implement this interface to construct a sync conflict handler.</span></span> <span data-ttu-id="71ab3-786">衝突解決使用者介面 (UI) 會呼叫這個介面，以解決呈現給使用者的衝突。</span><span class="sxs-lookup"><span data-stu-id="71ab3-786">The conflict resolution user interface (UI) will call this interface to resolve the conflict presented to the user.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-787"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrschedulewizarduioperation"><strong>ISyncMgrScheduleWizardUIOperation</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-787"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrschedulewizarduioperation"><strong>ISyncMgrScheduleWizardUIOperation</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-788">公開方法，這個方法可讓處理常式顯示處理常式的同步排程 wizard。</span><span class="sxs-lookup"><span data-stu-id="71ab3-788">Exposes a method that allows a handler to display the sync schedule wizard for the handler.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-789"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsessioncreator"><strong>ISyncMgrSessionCreator</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-789"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsessioncreator"><strong>ISyncMgrSessionCreator</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-790">公開單一方法，處理常式或外部應用程式可以透過此方法通知同步中心同步處理已開始，以及報告進度和事件。</span><span class="sxs-lookup"><span data-stu-id="71ab3-790">Exposes a single method through which a handler or external application can notify Sync Center that synchronization has begun, as well as report progress and events.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-791"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynccallback"><strong>ISyncMgrSyncCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-791"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynccallback"><strong>ISyncMgrSyncCallback</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-792">公開方法，以允許同步處理常式將進度和事件回報給同步中心，或查詢是否已取消處理常式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-792">Exposes methods that allow a synchronization process to report progress and events to Sync Center, or to query whether the process has been canceled.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-793"><a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize"><strong>ISyncMgrSynchronize</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-793"><a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize"><strong>ISyncMgrSynchronize</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-794">公開方法，讓已註冊的應用程式或服務接收來自同步處理管理員的通知。</span><span class="sxs-lookup"><span data-stu-id="71ab3-794">Exposes methods that enable the registered application or service to receive notifications from the synchronization manager.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-795"><a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback"><strong>ISyncMgrSynchronizeCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-795"><a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback"><strong>ISyncMgrSynchronizeCallback</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-796">公開管理同步處理常式的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-796">Exposes methods that manage the synchronization process.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-797"><a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronizeinvoke"><strong>ISyncMgrSynchronizeInvoke</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-797"><a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronizeinvoke"><strong>ISyncMgrSynchronizeInvoke</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-798">公開方法，讓已註冊的應用程式叫用同步處理管理員來更新專案。</span><span class="sxs-lookup"><span data-stu-id="71ab3-798">Exposes methods that enable a registered application to invoke the synchronization manager to update items.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-799"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem"><strong>ISyncMgrSyncItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-799"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem"><strong>ISyncMgrSyncItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-800">公開在單一同步處理專案中處理和取得資訊的方法，讓處理常式能夠將同步處理專案當做獨立物件來管理。</span><span class="sxs-lookup"><span data-stu-id="71ab3-800">Exposes methods that act on and retrieve information from a single sync item, allowing handlers to manage sync items as independent objects.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-801"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer"><strong>ISyncMgrSyncItemContainer</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-801"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer"><strong>ISyncMgrSyncItemContainer</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-802">公開方法，以提供有關其所包含專案之處理常式的資訊。</span><span class="sxs-lookup"><span data-stu-id="71ab3-802">Exposes methods that provide information to handlers about the items they contain.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-803"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo"><strong>ISyncMgrSyncItemInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-803"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo"><strong>ISyncMgrSyncItemInfo</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-804">公開提供單一同步處理專案之屬性和狀態資訊的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-804">Exposes methods that provide property and state information for a single sync item.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-805"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncresult"><strong>ISyncMgrSyncResult</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-805"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncresult"><strong>ISyncMgrSyncResult</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-806">公開呼叫 <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrcontrol"><strong>ISyncMgrControl</strong></a> 的應用程式可以使用的方法，以取得 <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-starthandlersync"><strong>ISyncMgrControl：： StartHandlerSync</strong></a> 或 <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-startitemsync"><strong>ISyncMgrControl：： StartItemSync</strong></a> 呼叫的結果。</span><span class="sxs-lookup"><span data-stu-id="71ab3-806">Exposes a method that applications calling <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrcontrol"><strong>ISyncMgrControl</strong></a> can use to get the result of a <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-starthandlersync"><strong>ISyncMgrControl::StartHandlerSync</strong></a> or <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-startitemsync"><strong>ISyncMgrControl::StartItemSync</strong></a> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-807"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgruioperation"><strong>ISyncMgrUIOperation</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-807"><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgruioperation"><strong>ISyncMgrUIOperation</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-808">公開方法，讓同步處理處理常式或同步處理專案可以在同步中心要求時，顯示 UI 物件。</span><span class="sxs-lookup"><span data-stu-id="71ab3-808">Exposes a method through which a sync handler or sync item can display a UI object when requested to do so by Sync Center.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-809"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist"><strong>ITaskbarList</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-809"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist"><strong>ITaskbarList</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-810">公開控制工作列的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-810">Exposes methods that control the taskbar.</span></span> <span data-ttu-id="71ab3-811">它可讓您以動態方式加入、移除和啟動工作列上的專案。</span><span class="sxs-lookup"><span data-stu-id="71ab3-811">It allows you to dynamically add, remove, and activate items on the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-812"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2"><strong>ITaskbarList2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-812"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2"><strong>ITaskbarList2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-813">藉由公開方法將視窗標示為全螢幕顯示，來擴充 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist"><strong>ITaskbarList</strong></a> 介面。</span><span class="sxs-lookup"><span data-stu-id="71ab3-813">Extends the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist"><strong>ITaskbarList</strong></a> interface by exposing a method to mark a window as a full-screen display.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-814"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>ITaskbarList3</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-814"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>ITaskbarList3</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-815">藉由公開支援 Windows 7 中所新增之統一啟動和切換工作列按鈕功能的方法，擴充 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2"><strong>ITaskbarList2</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="71ab3-815">Extends <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2"><strong>ITaskbarList2</strong></a> by exposing methods that support the unified launching and switching taskbar button functionality added in Windows 7.</span></span> <span data-ttu-id="71ab3-816">這項功能包含以索引標籤式應用程式中的個別索引標籤、縮圖工具列、通知和狀態重迭和進度指標為基礎的縮圖表示和切換目標。</span><span class="sxs-lookup"><span data-stu-id="71ab3-816">This functionality includes thumbnail representations and switch targets based on individual tabs in a tabbed application, thumbnail toolbars, notification and status overlays, and progress indicators.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-817"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist4"><strong>ITaskbarList4</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-817"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist4"><strong>ITaskbarList4</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-818">藉由提供可讓呼叫者控制索引標籤縮圖和預覽功能的兩個屬性值的方法，來擴充 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>ITaskbarList3</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="71ab3-818">Extends <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>ITaskbarList3</strong></a> by providing a method that allows the caller to control two property values for the tab thumbnail and peek feature.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-819"><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailcache"><strong>IThumbnailCache</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-819"><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailcache"><strong>IThumbnailCache</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-820">公開跨應用程式共用之系統縮圖快取的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-820">Exposes methods for a system thumbnail cache that is shared across applications.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-821"><a href="/windows/desktop/api/thumbcache/nn-thumbcache-ithumbnailcacheprimer"><strong>IThumbnailCachePrimer</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-821"><a href="/windows/desktop/api/thumbcache/nn-thumbcache-ithumbnailcacheprimer"><strong>IThumbnailCachePrimer</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-822"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ithumbnailhandlerfactory"><strong>IThumbnailHandlerFactory</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-822"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ithumbnailhandlerfactory"><strong>IThumbnailHandlerFactory</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-823">公開用來抓取專案縮圖處理常式的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-823">Exposes a method for retrieving the thumbnail handler of an item.</span></span> <span data-ttu-id="71ab3-824">如果您想要指定子 Idlist.txt 所使用的解壓縮程式，請執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="71ab3-824">Implement this interface if you want to specify what extractor is used for a child IDList.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-825"><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider"><strong>IThumbnailProvider</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-825"><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider"><strong>IThumbnailProvider</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-826">公開取得縮圖影像的方法，並將其設計為縮圖處理常式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-826">Exposes a method for getting a thumbnail image and is intended to be implemented for thumbnail handlers.</span></span> <span data-ttu-id="71ab3-827">執行這個介面的物件也必須執行 <a href="/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream"><strong>IInitializeWithStream</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="71ab3-827">The object that implements this interface must also implement <a href="/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream"><strong>IInitializeWithStream</strong></a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-828"><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailsettings"><strong>IThumbnailSettings</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-828"><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailsettings"><strong>IThumbnailSettings</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-829">提供方法，讓縮圖提供者判斷縮圖要求的使用者內容。</span><span class="sxs-lookup"><span data-stu-id="71ab3-829">Provides a method that enables a thumbnail provider to determine the user context of a thumbnail request.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-830"><a href="/windows/desktop/api/thumbnailstreamcache/nn-thumbnailstreamcache-ithumbnailstreamcache"><strong>IThumbnailStreamCache</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-830"><a href="/windows/desktop/api/thumbnailstreamcache/nn-thumbnailstreamcache-ithumbnailstreamcache"><strong>IThumbnailStreamCache</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-831">取得或設定縮圖資料流程。</span><span class="sxs-lookup"><span data-stu-id="71ab3-831">Gets or sets the thumbnail stream.</span></span> <span data-ttu-id="71ab3-832">這個介面僅供內部使用，而且只能由相片應用程式呼叫。</span><span class="sxs-lookup"><span data-stu-id="71ab3-832">This interface is for internal use only and can only be called by the photos application.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-833"><a href="/windows/desktop/api/Shdeprecated/nn-shdeprecated-itrackshellmenu"><strong>ITrackShellMenu</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-833"><a href="/windows/desktop/api/Shdeprecated/nn-shdeprecated-itrackshellmenu"><strong>ITrackShellMenu</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-834">公開擴充 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu"><strong>IShellMenu</strong></a> 介面的方法，方法是提供可協調工具列按鈕和功能表，以及顯示快顯功能表的功能。</span><span class="sxs-lookup"><span data-stu-id="71ab3-834">Exposes methods that extend the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu"><strong>IShellMenu</strong></a> interface by providing the ability to coordinate toolbar buttons with a menu as well as display a pop-up menu.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-835"><a href="/windows/desktop/api/Imagetranscode/nn-imagetranscode-itranscodeimage"><strong>ITranscodeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-835"><a href="/windows/desktop/api/Imagetranscode/nn-imagetranscode-itranscodeimage"><strong>ITranscodeImage</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-836">公開方法，這個方法可讓您從 Windows 支援的任何影像類型轉換成 JPEG 或點陣圖 (BMP) 影像格式。</span><span class="sxs-lookup"><span data-stu-id="71ab3-836">Exposes a method that allows conversion to JPEG or bitmap (BMP) image formats from any image type supported by Windows.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-837"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferadvisesink"><strong>ITransferAdviseSink</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-837"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferadvisesink"><strong>ITransferAdviseSink</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-838">公開支援狀態收集和失敗資訊的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-838">Exposes methods supporting status collection and failure information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-839"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination"><strong>ITransferDestination</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-839"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination"><strong>ITransferDestination</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-840">公開方法，以建立複製或移動作業的目的地 Shell 專案。</span><span class="sxs-lookup"><span data-stu-id="71ab3-840">Exposes methods that create a destination Shell item for a copy or move operation.</span></span> <span data-ttu-id="71ab3-841">提供此介面可提供 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransferdestination-advise"><strong>ITransferDestination：： Advise</strong></a> 方法，讓您更充分掌控檔案作業。</span><span class="sxs-lookup"><span data-stu-id="71ab3-841">This interface is provided to allow more control over file operations by providing an <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransferdestination-advise"><strong>ITransferDestination::Advise</strong></a> method.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-842"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfermediumitem"><strong>ITransferMediumItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-842"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfermediumitem"><strong>ITransferMediumItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-843">供複製引擎用來取得要呼叫 <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> 的專案，以傳回介面 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination"><strong>ITransferDestination</strong></a> 或介面 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource"><strong>ITransferSource</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="71ab3-843">Used by a copy engine to get the item on which to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> to return a pointer to interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination"><strong>ITransferDestination</strong></a> or interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource"><strong>ITransferSource</strong></a>.</span></span> <span data-ttu-id="71ab3-844">您可以查詢和列舉這些介面，以進行複製、移動或刪除作業。</span><span class="sxs-lookup"><span data-stu-id="71ab3-844">These interfaces can be queried and enumerated for copy, move, or delete operations.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-845"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource"><strong>ITransferSource</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-845"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource"><strong>ITransferSource</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-846">公開方法來操作 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>，包括複製、移動、回收和其他。</span><span class="sxs-lookup"><span data-stu-id="71ab3-846">Exposes methods to manipulate <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>, including copy, move, recycle, and others.</span></span> <span data-ttu-id="71ab3-847">提供此介面可提供 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-advise"><strong>ITransferSource：： Advise</strong></a> 方法來更充分掌控檔案作業。</span><span class="sxs-lookup"><span data-stu-id="71ab3-847">This interface is offered to provide more control over file operations by providing an <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-advise"><strong>ITransferSource::Advise</strong></a> method.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-848"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-itraydeskband"><strong>ITrayDeskBand</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-848"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-itraydeskband"><strong>ITrayDeskBand</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-849">公開顯示、隱藏和查詢 deskbands 的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-849">Exposes methods that show, hide, and query deskbands.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-850"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iupdateidlist"><strong>IUpdateIDList</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-850"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iupdateidlist"><strong>IUpdateIDList</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-851">提供方法來更新資料夾物件之子系的 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="71ab3-851">Provides a method to update the <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> of the child of an folder object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-852"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iurlsearchhook"><strong>IURLSearchHook</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-852"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iurlsearchhook"><strong>IURLSearchHook</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-853">公開瀏覽器用來轉譯未知 URL 通訊協定位址的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-853">Exposes a method that is used by the browser to translate the address of an unknown URL protocol.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-854"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iurlsearchhook2"><strong>IURLSearchHook2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-854"><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iurlsearchhook2"><strong>IURLSearchHook2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-855">公開一種方法，讓瀏覽器使用搜尋內容物件來轉譯未知 URL 通訊協定的位址。</span><span class="sxs-lookup"><span data-stu-id="71ab3-855">Exposes a method that is used by the browser to translate the address of an unknown URL protocol by using a search context object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-856"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iuseraccountchangecallback"><strong>IUserAccountChangeCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-856"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iuseraccountchangecallback"><strong>IUserAccountChangeCallback</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-857">公開方法，這個方法會在代表使用者帳戶的圖片變更時呼叫。</span><span class="sxs-lookup"><span data-stu-id="71ab3-857">Exposes a method which is called when the picture that represents a user account is changed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-858"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-858"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-859">公開設定通知資訊的方法，然後在與工作列的通知區域一起出現的氣球中，向使用者顯示該通知。</span><span class="sxs-lookup"><span data-stu-id="71ab3-859">Exposes methods that set notification information and then display that notification to the user in a balloon that appears in conjunction with the notification area of the taskbar.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="71ab3-860">
<a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2"><strong>IUserNotification2</strong></a> 與 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a> 的不同之處在于它的 <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-iusernotification2-show"><strong>Show</strong></a> 方法，它會針對回呼介面加入額外的參數，以與通知進行通訊。</span><span class="sxs-lookup"><span data-stu-id="71ab3-860">
<a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2"><strong>IUserNotification2</strong></a> differs from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a> only in its <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-iusernotification2-show"><strong>Show</strong></a> method, which adds an additional parameter for a callback interface to communicate with the notification.</span></span> <span data-ttu-id="71ab3-861">否則，表單和函式中的兩個介面都相同。</span><span class="sxs-lookup"><span data-stu-id="71ab3-861">Otherwise the two interfaces are identical in form and function.</span></span> <span data-ttu-id="71ab3-862">CLSID_UserNotification 會將這兩個版本的 <strong>顯示</strong> 為多載。</span><span class="sxs-lookup"><span data-stu-id="71ab3-862">CLSID_UserNotification implements both versions of <strong>Show</strong> as an overload.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-863"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2"><strong>IUserNotification2</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-863"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2"><strong>IUserNotification2</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-864">公開設定通知資訊的方法，然後在與工作列的通知區域一起出現的氣球中，向使用者顯示該通知。</span><span class="sxs-lookup"><span data-stu-id="71ab3-864">Exposes methods that set notification information and then display that notification to the user in a balloon that appears in conjunction with the notification area of the taskbar.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="71ab3-865">
<a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2"><strong>IUserNotification2</strong></a> 不會繼承自 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="71ab3-865">
<a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2"><strong>IUserNotification2</strong></a> does not inherit from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a>.</span></span> <span data-ttu-id="71ab3-866"><strong>IUserNotification2</strong> 與 <strong>IUserNotification</strong> 的不同之處在于它的 <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-iusernotification2-show"><strong>Show</strong></a> 方法，它會針對回呼介面加入額外的參數，以與通知進行通訊。</span><span class="sxs-lookup"><span data-stu-id="71ab3-866"><strong>IUserNotification2</strong> differs from <strong>IUserNotification</strong> only in its <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-iusernotification2-show"><strong>Show</strong></a> method, which adds an additional parameter for a callback interface to communicate with the notification.</span></span> <span data-ttu-id="71ab3-867">否則，表單和函式中的兩個介面都相同。</span><span class="sxs-lookup"><span data-stu-id="71ab3-867">Otherwise the two interfaces are identical in form and function.</span></span> <span data-ttu-id="71ab3-868">CLSID_UserNotification 會將這兩個版本的 <strong>顯示</strong> 為多載。</span><span class="sxs-lookup"><span data-stu-id="71ab3-868">CLSID_UserNotification implements both versions of <strong>Show</strong> as an overload.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-869"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotificationcallback"><strong>IUserNotificationCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-869"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotificationcallback"><strong>IUserNotificationCallback</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-870">公開在通知氣球中處理滑鼠按一下或快捷方式功能表存取的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-870">Exposes a method for the handling of a mouse click or shortcut menu access in a notification balloon.</span></span> <span data-ttu-id="71ab3-871">搭配 <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-iusernotification2-show"><strong>IUserNotification2：： Show</strong></a>使用。</span><span class="sxs-lookup"><span data-stu-id="71ab3-871">Used with <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-iusernotification2-show"><strong>IUserNotification2::Show</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-872"><a href="/windows/desktop/api/shobjidl/nn-shobjidl-iusetobrowseitem"><strong>IUseToBrowseItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-872"><a href="/windows/desktop/api/shobjidl/nn-shobjidl-iusetobrowseitem"><strong>IUseToBrowseItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-873">尋找流覽至此專案時應該使用的專案。</span><span class="sxs-lookup"><span data-stu-id="71ab3-873">Finds the item that should be used when browsing to this item.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-874"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iviewstateidentityitem"><strong>IViewStateIdentityItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-874"><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iviewstateidentityitem"><strong>IViewStateIdentityItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-875">提供標準的持續性專案，將會記住其 view 自訂專案。</span><span class="sxs-lookup"><span data-stu-id="71ab3-875">Provides a canonical persistence item, an item for which view customizations will be remembered.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-876"><a href="/windows/win32/api/shobjidl_core/nn-shobjidl_core-ivirtualdesktopmanager"><strong>IVirtualDesktopManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-876"><a href="/windows/win32/api/shobjidl_core/nn-shobjidl_core-ivirtualdesktopmanager"><strong>IVirtualDesktopManager</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-877">公開方法，讓應用程式與構成虛擬工作區的視窗群組進行互動。</span><span class="sxs-lookup"><span data-stu-id="71ab3-877">Exposes methods that enable an application to interact with groups of windows that form virtual workspaces.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-878"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ivisualproperties"><strong>IVisualProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-878"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ivisualproperties"><strong>IVisualProperties</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-879">公開設定和取得視覺屬性的方法。</span><span class="sxs-lookup"><span data-stu-id="71ab3-879">Exposes methods that set and get visual properties.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-880"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwebwizardextension"><strong>IWebWizardExtension</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-880"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwebwizardextension"><strong>IWebWizardExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-881">藉由公開方法來擴充 <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwizardextension"><strong>IWizardExtension</strong></a> 介面，以設定 wizard 擴充功能的初始 URL，以及在發生錯誤時使用特定的 url。</span><span class="sxs-lookup"><span data-stu-id="71ab3-881">Extends the <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwizardextension"><strong>IWizardExtension</strong></a> interface by exposing methods to set the wizard extension's initial URL, and a specific URL in case of an error.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-882"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwizardextension"><strong>IWizardExtension</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-882"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwizardextension"><strong>IWizardExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-883">由 Web 發佈嚮導和裝載伺服器端內容頁面的 [線上列印順序] Wizard 等的嚮導使用。</span><span class="sxs-lookup"><span data-stu-id="71ab3-883">Used by wizards such as the Web Publishing Wizard and Online Print Ordering Wizard which host server-side content pages.</span></span> <span data-ttu-id="71ab3-884">這個介面會公開方法，以指定支援的延伸模組頁面，以及流覽和移出這些頁面。</span><span class="sxs-lookup"><span data-stu-id="71ab3-884">This interface exposes methods to specify supported extension pages and to navigate into and out of those pages.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ab3-885"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwizardsite"><strong>IWizardSite</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-885"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwizardsite"><strong>IWizardSite</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-886">公開 wizard 擴充功能所使用的方法，以導覽其本身和嚮導其餘部分之間的框線。</span><span class="sxs-lookup"><span data-stu-id="71ab3-886">Exposes methods used by a wizard extension to navigate the borders between itself and the rest of the wizard.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ab3-887"><a href="taskcompletionclient.md"><strong>TaskCompletionClient</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ab3-887"><a href="taskcompletionclient.md"><strong>TaskCompletionClient</strong></a></span></span><br/></td>
<td><span data-ttu-id="71ab3-888">啟用工作完成。</span><span class="sxs-lookup"><span data-stu-id="71ab3-888">Enables task completion.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

 

 