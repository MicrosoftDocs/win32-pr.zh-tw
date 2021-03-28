---
description: 本節說明 Windows Shell 結構。
title: Shell 結構
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 814ae153-39b3-49ee-9da1-efe7e649c73e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5bbda4cd81c3db2dff664b9d16d2db60aa8f12f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973773"
---
# <a name="shell-structures"></a>Shell 結構

本節說明 Windows Shell 結構。

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
<td><a href="/windows/win32/api/shlobj/ns-shlobj-aashellmenufilename"><strong>AASHELLMENUFILENAME</strong></a><br/></td>
<td>變數大小的結構，包含功能表檔名稱的相關資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj/ns-shlobj-aashellmenuitem"><strong>AASHELLMENUITEM</strong></a><br/></td>
<td>包含功能表項目的相關資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-appbardata"><strong>APPBARDATA</strong></a><br/></td>
<td>包含系統 appbar 訊息的相關資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfo"><strong>APPCATEGORYINFO</strong></a><br/></td>
<td>提供在主控台中新增/移除程式的應用程式類別目錄資訊。 <a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfolist"><strong>APPCATEGORYINFOLIST</strong></a>結構是用來建立應用程式發行者的完整類別清單。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfolist"><strong>APPCATEGORYINFOLIST</strong></a><br/></td>
<td>提供應用程式發行者提供的支援應用程式類別清單，以在主控台中新增/移除程式。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shappmgr/ns-shappmgr-appinfodata"><strong>APPINFODATA</strong></a><br/></td>
<td>提供已發佈應用程式至 [新增/移除程式] 主控台公用程式的相關資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-associationelement"><strong>ASSOCIATIONELEMENT</strong></a><br/></td>
<td>定義 <a href="/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses"><strong>AssocCreateForClasses</strong></a> 用來取得指定檔案關聯之 <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a> 介面的資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-bandinfosfb"><strong>BANDINFOSFB</strong></a><br/></td>
<td>包含有關資料夾帶的資訊。 此結構會與 <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-getbandinfosfb"><strong>IShellFolderBand：： GetBandInfoSFB</strong></a> 和 <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-setbandinfosfb"><strong>IShellFolderBand：： SetBandInfoSFB</strong></a> 方法搭配使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-bandsiteinfo"><strong>BANDSITEINFO</strong></a><br/></td>
<td>包含有關寬線網站的資訊。 此結構會與 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-getbandsiteinfo"><strong>IBandSite：： GetBandSiteInfo</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-setbandsiteinfo"><strong>IBandSite：： SetBandSiteInfo</strong></a> 方法搭配使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>BASEBROWSERDATA</strong></a><br/></td>
<td>包含基類的受保護成員。 <a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>BASEBROWSERDATA</strong></a> 會定義瀏覽器狀態，並搭配 <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-getbasebrowserdata"><strong>IBrowserService2：： GetBaseBrowserData</strong></a> 和 <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-putbasebrowserdata"><strong>IBrowserService2：:P utbasebrowserdata</strong></a>使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)"><strong>BORDERWIDTHS</strong></a><br/></td>
<td>定義框線矩形左上角和右下角的座標。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa"><strong>BROWSEINFO</strong></a><br/></td>
<td>包含 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera"><strong>SHBrowseForFolder</strong></a> 函式的參數，並接收使用者所選取之資料夾的相關資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-category_info"><strong>CATEGORY_INFO</strong></a><br/></td>
<td>包含類別目錄資訊。 元件類別是邏輯相關元件物件模型的群組， (COM) 類別，可 (CATID) 共用通用分類識別碼。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-cida"><strong>CIDA</strong></a><br/></td>
<td>搭配 <a href="clipboard.md">CFSTR_SHELLIDLIST</a> 剪貼簿格式使用，可將指標傳送至一個或多個 Shell 命名空間物件 (PIDL) 的專案識別碼清單。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a><br/></td>
<td>定義資料行資訊。 供 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>IColumnManager</strong></a> 介面的成員使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a><br/></td>
<td>包含 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>ICoNtextMenu：： InvokeCommand</strong></a> 用來叫用快捷方式功能表命令所需的資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex"><strong>CMINVOKECOMMANDINFOEX</strong></a><br/></td>
<td>包含快捷方式功能表命令的延伸資訊。 此結構是 <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a> 的延伸版本，可允許使用 Unicode 值。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec"><strong>COMDLG_FILTERSPEC</strong></a><br/></td>
<td>一般用來篩選元素。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-component"><strong>元件</strong></a><br/></td>
<td>由 Windows 2000 用來保存元件的相關資訊。 此結構會取代 <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-ie4component"><strong>IE4COMPONENT</strong></a> 結構。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-componentsopt"><strong>COMPONENTSOPT</strong></a><br/></td>
<td>包含桌面專案選項。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-comppos"><strong>COMPPOS</strong></a><br/></td>
<td>保存元件的位置和大小的相關資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-compstateinfo"><strong>COMPSTATEINFO</strong></a><br/></td>
<td>由 Windows 2000 用來保存元件狀態的相關資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_item"><strong>CONFIRM_CONFLICT_ITEM</strong></a><br/></td>
<td>定義衝突專案結構。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_result_info"><strong>CONFIRM_CONFLICT_RESULT_INFO</strong></a><br/></td>
<td>定義衝突結果資訊結構。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cpl/ns-cpl-cplinfo"><strong>CPLINFO</strong></a><br/></td>
<td>包含主控台應用程式所支援之對話方塊的資源資訊和應用程式定義的值。 主控台應用程式的 <a href="/windows/desktop/api/cpl/nc-cpl-applet_proc"><strong>CPlApplet</strong></a> 函式會將這項資訊傳回主控台，以回應 <a href="cpl-inquire.md"><strong>CPL_INQUIRE</strong></a> 訊息。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_credential_serialization"><strong>CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</strong></a><br/></td>
<td>包含認證的詳細資料。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_field_descriptor"><strong>CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</strong></a><br/></td>
<td>描述認證中的單一欄位。 例如，字串或使用者映射。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-csfv"><strong>CSFV</strong></a><br/></td>
<td>搭配 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex"><strong>SHCreateShellFolderViewEx</strong></a> 函式使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-datablock_header"><strong>DATABLOCK_HEADER</strong></a><br/></td>
<td>作為 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>所使用之部分額外資料結構的標頭。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu"><strong>DEFCONTEXTMENU</strong></a><br/></td>
<td>包含 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>SHCreateDefaultCoNtextMenu</strong></a>所使用的內容功能表資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-delegateitemid"><strong>DELEGATEITEMID</strong></a><br/></td>
<td>由委派資料夾用來取代標準 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo"><strong>DETAILSINFO</strong></a><br/></td>
<td>包含 Shell 資料夾專案的詳細資訊。 搭配 <a href="sfvm-getdetailsof.md"><strong>SFVM_GETDETAILSOF</strong></a> 通知使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics"><strong>DFMICS</strong></a><br/></td>
<td>包含 <a href="dfm-invokecommandex.md"><strong>DFM_INVOKECOMMANDEX</strong></a>所使用的其他引數。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo"><strong>DLLVERSIONINFO</strong></a><br/></td>
<td>接收 DLL 特定版本資訊。 它會與 <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><strong>DllGetVersion</strong></a> 函數搭配使用。 <br/>
<blockquote>
[!Note]<br />
您可以使用 <a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2"><strong>DLLVERSIONINFO2</strong></a> 結構來取代此結構。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2"><strong>DLLVERSIONINFO2</strong></a><br/></td>
<td>接收 DLL 特定版本資訊。 它會與 <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><strong>DllGetVersion</strong></a> 函數搭配使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription"><strong>DROPDESCRIPTION</strong></a><br/></td>
<td>描述放置物件的影像和伴隨的文字。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles"><strong>DROPFILES</strong></a><br/></td>
<td>定義 <a href="clipboard.md">CF_HDROP</a> 剪貼簿格式。 接下來的資料是以雙精度 null 結束的檔案名清單。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_darwin_link"><strong>EXP_DARWIN_LINK</strong></a><br/></td>
<td>保存 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>所使用的額外資料區塊。 它會保存連結的 Windows Installer 識別碼。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_propertystorage"><strong>EXP_PROPERTYSTORAGE</strong></a><br/></td>
<td>儲存 Shell 連結狀態的相關資訊。 此結構會用於標記為 EXP_PROPERTYSTORAGE_SIG 的額外資料區段。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_special_folder"><strong>EXP_SPECIAL_FOLDER</strong></a><br/></td>
<td>保存 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>所使用的額外資料區塊。 它包含特殊的資料夾資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_sz_link"><strong>EXP_SZ_LINK</strong></a><br/></td>
<td>保存 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>所使用的額外資料區塊。 它會保留圖示或目標的可展開環境字串。<br/></td>
</tr>
<tr class="even">
<td><a href="ext-button.md"><strong>EXT_BUTTON</strong></a><br/></td>
<td>包含有關檔案管理員延伸模組 DLL 新增至 [檔案管理員] 工具列之按鈕的資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-extrasearch"><strong>EXTRASEARCH</strong></a><br/></td>
<td>由 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumextrasearch"><strong>IEnumExtraSearch</strong></a> 列舉值物件用來傳回 Shell 資料夾物件所支援之搜尋物件的資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-file_attributes_array"><strong>FILE_ATTRIBUTES_ARRAY</strong></a><br/></td>
<td>包含 CFSTR_FILE_ATTRIBUTES_ARRAY 的剪貼簿格式定義。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filedescriptora"><strong>FILEDESCRIPTOR</strong></a><br/></td>
<td>描述在 Microsoft ActiveX <a href="dragdrop.md">拖放</a> 作業期間，透過剪貼簿所複製之檔案的屬性。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filegroupdescriptora"><strong>FILEGROUPDESCRIPTOR</strong></a><br/></td>
<td>定義 CF_FILEGROUPDESCRIPTOR 剪貼簿格式。<br/></td>
</tr>
<tr class="odd">
<td><a href="fms-getdriveinfo.md"><strong>FMS_GETDRIVEINFO</strong></a><br/></td>
<td>包含 [active File Manager] 視窗中所選磁片磁碟機的相關資訊 ([目錄] 視窗或 [搜尋結果] 視窗) 。<br/></td>
</tr>
<tr class="even">
<td><a href="fms-getfilesel.md"><strong>FMS_GETFILESEL</strong></a><br/></td>
<td>在 [active 檔案管理員] 視窗中， ([目錄] 視窗或 [搜尋結果] 視窗) ，包含所選取檔案的相關資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="fms-helpstring.md"><strong>FMS_HELPSTRING</strong></a><br/></td>
<td>包含檔管理員用來加入功能表或工具列命令專案之說明字串的資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="fms-load.md"><strong>FMS_LOAD</strong></a><br/></td>
<td>包含檔管理員用來新增由檔管理程式延伸模組 DLL 提供之自訂功能表的資訊。 此結構也提供差異值，可供延伸模組 DLL 在檔案管理員載入功能表之後，用來操作自訂功能表。<br/></td>
</tr>
<tr class="odd">
<td><a href="fms-toolbarload.md"><strong>FMS_TOOLBARLOAD</strong></a><br/></td>
<td>包含要新增至 [檔案管理員] 工具列之自訂按鈕的相關資訊。 這些按鈕是由檔案管理員延伸模組 DLL 提供。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings"><strong>FOLDERSETTINGS</strong></a><br/></td>
<td>包含資料夾檢視資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-fvshowinfo"><strong>FVSHOWINFO</strong></a><br/></td>
<td>包含檔案檢視器用來顯示檔案的資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/winuser/ns-winuser-helpinfo"><strong>HELPINFO</strong></a><br/></td>
<td>包含已要求即時線上說明之專案的相關資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/ns-winuser-helpwininfow"><strong>HELPWININFO</strong></a><br/></td>
<td>包含主要或次要說明視窗的大小和位置。 應用程式可以使用 HELP_SETWINPOS 值呼叫 <a href="/windows/desktop/api/Winuser/nf-winuser-winhelpa"><strong>WinHelp</strong></a> 函數來設定這項資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-ie4component"><strong>IE4COMPONENT</strong></a><br/></td>
<td>由 Microsoft Internet Explorer 4.0 與 Microsoft Internet Explorer 4.01 用來保存元件的相關資訊。 在 Windows 2000 中，它會被 <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-component"><strong>元件</strong></a> 結構取代。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a><br/></td>
<td>包含專案識別碼的清單。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-itemspacing"><strong>ITEMSPACING</strong></a><br/></td>
<td>儲存兩個可能大小的圖示間距尺寸，可供顯示：小型和大型。 由 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getitemspacing"><strong>IShellFolderView：： GetItemSpacing</strong></a>使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition"><strong>KNOWNFOLDER_DEFINITION</strong></a><br/></td>
<td>定義已知資料夾的詳細資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shtypes/ns-shtypes-logfontw"><strong>LOGFONT</strong></a><br/></td>
<td>定義字型的屬性。<br/></td>
</tr>
<tr class="odd">
<td><a href="mruinfo.md"><strong>MRUINFO</strong></a><br/></td>
<td>包含定義最近使用的新 (MRU) 清單的資訊。 由 <a href="createmrulist.md"><strong>CreateMRUListW</strong></a>使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/winuser/ns-winuser-multikeyhelpw"><strong>MULTIKEYHELP</strong></a><br/></td>
<td>指定要搜尋的關鍵字，以及要在 Windows 說明中搜尋的關鍵字資料表。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shellapi/ns-shellapi-nc_address"><strong>NC_ADDRESS</strong></a><br/></td>
<td>包含描述網路位址的資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/hkey-type"><strong>NET_ADDRESS_INFO</strong></a><br/></td>
<td>描述網路位址。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cpl/ns-cpl-newcplinfow"><strong>NEWCPLINFO</strong></a><br/></td>
<td>包含主控台應用程式所支援之對話方塊的資源資訊和應用程式定義的值。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa"><strong>NOTIFYICONDATA</strong></a><br/></td>
<td>包含系統在通知區域中顯示通知所需的資訊。 由 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona"><strong>Shell_NotifyIcon</strong></a>使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-notifyiconidentifier"><strong>NOTIFYICONIDENTIFIER</strong></a><br/></td>
<td>包含 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect"><strong>Shell_NotifyIconGetRect</strong></a> 用來識別要取得周框矩形之圖示的資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nresarray"><strong>NRESARRAY</strong></a><br/></td>
<td>定義 CF_NETRESOURCE 剪貼簿格式。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ns-shobjidl-nstccustomdraw"><strong>NSTCCUSTOMDRAW</strong></a><br/></td>
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw"><strong>INameSpaceTreeControlCustomDraw</strong></a>方法所使用的自訂繪圖結構。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_console_props"><strong>NT_CONSOLE_PROPS</strong></a><br/></td>
<td>保存 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>所使用的額外資料區塊。 它會保存主控台屬性。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_fe_console_props"><strong>NT_FE_CONSOLE_PROPS</strong></a><br/></td>
<td>保存 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>所使用的額外資料區塊。 它會保存主控台的字碼頁。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-open_printer_props_infoa"><strong>OPEN_PRINTER_PROPS_INFO</strong></a><br/></td>
<td>識別印表機屬性頁中的特定屬性工作表，以及該屬性工作表是否應為強制回應。 選擇性地搭配 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda"><strong>SHInvokePrinterCommand</strong></a> 函式使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-openasinfo"><strong>OPENASINFO</strong></a><br/></td>
<td>儲存 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenwithdialog"><strong>SHOpenWithDialog</strong></a> 函數的資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/ns-shobjidl-overlapped"><strong>重疊</strong></a><br/></td>
<td>包含用於非同步 (重迭) 輸入/輸出 (i/o) 的資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlwapi/ns-shlwapi-parsedurlw"><strong>PARSEDURL</strong></a><br/></td>
<td>由 <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-parseurla"><strong>ParseURL</strong></a> 函數用來傳回剖析的 URL。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-persist_folder_target_info"><strong>PERSIST_FOLDER_TARGET_INFO</strong></a><br/></td>
<td>指定資料夾快捷方式的目的檔案夾及其屬性。 此結構是由 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-getfoldertargetinfo"><strong>IPersistFolder3：： GetFolderTargetInfo</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex"><strong>IPersistFolder3：： InitializeEx</strong></a>使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-previewhandlerframeinfo"><strong>PREVIEWHANDLERFRAMEINFO</strong></a><br/></td>
<td>快速鍵表格結構。 由 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext"><strong>IPreviewHandlerFrame：： GetWindowCoNtext</strong></a>使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa"><strong>PROFILEINFO.TXT</strong></a><br/></td>
<td>包含載入或卸載使用者設定檔時所使用的資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shappmgr/ns-shappmgr-pubappinfo"><strong>PUBAPPINFO</strong></a><br/></td>
<td>提供有關應用程式發行者的已發行應用程式的資訊，以便在主控台中 <strong>新增/移除程式</strong> 。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo"><strong>QCMINFO</strong></a><br/></td>
<td>包含將功能表項目合併到 Windows 檔案總管功能表的資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-qitab"><strong>QITAB</strong></a><br/></td>
<td>由 <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-qisearch"><strong>QISearch</strong></a> 函數用來描述單一介面。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/propidl/ns-propidl-serializedpropertyvalue"><strong>SERIALIZEDPROPERTYVALUE</strong></a><br/></td>
<td>代表序列化 <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> 結構之任意類型的記憶體範圍。 程式不應該檢查 <a href="/windows/win32/api/propidl/ns-propidl-serializedpropertyvalue"><strong>SERIALIZEDPROPERTYVALUE</strong></a>的內容;相反地，它們應該使用 <a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgserializepropvariant"><strong>StgSerializePropVariant</strong></a> 和 <a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgdeserializepropvariant"><strong>StgDeserializePropVariant</strong></a> 函式來處理它。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfv_create"><strong>SFV_CREATE</strong></a><br/></td>
<td>此結構會與 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a> 函數搭配使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos"><strong>SFV_SETITEMPOS</strong></a><br/></td>
<td>儲存專案的位置資訊。 搭配 message <a href="sfvm-setitempos.md"><strong>SFVM_SETITEMPOS</strong></a>使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data"><strong>SFVM_HELPTOPIC_DATA</strong></a><br/></td>
<td>包含 HTML 說明檔的名稱和該檔案中的主題。 搭配 <a href="sfvm-gethelptopic.md"><strong>SFVM_GETHELPTOPIC</strong></a> 通知使用。 此結構需要 Unicode 字串。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data"><strong>SFVM_PROPPAGE_DATA</strong></a><br/></td>
<td>包含要加入至物件 <strong>屬性</strong> 表之頁面的詳細資料。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfo"><strong>SHARDAPPIDINFO</strong></a><br/></td>
<td>包含 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> 用來識別專案的資料（在此案例中為 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>），以及與其相關聯的處理常式。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfoidlist"><strong>SHARDAPPIDINFOIDLIST</strong></a><br/></td>
<td>包含 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> 用來識別專案的資料（在此案例中為絕對 PIDL），以及與它相關聯的處理常式。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfolink"><strong>SHARDAPPIDINFOLINK</strong></a><br/></td>
<td>包含 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> 用來識別兩個專案的資料，在此案例中是透過 <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a>，以及與其相關聯的處理常式。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shchangenotifyentry"><strong>SHChangeNotifyEntry</strong></a><br/></td>
<td>包含和接收變更通知的資訊。 此結構會搭配 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister"><strong>SHChangeNotifyRegister</strong></a> 函式和 <a href="sfvm-queryfsnotify.md"><strong>SFVM_QUERYFSNOTIFY</strong></a> 通知一起使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumndata"><strong>SHCOLUMNDATA</strong></a><br/></td>
<td>包含可識別特定檔案的資訊。 <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata"><strong>IColumnProvider：： GetItemData</strong></a>會在要求特定檔案的資料時使用它。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/objects"><strong>SHCOLUMNID</strong></a><br/></td>
<td>指定 Windows 檔案總管詳細資料檢視將顯示之資料行的 FMTID/PID 識別碼。 <br/>
<blockquote>
[!Note]<br />
在 Windows Vista 中， <a href="/windows/desktop/shell/objects"><strong>SHCOLUMNID</strong></a> 被視為舊版的表單，不應該使用。 在其位置中，使用 <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> 結構。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumninfo"><strong>SHCOLUMNINFO</strong></a><br/></td>
<td>包含資料行屬性的相關資訊。 它是由 <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo"><strong>IColumnProvider：： GetColumnInfo</strong></a>所使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumninit"><strong>SHCOLUMNINIT</strong></a><br/></td>
<td>將初始化資訊傳遞給 <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize"><strong>IColumnProvider：： Initialize</strong></a>。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shdescriptionid"><strong>SHDESCRIPTIONID</strong></a><br/></td>
<td>接收專案資料以回應 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdatafromidlista"><strong>SHGetDataFromIDList</strong></a>的呼叫。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shdragimage"><strong>SHDRAGIMAGE</strong></a><br/></td>
<td>包含建立拖曳影像所需的資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shell_item_resource"><strong>SHELL_ITEM_RESOURCE</strong></a><br/></td>
<td>定義 Shell 專案資源。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-shelldetails"><strong>SHELLDETAILS</strong></a><br/></td>
<td>報告 Shell 資料夾中專案的詳細資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa"><strong>SHELLEXECUTEINFO</strong></a><br/></td>
<td>包含 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>所使用的資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellflagstate"><strong>SHELLFLAGSTATE</strong></a><br/></td>
<td>包含一組表示目前 Shell 設定的旗標。 此結構會與 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsettings"><strong>SHGetSettings</strong></a> 函數搭配使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellstatea"><strong>SHELLSTATE</strong></a><br/></td>
<td>包含 Shell 狀態的設定。 此結構會與 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings"><strong>SHGetSetSettings</strong></a> 函數搭配使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shfileinfoa"><strong>SHFILEINFO</strong></a><br/></td>
<td>包含檔案物件的相關資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa"><strong>SHFILEOPSTRUCT</strong></a><br/></td>
<td>包含 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> 函數用來執行檔案作業的資訊。 <br/>
<blockquote>
[!Note]<br />
從 Windows Vista 起，建議使用 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a> 介面，而不是這個函式。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shfoldercustomsettings"><strong>SHFOLDERCUSTOMSETTINGS</strong></a><br/></td>
<td>保存自訂資料夾設定。 此結構會與 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetfoldercustomsettings"><strong>SHGetSetFolderCustomSettings</strong></a> 函數搭配使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a><br/></td>
<td>定義專案識別碼。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shnamemappinga"><strong>SHNAMEMAPPING</strong></a><br/></td>
<td>包含 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> 函式所移動、複製或重新命名之每個檔案的舊路徑名稱和新路徑名稱。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shqueryrbinfo"><strong>SHQUERYRBINFO</strong></a><br/></td>
<td>包含 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryrecyclebina"><strong>SHQueryRecycleBin</strong></a> 函數取出的大小和專案計數資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shstockiconinfo"><strong>SHSTOCKICONINFO</strong></a><br/></td>
<td>接收用來取出股票殼圖示的資訊。 此結構用於呼叫 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>SHGetStockIconInfo</strong></a>中。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shappmgr/ns-shappmgr-slowappinfo"><strong>SLOWAPPINFO</strong></a><br/></td>
<td>提供在主控台中 <strong>新增/移除程式</strong> 的特殊應用程式資訊。 此結構不適用於已發佈的應用程式。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct"><strong>SMCSHCHANGENOTIFYSTRUCT</strong></a><br/></td>
<td>包含變更通知的相關資訊。 它是由 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm"><strong>IShellMenuCallback：： CallbackSM</strong></a>所使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata"><strong>SMDATA</strong></a><br/></td>
<td>包含來自功能表區的資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo"><strong>SMINFO</strong></a><br/></td>
<td>包含來自功能表區之專案的相關資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/urlmon/ns-urlmon-softdistinfo"><strong>SOFTDISTINFO</strong></a><br/></td>
<td>包含軟體更新的相關資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-sortcolumn"><strong>SORTCOLUMN</strong></a><br/></td>
<td>儲存有關如何排序資料夾檢視中所顯示之資料行的資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a><br/></td>
<td>包含從 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> 介面方法傳回的字串。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-sv2cvw2_params"><strong>SV2CVW2_PARAMS</strong></a><br/></td>
<td>保留 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-createviewwindow2"><strong>IShellView2：： CreateViewWindow2</strong></a> 方法的參數。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/shell/objects-cpp"><strong>SYNC_HANDLER_ITEM_INFO</strong></a><br/></td>
<td>定義排程同步處理的處理常式。 搭配 <a href="/previous-versions/windows/desktop/isync-schedule/bb774680(v=vs.85)"><strong>ISyncSchedule：： AddItem</strong></a>使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-syncmgr_conflict_id_info"><strong>SYNCMGR_CONFLICT_ID_INFO</strong></a><br/></td>
<td>描述衝突識別碼資訊結構。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrhandlerinfo"><strong>SYNCMGRHANDLERINFO</strong></a><br/></td>
<td>提供在 <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-gethandlerinfo"><strong>ISyncMgrSynchronize：： GetHandlerInfo</strong></a> 方法中使用之處理常式的相關資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>SYNCMGRITEM</strong></a><br/></td>
<td>提供 <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>ISyncMgrEnumItems</strong></a> 介面所列舉之專案的相關資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrlogerrorinfo"><strong>SYNCMGRLOGERRORINFO</strong></a><br/></td>
<td>提供在 <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror"><strong>ISyncMgrSynchronizeCallback：： LogError</strong></a> 方法中使用的錯誤資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrprogressitem"><strong>SYNCMGRPROGRESSITEM</strong></a><br/></td>
<td>在進行同步處理時提供狀態資訊。 此結構會與 <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-progress"><strong>ISyncMgrSynchronizeCallback：:P rogress</strong></a> 方法搭配使用，並對應至單一同步處理專案。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-tbinfo"><strong>TBINFO</strong></a><br/></td>
<td>搭配 <a href="sfvm-getbuttoninfo.md"><strong>SFVM_GETBUTTONINFO</strong></a> 通知使用，可指定要新增至工具列的按鈕數目，以及新增的按鈕數目。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong>THUMBBUTTON</strong></a><br/></td>
<td>由 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>ITaskbarList3</strong></a> 介面的方法用來定義以視窗的縮圖標記法內嵌的工具列中使用的按鈕。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-wallpaperopt"><strong>WALLPAPEROPT</strong></a><br/></td>
<td>包含壁紙顯示選項。 搭配 <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop"><strong>IActiveDesktop</strong></a> 介面的成員使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tlogstg/ns-tlogstg-windowdata"><strong>WINDOWDATA</strong></a><br/></td>
<td>儲存視窗資料。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Thumbcache/ne-thumbcache-wts_contextflags"><strong>WTS_CONTEXTFLAGS</strong></a><br/></td>
<td>指定縮圖解壓縮的內容。 由 <a href="/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailsettings-setcontext"><strong>IThumbnailSettings：： SetCoNtext</strong></a>使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Thumbcache/ne-thumbcache-wts_flags"><strong>WTS_FLAGS</strong></a><br/></td>
<td><a href="/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailcache-getthumbnail"><strong>IThumbnailCache：： GetThumbnail</strong></a>所使用的值，可指定用於解壓縮和顯示縮圖影像的選項。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Thumbcache/ns-thumbcache-wts_thumbnailid"><strong>WTS_THUMBNAILID</strong></a><br/></td>
<td>包含系統縮圖快取中縮圖的唯一識別碼。<br/></td>
</tr>
</tbody>
</table>



 

 

 
