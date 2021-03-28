---
description: 本節說明 Windows Shell 常數、列舉和旗標。
title: Shell 常數、列舉和旗標
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 638beaa7-a065-4ab3-8eb5-286a306a8f24
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2070ef1acc37262a526186862f46afa002c47343
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104195649"
---
# <a name="shell-constants-enumerations-and-flags"></a>Shell 常數、列舉和旗標

本節說明 Windows Shell 常數、列舉和旗標。

## <a name="in-this-section"></a>本節內容



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_svgio"><strong>_SVGIO</strong></a><br/></td>
<td>搭配 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-items"><strong>IFolderView：： Items</strong></a>、 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-itemcount"><strong>IFolderView：： ItemCount</strong></a>和 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getitemobject"><strong>IShellView：： GetItemObject</strong></a> 方法使用，以限制或控制其集合中的專案。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_svsif"><strong>_SVSIF</strong></a><br/></td>
<td>表示 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview"><strong>IFolderView</strong></a>、 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview2"><strong>IFolderView2</strong></a>、 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2"><strong>IShellView2</strong></a> 所使用的旗標，以指定要套用的選取專案類型。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shappmgr/ne-shappmgr-appactionflags"><strong>APPACTIONFLAGS</strong></a><br/></td>
<td>指定應用程式發行者所支援的應用程式管理動作。 這些旗標是傳遞給 <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-ishellapp-getpossibleactions"><strong>IShellApp：： GetPossibleActions</strong></a>的位元遮罩。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shappmgr/ne-shappmgr-appinfodataflags"><strong>APPINFODATAFLAGS</strong></a><br/></td>
<td>指定要從 <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-ishellapp-getappinfo"><strong>IShellApp：： GetAppInfo</strong></a>傳回的應用程式資訊。 這些旗標是在<strong>APPINFODATA</strong>結構的<a href="/windows/desktop/api/Shappmgr/ns-shappmgr-appinfodata"><strong>dwMask</strong></a>成員中使用的位元遮罩。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ne-shobjidl_core-application_view_orientation"><strong>APPLICATION_VIEW_ORIENTATION</strong></a><br/></td>
<td>為視窗 (應用程式視圖) 定義一組顯示方向模式。 由 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings2-getapplicationvieworientation"><strong>IApplicationDesignModeSettings2：： GetApplicationViewOrientation</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings2-setapplicationvieworientation"><strong>IApplicationDesignModeSettings2：： SetApplicationViewOrientation</strong></a>使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ne-shobjidl_core-application_view_size_preference"><strong>APPLICATION_VIEW_SIZE_PREFERENCE</strong></a><br/></td>
<td>定義可能的一般視窗 (應用程式視圖) 大小喜好設定。 由 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ilaunchsourceviewsizepreference-getsourceviewsizepreference"><strong>ILaunchSourceViewSizePreference：： GetSourceViewSizePreference</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ilaunchtargetviewsizepreference-gettargetviewsizepreference"><strong>ILaunchTargetViewSizePreference：： GetTargetViewSizePreference</strong></a>使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-application_view_state"><strong>APPLICATION_VIEW_STATE</strong></a><br/></td>
<td>指出 Windows Store 應用程式目前的檢視狀態。 由 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-setapplicationviewstate"><strong>IApplicationDesignModeSettings：： SetApplicationViewState</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-isapplicationviewstatesupported"><strong>IApplicationDesignModeSettings：： IsApplicationViewStateSupported</strong></a>使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-assocdata"><strong>ASSOCDATA</strong></a><br/></td>
<td>供 <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getdata"><strong>IQueryAssociations：：：</strong></a> 定義要傳回之資料的類型。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/shell/assocf_str"><strong>ASSOCF</strong></a><br/></td>
<td>提供 <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a> 介面方法的資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel"><strong>ASSOCIATIONLEVEL</strong></a><br/></td>
<td>指定副檔名的預設關聯來源。 由 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>IApplicationAssociationRegistration</strong></a> 介面的方法所使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype"><strong>ASSOCIATIONTYPE</strong></a><br/></td>
<td>指定應用程式的關聯類型。 由 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>IApplicationAssociationRegistration</strong></a> 介面的方法所使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-assockey"><strong>ASSOCKEY</strong></a><br/></td>
<td>指定要由 <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getkey"><strong>IQueryAssociations：： GetKey</strong></a>傳回的索引鍵類型。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr"><strong>ASSOCSTR</strong></a><br/></td>
<td>由 <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getstring"><strong>IQueryAssociations：： GetString</strong></a> 用來定義要傳回之字串的型別。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-attachment_action"><strong>ATTACHMENT_ACTION</strong></a><br/></td>
<td>提供一組要搭配 IAttachmentExecute 使用的旗標 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-prompt"><strong>：:P 提示 r) </strong></a> ，以指出要在使用者確認時執行的動作。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-attachment_prompt"><strong>ATTACHMENT_PROMPT</strong></a><br/></td>
<td>提供一組要搭配 IAttachmentExecute 使用的旗標 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-prompt"><strong>：:P 提示 r) </strong></a> ，以指出要顯示的提示 UI 類型。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ne-shlobj_core-autocompletelistoptions"><strong>AUTOCOMPLETELISTOPTIONS</strong></a><br/></td>
<td>指定要列舉自動完成清單的物件。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shldisp/ne-shldisp-autocompleteoptions"><strong>AUTOCOMPLETEOPTIONS</strong></a><br/></td>
<td>針對 [自動完成] 周圍的選項，指定 <a href="/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-getoptions"><strong>IAutoComplete2：： GetOptions</strong></a> 和 <a href="/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions"><strong>IAutoComplete2：： >setoptions</strong></a> 所使用的值。<br/></td>
</tr>
<tr class="even">
<td><a href="str-constants.md"><strong>系結內容字串索引鍵</strong></a><br/></td>
<td>搭配 <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx：： RegisterObjectParam</strong></a> 方法用來指定系結內容的一組字串索引鍵。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shdeprecated/ne-shdeprecated-bnstate"><strong>BNSTATE</strong></a><br/></td>
<td>已取代。 由 <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice-setnavigatestate"><strong>IBrowserService：： SetNavigateState</strong></a> 和 <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice-getnavigatestate"><strong>IBrowserService：： GetNavigateState</strong></a> 用來指定流覽狀態。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ne-shobjidl_core-_browserframeoptions"><strong>BROWSERFRAMEOPTIONS</strong></a><br/></td>
<td>與方法 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibrowserframeoptions-getframeoptions"><strong>IBrowserFrameOptions：： GetFrameOptions</strong></a>搭配使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-categoryinfo_flags"><strong>CATEGORYINFO_FLAGS</strong></a><br/></td>
<td>提供一組用於 <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-category_info"><strong>CATEGORY_INFO</strong></a> 結構的旗標。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-catsort_flags"><strong>CATSORT_FLAGS</strong></a><br/></td>
<td>指定排序類別目錄資料的方法。<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb762483(v=vs.85)"><strong>CDCONTROLSTATE</strong></a><br/></td>
<td>指定值，指出控制項是否可見且已啟用。 供 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize"><strong>IFileDialogCustomize</strong></a> 介面的成員使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_enum_flags"><strong>CM_ENUM_FLAGS</strong></a><br/></td>
<td>供 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>IColumnManager</strong></a> 介面的成員用來指定所要求的資料行集，不論是目前可見的資料行。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_mask"><strong>CM_MASK</strong></a><br/></td>
<td>表示在呼叫<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icolumnmanager-setcolumninfo"><strong>IColumnManager：： SetColumnInfo</strong></a>期間應設定<a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a>結構中的哪些值。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_set_width_value"><strong>CM_SET_WIDTH_VALUE</strong></a><br/></td>
<td>指定寬度值（以圖元為單位），並包含預設和自動調整的特殊支援。 由 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>IColumnManager</strong></a> 介面的成員透過 <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a> 結構使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_state"><strong>CM_STATE</strong></a><br/></td>
<td>指定資料行狀態值。 由 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>IColumnManager</strong></a> 介面的成員透過 <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a> 結構使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/CredentialProvider/ne-credentialprovider-credential_provider_account_options"><strong>CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS</strong></a><br/></td>
<td>指出認證提供者應該傳回的認證類型，以與 &quot; 其他使用者磚產生關聯 &quot; 。 由 <a href="/windows/desktop/api/CredentialProvider/nf-credentialprovider-icredentialprovideruserarray-getaccountoptions"><strong>ICredentialProviderUserArray_GetAccountOptions</strong></a>使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/ne-credentialprovider-credential_provider_credential_field_options"><strong>CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS</strong></a><br/></td>
<td>提供登入或認證 UI 中單一欄位的自訂選項。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_field_interactive_state"><strong>CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE</strong></a><br/></td>
<td>描述欄位的狀態以及使用者可以如何與其互動。 欄位可以由各種不同互動狀態中的認證提供者來顯示。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_field_state"><strong>CREDENTIAL_PROVIDER_FIELD_STATE</strong></a><br/></td>
<td>指定認證 UI 中單一欄位的狀態。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_field_type"><strong>CREDENTIAL_PROVIDER_FIELD_TYPE</strong></a><br/></td>
<td>指定認證欄位的類型。 由 <a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_field_descriptor"><strong>CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</strong></a>使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_get_serialization_response"><strong>CREDENTIAL_PROVIDER_GET_SERIALIZATION_RESPONSE</strong></a><br/></td>
<td>描述認證提供者嘗試序列化認證時的回應。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_status_icon"><strong>CREDENTIAL_PROVIDER_STATUS_ICON</strong></a><br/></td>
<td>指出應該顯示的狀態圖示。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_usage_scenario"><strong>CREDENTIAL_PROVIDER_USAGE_SCENARIO</strong></a><br/></td>
<td>宣告支援認證提供者的案例。  (CPU 的認證提供者使用案例) 可讓認證提供者跨案例提供不同的列舉行為和 UI 欄位設定。<br/></td>
</tr>
<tr class="even">
<td><a href="csidl.md"><strong>CSIDL</strong></a><br/></td>
<td><blockquote>
<p><b>注意： </b>在 Windows Vista 中，這些值已由 <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a> 值取代。 如需新的常數及其對應的 CSIDL 值清單，請參閱該主題。 為了方便起見，此處也會針對每個 CSIDL 值注明對應的 <strong>KNOWNFOLDERID</strong> 值。</p>
<p>基於相容性因素，Windows Vista 支援 CSIDL 系統。 不過，新的開發應該使用 <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a> 值，而不是 CSIDL 值。<br/></p>
</blockquote>
<br/> CSIDL (固定的特殊專案識別碼清單) 值提供獨特的系統獨立方式來識別應用程式經常使用的特殊資料夾，但在任何指定的系統上可能不會有相同的名稱或位置。 例如，系統資料夾可能是 &quot; &quot; 一個系統上的 C：\Windows，並 &quot; &quot; 在另一個系統上 C:\Winnt。 這些常數定義于 Shlobj.h 中。<br/></td>
</tr>
<tr class="odd">
<td><a href="ctf.md"><strong>CTF 旗標</strong></a><br/></td>
<td>控制呼叫函式行為的旗標。 由 <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread"><strong>SHCreateThread</strong></a> 和 <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadwithhandle"><strong>SHCreateThreadWithHandle</strong></a>使用。 在這些函數中，這些值會定義為 SHCT_FLAGS 類型。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-dataobj_get_item_flags"><strong>DATAOBJ_GET_ITEM_FLAGS</strong></a><br/></td>
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromdataobject"><strong>SHGetItemFromDataObject</strong></a>函數用來指定有關處理來源物件之選項的值。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-tagdeskbandcid"><strong>DBID 命令旗標</strong></a><br/></td>
<td>您可以使用 <a href="/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-exec"><strong>IOleCommandTarget：： Exec</strong></a>將這些命令識別碼傳送至帶狀物件的容器。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-def_share_id"><strong>DEF_SHARE_ID</strong></a><br/></td>
<td>值，指定 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isharingconfigurationmanager"><strong>ISharingConfigurationManager</strong></a> 介面的方法所處理的資料夾。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype"><strong>DEFAULTSAVEFOLDERTYPE</strong></a><br/></td>
<td>指定預設的儲存位置。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-default_folder_menu_restrictions"><strong>DEFAULT_FOLDER_MENU_RESTRICTIONS</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-desktop_wallpaper_position"><strong>DESKTOP_WALLPAPER_POSITION</strong></a><br/></td>
<td>指定桌面壁紙的顯示方式。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shtypes/ne-shtypes-device_scale_factor"><strong>DEVICE_SCALE_FACTOR</strong></a><br/></td>
<td>表示詐騙裝置縮放比例，以百分比表示。 由<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-setapplicationviewstate"><strong>IApplicationDesignModeSettings：： SetApplicationViewState</strong></a>和<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-isapplicationviewstatesupported"><strong>IApplicationDesignModeSettings：： IsApplicationViewStateSupported</strong></a>使用<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/ne-shellscalingapi-display_device_type"><strong>DISPLAY_DEVICE_TYPE</strong></a><br/></td>
<td>指出裝置是否為主要或沉浸式顯示器類型。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype"><strong>DROPIMAGETYPE</strong></a><br/></td>
<td>搭配 <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription"><strong>DROPDESCRIPTION</strong></a> 結構使用的值，以指定卸載映射。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_expcmdstate"><strong>EXPCMDSTATE</strong></a><br/></td>
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_expcmdstate"><strong>EXPCMDSTATE</strong></a> 值代表 Shell 專案的命令狀態。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_fill_flags"><strong>EXPLORER_BROWSER_FILL_FLAGS</strong></a><br/></td>
<td>這些旗標會搭配 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-fillfromobject"><strong>IExplorerBrowser：： FillFromObject</strong></a>使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_options"><strong>EXPLORER_BROWSER_OPTIONS</strong></a><br/></td>
<td>這些旗標會搭配 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-getoptions"><strong>IExplorerBrowser：： GetOptions</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-setoptions"><strong>IExplorerBrowser：： >setoptions</strong></a>使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_explorerpanestate"><strong>EXPLORERPANESTATE</strong></a><br/></td>
<td>指出 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate"><strong>IExplorerPaneVisibility：： GetPaneState</strong></a> 所使用的旗標，以取得指定 Windows 檔案總管窗格的目前狀態。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fdap"><strong>FDAP</strong></a><br/></td>
<td>指定清單位置。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fde_overwrite_response"><strong>FDE_OVERWRITE_RESPONSE</strong></a><br/></td>
<td>指定 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onoverwrite"><strong>IFileDialogEvents：： OnOverwrite</strong></a> 方法所使用的值，以指出應用程式在使用 [一般檔案] 對話方塊進行儲存作業期間對覆寫要求的回應。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fde_shareviolation_response"><strong>FDE_SHAREVIOLATION_RESPONSE</strong></a><br/></td>
<td>指定 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onshareviolation"><strong>IFileDialogEvents：： OnShareViolation</strong></a> 方法所使用的值，以指出應用程式對檔案開啟或儲存時發生的共用違規回應。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fffp_mode"><strong>FFFP_MODE</strong></a><br/></td>
<td>描述項合準則。 由 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager"><strong>IKnownFolderManager</strong></a> 介面的方法所使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-file_usage_type"><strong>FILE_USAGE_TYPE</strong></a><br/></td>
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileisinuse-getusage"><strong>IFileIsInUse：： GetUsage</strong></a>所使用的常數，表示使用中的檔案。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_fileopendialogoptions"><strong>FILEOPENDIALOGOPTIONS</strong></a><br/></td>
<td>定義可用來開啟或儲存對話方塊的選項組。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a><br/></td>
<td>表示在檔案關聯<a href="fa-progids.md">PROGID</a>登錄機碼的 EditFlags 值中所使用的<a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a>常數。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folder_enum_mode"><strong>FOLDER_ENUM_MODE</strong></a><br/></td>
<td>由 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithfolderenummode-getmode"><strong>IObjectWithFolderEnumMode：： GetMode</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithfolderenummode-setmode"><strong>IObjectWithFolderEnumMode：： SetMode</strong></a> 方法用來取得及設定資料夾的顯示模式。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderflags"><strong>FOLDERFLAGS</strong></a><br/></td>
<td>指定資料夾檢視選項的一組旗標。 旗標彼此獨立，而且可用於任何組合。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderlogicalviewmode"><strong>FOLDERLOGICALVIEWMODE</strong></a><br/></td>
<td>由 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderviewsettings-getviewmode"><strong>IFolderViewSettings：： GetViewMode</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-setfolderlogicalviewmode"><strong>ISearchFolderItemFactory：： SetFolderLogicalViewMode</strong></a> 用來描述 view 模式。<br/></td>
</tr>
<tr class="odd">
<td><a href="foldertypeid.md"><strong>FOLDERTYPEID</strong></a><br/></td>
<td><a href="foldertypeid.md"><strong>FOLDERTYPEID</strong></a>值代表套用至資料夾的視圖範本，通常是根據其預定用途和內容。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode"><strong>FOLDERVIEWMODE</strong></a><br/></td>
<td>指定資料夾檢視類型。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-folderviewoptions"><strong>FOLDERVIEWOPTIONS</strong></a><br/></td>
<td>由 <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifolderviewoptions"><strong>IFolderViewOptions</strong></a> 介面的方法用來啟用 windows 7 及更新版本系統中預設不支援的 windows Vista 選項，以及停用新的 windows 7 選項。<br/></td>
</tr>
<tr class="even">
<td><a href="iactivedesktop-flags.md"><strong>IActiveDesktop 旗標</strong></a><br/></td>
<td>本節描述 <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop"><strong>IActiveDesktop</strong></a> 介面方法所使用的旗標。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ne-shlobj_core-ieshortcutflags"><strong>IESHORTCUTFLAGS</strong></a><br/></td>
<td>指定瀏覽器如何處理快捷方式。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category"><strong>KF_CATEGORY</strong></a><br/></td>
<td>值，表示可分類為已知資料夾系統註冊之資料夾的類別。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_kf_definition_flags"><strong>KF_DEFINITION_FLAGS</strong></a><br/></td>
<td>指定特定已知資料夾行為的旗標。 搭配 <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition"><strong>KNOWNFOLDER_DEFINITION</strong></a> 結構使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_kf_redirect_flags"><strong>KF_REDIRECT_FLAGS</strong></a><br/></td>
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-redirect"><strong>IKnownFolderManager：：重新導向</strong></a>所使用的旗標，可指定已知資料夾重新導向的詳細資料，例如重新導向資料夾的許可權和擁有權。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_kf_redirection_capabilities"><strong>KF_REDIRECTION_CAPABILITIES</strong></a><br/></td>
<td>旗標，指定已知資料夾目前的重新導向功能。 由 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getredirectioncapabilities"><strong>IKnownFolder：： GetRedirectionCapabilities</strong></a>使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag"><strong>KNOWN_FOLDER_FLAG</strong></a><br/></td>
<td>指定已知資料夾的特殊抓取選項。 這些值會取代具有平行意義的 <a href="csidl.md"><strong>CSIDL</strong></a> 值。<br/></td>
</tr>
<tr class="odd">
<td><a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a><br/></td>
<td><a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a>常數代表 guid，可識別以<a href="known-folders.md">已知的資料夾</a>向系統註冊的標準資料夾。 這些資料夾會與 Windows Vista 和更新版本的作業系統一起安裝，而電腦將只會有適合安裝的資料夾。 如需這些資料夾的說明，請參閱 <a href="csidl.md"><strong>CSIDL</strong></a>。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryfolderfilter"><strong>LIBRARYFOLDERFILTER</strong></a><br/></td>
<td>定義篩選資料夾專案的選項。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarymanagedialogoptions"><strong>LIBRARYMANAGEDIALOGOPTIONS</strong></a><br/></td>
<td>供 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shshowmanagelibraryui"><strong>SHShowManageLibraryUI</strong></a> 用來定義儲存程式庫時處理名稱衝突的選項。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryoptionflags"><strong>LIBRARYOPTIONFLAGS</strong></a><br/></td>
<td>指定程式庫選項。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarysaveflags"><strong>LIBRARYSAVEFLAGS</strong></a><br/></td>
<td>指定儲存程式庫時，用來處理名稱衝突的選項。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Intshcut/ne-intshcut-mimeassociationdialog_in_flags"><strong>MIMEASSOCIATIONDIALOG_IN_FLAGS</strong></a><br/></td>
<td>搭配 <a href="/windows/desktop/api/Intshcut/nf-intshcut-mimeassociationdialoga"><strong>MIMEAssociationDialog</strong></a> 函式使用，以判斷其執行方式。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-monitor_app_visibility"><strong>MONITOR_APP_VISIBILITY</strong></a><br/></td>
<td>指定顯示畫面是否顯示桌面 windows，而非 Windows Store 應用程式。<br/></td>
</tr>
<tr class="even">
<td><a href="mp-popupflags.md"><strong>MP_POPUPFLAGS 常數</strong></a><br/></td>
<td>表示顯示快顯功能表時可用的選項。<br/></td>
</tr>
<tr class="odd">
<td><a href="net-string.md"><strong>NET_STRING</strong></a><br/></td>
<td>代表網路位址類型。 使用一或多個 (作為下列常數的位元組合) ，以建立與宏 <a href="/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype"><strong>NetAddr_SetAllowType</strong></a>搭配使用的網路位址遮罩。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-nstcfoldercapabilities"><strong>NSTCFOLDERCAPABILITIES</strong></a><br/></td>
<td>指定樹狀目錄專案的狀態。 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrolfoldercapabilities"><strong>INameSpaceTreeControlFolderCapabilities</strong></a>介面的方法會使用這些值。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_nstcitemstate"><strong>NSTCITEMSTATE</strong></a><br/></td>
<td>指定樹狀目錄專案的狀態。 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>INameSpaceTreeControl</strong></a>介面的方法會使用這些值。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_nstcstyle"><strong>NSTCSTYLE</strong></a><br/></td>
<td>描述給定命名空間樹狀目錄控制項的特性。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-nstcstyle2"><strong>NSTCSTYLE2</strong></a><br/></td>
<td>由 <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrol2"><strong>INameSpaceTreeControl2</strong></a> 的方法用來指定 Shell 命名空間 treeview 中的擴充顯示樣式。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-nwmf"><strong>NWMF</strong></a><br/></td>
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inewwindowmanager-evaluatenewwindow"><strong>INewWindowManager：： EvaluateNewWindow</strong></a>所使用的旗標。 這些值是決定是否要顯示快顯視窗的因素。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-package_execution_state"><strong>PACKAGE_EXECUTION_STATE</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/win32/api/shtypes/ne-shtypes-perceived"><strong>認為</strong></a><br/></td>
<td>指定檔案的認知型別。 <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype"><strong>AssocGetPerceivedType</strong></a>函式中會使用這組常數。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shappmgr/ne-shappmgr-pubappinfoflags"><strong>PUBAPPINFOFLAGS</strong></a><br/></td>
<td>指定 <a href="/windows/desktop/api/Shappmgr/ns-shappmgr-pubappinfo"><strong>PUBAPPINFO</strong></a> 結構中的哪些成員有效。 這些旗標是在 <strong>dwMask</strong> 成員中設定的位元遮罩，而且會傳遞至 <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-ipublishedapp-getpublishedappinfo"><strong>IPublishedApp：： GetPublishedAppInfo</strong></a>。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ne-shellapi-query_user_notification_state"><strong>QUERY_USER_NOTIFICATION_STATE</strong></a><br/></td>
<td>指定目前使用者的電腦狀態，與傳送通知的專利有關。 由 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate"><strong>SHQueryUserNotificationState</strong></a>使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="hkey-type.md"><strong>登錄資料類型</strong></a><br/></td>
<td>這些資料類型可以用來指定登錄值的型別。<br/></td>
</tr>
<tr class="even">
<td><a href="regsam.md"><strong>REGSAM</strong></a><br/></td>
<td>用來指定登錄中安全性存取屬性的資料類型。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions"><strong>限制</strong></a><br/></td>
<td>這些旗標會搭配 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shrestricted"><strong>SHRestricted</strong></a> 函式使用。 <strong>SHRestricted</strong> 用來判斷指定的系統管理員原則是否有效。 在許多情況下，應用程式必須修改某些行為，才能符合系統管理員所制訂的原則。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ShellScalingAPI/ne-shellscalingapi-scale_change_flags"><strong>SCALE_CHANGE_FLAGS</strong></a><br/></td>
<td>用來表示發生的調整變更的旗標。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-scnrt_status"><strong>SCNRT_STATUS</strong></a><br/></td>
<td>指出是否要啟用或停用 <a href="/windows/desktop/api/Shlobj/nf-shlobj-shchangenotifyregisterthread"><strong>SHChangeNotifyRegisterThread</strong></a>的 Async Register 和取消註冊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-tagsfbs_flags"><strong>SFBS_FLAGS</strong></a><br/></td>
<td>指定 <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a> 函數應該如何處理 undisplayed 數位的舍入。<br/></td>
</tr>
<tr class="odd">
<td><a href="sfgao.md"><strong>SFGAO</strong></a><br/></td>
<td>可以在專案 (檔案或資料夾) 或一組專案上抓取的屬性。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-shard"><strong>碎片</strong></a><br/></td>
<td>表示 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> 在其 <em>pv</em> 參數中所傳遞之資料的解讀，以識別正在追蹤其使用統計資料的專案。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-share_role"><strong>SHARE_ROLE</strong></a><br/></td>
<td>指定指派給 <strong>使用者</strong> 或 <strong>公用</strong> 資料夾的存取權限。 用於 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isharingconfigurationmanager-createshare"><strong>CreateShare</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isharingconfigurationmanager-getsharepermissions"><strong>GetSharePermissions</strong></a>。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shtypes/ne-shtypes-shcolstate"><strong>SHCOLSTATE</strong></a><br/></td>
<td>描述如何處理屬性。 這些值定義于 Shtypes.idl 中。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_shcontf"><strong>SHCONTF</strong></a><br/></td>
<td>決定列舉中包含的專案類型。 這些值會搭配 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>IShellFolder：： EnumObjects</strong></a> 方法使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-shell_link_data_flags"><strong>SHELL_LINK_DATA_FLAGS</strong></a><br/></td>
<td>指定選項設定。 搭配 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinkdatalist-getflags"><strong>IShellLinkDataList：： GetFlags</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinkdatalist-setflags"><strong>IShellLinkDataList：： SetFlags</strong></a>使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-shell_ui_component"><strong>SHELL_UI_COMPONENT</strong></a><br/></td>
<td>識別 shell 中所需的 UI 元件類型。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shldisp/ne-shldisp-shellfolderviewoptions"><strong>ShellFolderViewOptions</strong></a><br/></td>
<td>指定 <a href="shellfolderview-viewoptions.md"><strong>ViewOptions</strong></a> 屬性所傳回的視圖選項。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants"><strong>ShellSpecialFolderConstants</strong></a><br/></td>
<td>指定可識別特殊資料夾的唯一、系統獨立值。 這些資料夾經常是由應用程式使用，但在任何指定的系統上可能不會有相同的名稱或位置。 例如，系統資料夾可以是 &quot; &quot; 一個系統上的 C：\Windows，並 &quot; &quot; 在另一個系統上 C:\Winnt。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ExDisp/ne-exdisp-shellwindowfindwindowoptions"><strong>ShellWindowFindWindowOptions</strong></a><br/></td>
<td>指定在 Shell windows 集合中尋找視窗的選項。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Exdisp/ne-exdisp-shellwindowtypeconstants"><strong>ShellWindowTypeConstants</strong></a><br/></td>
<td>指定 Shell 視窗的類型。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_shgdnf"><strong>SHGDNF</strong></a><br/></td>
<td>定義與 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder：： GetDisplayNameOf</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-setnameof"><strong>IShellFolder：： SetNameOf</strong></a> 方法搭配使用的值，以指定這些方法所使用的檔案或資料夾名稱類型。 <br/>
<blockquote>
<b>注意：</b><br />
在 Windows 7 之前，這些值已封裝為 SHGNO 列舉。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-shglobalcounter"><strong>SHGLOBALCOUNTER</strong></a><br/></td>
<td>各種全域計數器或共用變數的識別碼。 每個全域計數器都可以使用 <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shglobalcounterincrement"><strong>SHGlobalCounterIncrement</strong></a> 和 <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shglobalcounterdecrement"><strong>SHGlobalCounterDecrement</strong></a>來遞增或遞減。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-shregdel_flags"><strong>SHREGDEL_FLAGS</strong></a><br/></td>
<td>提供一組值，這些值會指出將刪除專案的基底索引鍵。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-shregenum_flags"><strong>SHREGENUM_FLAGS</strong></a><br/></td>
<td>提供一組值，這些值表示將用於列舉的基底索引鍵。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ne-shellapi-shstockiconid"><strong>SHSTOCKICONID</strong></a><br/></td>
<td>供 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>SHGetStockIconInfo</strong></a> 用來識別要取出的存貨系統圖示。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_sichintf"><strong>SICHINTF</strong></a><br/></td>
<td>用來決定如何比較兩個 Shell 專案。 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-compare"><strong>IShellItem：： Compare</strong></a> 會使用這個列舉型別。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-sigdn"><strong>SIGDN</strong></a><br/></td>
<td>要求透過 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname"><strong>IShellItem：： GetDisplayName</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetnamefromidlist"><strong>SHGetNameFromIDList</strong></a>取得專案的顯示名稱格式。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-spaction"><strong>SPACTION</strong></a><br/></td>
<td>描述要執行的動作，此動作需要使用 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress"><strong>IActionProgress</strong></a> 介面向使用者顯示進度。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_spbeginf"><strong>SPBEGINF</strong></a><br/></td>
<td>由 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iactionprogress-begin"><strong>IActionProgress：： Begin</strong></a>使用，這些常數會指定要啟用或停用的特定 UI 作業。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-sptext"><strong>SPTEXT</strong></a><br/></td>
<td>指定要提供給 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress"><strong>IActionProgress</strong></a> 介面的描述性文字類型。<br/></td>
</tr>
<tr class="even">
<td><a href="srrf.md"><strong>SRRF</strong></a><br/></td>
<td>限制要設定或傳回之資料的旗標。<br/></td>
</tr>
<tr class="odd">
<td><a href="ssf-constants.md"><strong>SSF 常數</strong></a><br/></td>
<td>由 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings"><strong>SHGetSetSettings</strong></a> 函數用來指定應設定或擷取其 <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellstatea"><strong>SHELLSTATE</strong></a> 結構的成員。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-stpflag"><strong>STPFLAG</strong></a><br/></td>
<td>由 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist4-settabproperties"><strong>ITaskbarList4：： SetTabProperties</strong></a> 方法用來指定索引標籤屬性。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-svuia_status"><strong>SVUIA_STATUS</strong></a><br/></td>
<td>與 <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-_uiactivateview"><strong>IBrowserService2：： _UIActivateView</strong></a> 方法搭配使用，以設定瀏覽器視圖的狀態。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_cancel_request"><strong>SYNCMGR_CANCEL_REQUEST</strong></a><br/></td>
<td>描述使用者取消同步處理的要求。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_conflict_item_type"><strong>SYNCMGR_CONFLICT_ITEM_TYPE</strong></a><br/></td>
<td>描述衝突專案類型。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_control_flags"><strong>SYNCMGR_CONTROL_FLAGS</strong></a><br/></td>
<td>指定如何執行在 <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrcontrol"><strong>ISyncMgrControl</strong></a> 特定方法上所要求的作業。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_event_flags"><strong>SYNCMGR_EVENT_FLAGS</strong></a><br/></td>
<td>指定同步處理事件的旗標。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_event_level"><strong>SYNCMGR_EVENT_LEVEL</strong></a><br/></td>
<td>指定回報給同步中心的事件種類。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_handler_capabilities"><strong>SYNCMGR_HANDLER_CAPABILITIES</strong></a><br/></td>
<td>指定處理常式的功能，其與可對其執行的動作有關。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_handler_policies"><strong>SYNCMGR_HANDLER_POLICIES</strong></a><br/></td>
<td>列舉偏離預設原則的同步處理處理常式所指定的原則。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_handler_type"><strong>SYNCMGR_HANDLER_TYPE</strong></a><br/></td>
<td>指定處理常式的類型。 由 <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrhandlerinfo-gettype"><strong>ISyncMgrHandlerInfo：： GetType</strong></a>使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_item_capabilities"><strong>SYNCMGR_ITEM_CAPABILITIES</strong></a><br/></td>
<td>指定可針對專案執行的動作。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_item_policies"><strong>SYNCMGR_ITEM_POLICIES</strong></a><br/></td>
<td>指定專案的原則，以控制群組原則可以啟用或停用它們的方式。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_presenter_choice"><strong>SYNCMGR_PRESENTER_CHOICE</strong></a><br/></td>
<td>描述使用者對同步管理員衝突解決所做的選擇。 由 <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictpresenter"><strong>ISyncMgrConflictPresenter</strong></a>使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_presenter_next_step"><strong>SYNCMGR_PRESENTER_NEXT_STEP</strong></a><br/></td>
<td>描述在同步管理員衝突解決中所發生的下一個步驟。 由 <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictpresenter"><strong>ISyncMgrConflictPresenter</strong></a>使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_progress_status"><strong>SYNCMGR_PROGRESS_STATUS</strong></a><br/></td>
<td>指定同步處理常式目前的進度狀態。 由 <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsynccallback-reportprogress"><strong>ISyncMgrSyncCallback：： >reportprogress</strong></a>使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_resolution_abilities"><strong>SYNCMGR_RESOLUTION_ABILITIES</strong></a><br/></td>
<td>指出要遵循的功能和衝突解決活動。 搭配 <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrresolutionhandler-queryabilities"><strong>ISyncMgrResolutionHandler：： QueryAbilities</strong></a>使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_resolution_feedback"><strong>SYNCMGR_RESOLUTION_FEEDBACK</strong></a><br/></td>
<td>描述同步處理管理員的解決意見反應。 由 <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrresolutionhandler"><strong>ISyncMgrResolutionHandler</strong></a>使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_sync_control_flags"><strong>SYNCMGR_SYNC_CONTROL_FLAGS</strong></a><br/></td>
<td>表示 <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-starthandlersync"><strong>ISyncMgrControl：： StartHandlerSync</strong></a> 和 <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-startitemsync"><strong>ISyncMgrControl：： StartItemSync</strong></a>所使用的旗標。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrflag"><strong>SYNCMGRFLAG</strong></a><br/></td>
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrflag"><strong>SYNCMGRFLAG</strong></a>列舉值會用在<a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-initialize"><strong>ISyncMgrSynchronize：： Initialize</strong></a>方法中，以指出如何起始同步處理事件。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrhandlerflags"><strong>SYNCMGRHANDLERFLAGS</strong></a><br/></td>
<td>使用於 <a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrhandlerinfo"><strong>SYNCMGRHANDLERINFO</strong></a> 結構中做為套用至目前處理常式的旗標。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrinvokeflags"><strong>SYNCMGRINVOKEFLAGS</strong></a><br/></td>
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrinvokeflags"><strong>SYNCMGRINVOKEFLAGS</strong></a>列舉值會指定如何在<a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizeinvoke-updateitems"><strong>ISyncMgrSynchronizeInvoke：： UpdateItems</strong></a>方法中叫用同步處理管理員。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgritemflags"><strong>SYNCMGRITEMFLAGS</strong></a><br/></td>
<td>指定 <a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>SYNCMGRITEM</strong></a> 結構中目前專案的資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrloglevel"><strong>SYNCMGRLOGLEVEL</strong></a><br/></td>
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrloglevel"><strong>SYNCMGRLOGLEVEL</strong></a>列舉值會指定在<a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror"><strong>ISyncMgrSynchronizeCallback：： LogError</strong></a>方法中使用的錯誤層級。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrregisterflags"><strong>SYNCMGRREGISTERFLAGS</strong></a><br/></td>
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrregisterflags"><strong>SYNCMGRREGISTERFLAGS</strong></a>列舉值會用在<a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrregister"><strong>ISyncMgrRegister</strong></a>介面的方法中，以識別已註冊要通知處理常式的事件。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrstatus"><strong>SYNCMGRSTATUS</strong></a><br/></td>
<td>用於 <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-setitemstatus"><strong>ISyncMgrSynchronize：： SetItemStatus</strong></a> 方法，以指定專案的更新狀態。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-thumbbuttonflags"><strong>THUMBBUTTONFLAGS</strong></a><br/></td>
<td>供 <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong>THUMBBUTTON</strong></a> 用來控制按鈕的特定狀態和行為。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-thumbbuttonmask"><strong>THUMBBUTTONMASK</strong></a><br/></td>
<td>由 <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong>THUMBBUTTON</strong></a> 結構用來指定該結構的哪些成員包含有效的資料。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/thumbnailstreamcache/ne-thumbnailstreamcache-thumbnailstreamcacheoptions"><strong>ThumbnailStreamCacheOptions</strong></a><br/></td>
<td>定義 <a href="/windows/desktop/api/thumbnailstreamcache/nn-thumbnailstreamcache-ithumbnailstreamcache"><strong>IThumbnailStreamCache</strong></a> 介面使用的快取選項。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags"><strong>TRANSFER_SOURCE_FLAGS</strong></a><br/></td>
<td>由 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource"><strong>ITransferSource</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination"><strong>ITransferDestination</strong></a> 介面的方法用來控制其檔案作業。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Intshcut/ne-intshcut-translateurl_in_flags"><strong>TRANSLATEURL_IN_FLAGS</strong></a><br/></td>
<td><a href="/windows/desktop/api/Intshcut/ne-intshcut-translateurl_in_flags"><strong>TRANSLATEURL_IN_FLAGS</strong></a>列舉值會搭配<a href="/windows/desktop/api/Intshcut/nf-intshcut-translateurla"><strong>TRANSLATEURL</strong></a>函式使用，以決定它的執行方式。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-undock_reason"><strong>UNDOCK_REASON</strong></a><br/></td>
<td>值，指出停駐的協助工具應用程式視窗已解除鎖定的原因。 由 <a href="/windows/desktop/api/shobjidl/nf-shobjidl-iaccessibilitydockingservicecallback-undocked"><strong>IAccessibilityDockingServiceCallback：：未移除</strong></a>的使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-url_scheme"><strong>URL_SCHEME</strong></a><br/></td>
<td>用來指定 URL 配置。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Intshcut/ne-intshcut-urlassociationdialog_in_flags"><strong>URLASSOCIATIONDIALOG_IN_FLAGS</strong></a><br/></td>
<td><a href="/windows/desktop/api/Intshcut/ne-intshcut-urlassociationdialog_in_flags"><strong>URLASSOCIATIONDIALOG_IN_FLAGS</strong></a>列舉值會與<a href="/windows/desktop/api/Intshcut/nf-intshcut-urlassociationdialoga"><strong>URLASSOCIATIONDIALOG</strong></a>搭配使用，以判斷其執行方式。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-vpcolorflags"><strong>VPCOLORFLAGS</strong></a><br/></td>
<td>指定色彩的使用。 由 <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ivisualproperties"><strong>IVisualProperties</strong></a> 方法所使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-vpwatermarkflags"><strong>VPWATERMARKFLAGS</strong></a><br/></td>
<td>指定水位線旗標。 由 <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-ivisualproperties-setwatermark"><strong>IVisualProperties：： SetWatermark</strong></a>使用。<br/></td>
</tr>
</tbody>
</table>



 

 

 
