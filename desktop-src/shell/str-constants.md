---
description: 搭配 IBindCtx：： RegisterObjectParam 方法用來指定系結內容的一組字串索引鍵。
title: " (Shobjidl.h) 系結內容字串金鑰"
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d89a0ee1-9a4b-48a4-8965-0d92f09743a6
api_name:
- STR_AVOID_DRIVE_RESTRICTION_POLICY
- STR_BIND_DELEGATE_CREATE_OBJECT
- STR_BIND_FOLDER_ENUM_MODE
- STR_BIND_FOLDERS_READ_ONLY
- STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE
- STR_DONT_PARSE_RELATIVE
- STR_DONT_RESOLVE_LINK
- STR_FILE_SYS_FIND_DATA
- STR_FILE_SYS_BIND_DATA_WIN7_FORMAT
- STR_GET_ASYNC_HANDLER
- STR_GPS_BESTEFFORT
- STR_GPS_DELAYCREATION
- STR_GPS_FASTPROPERTIESONLY
- STR_GPS_HANDLERPROPERTIESONLY
- STR_GPS_NO_OPLOCK
- STR_GPS_OPENSLOWITEM
- STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK
- STR_IFILTER_LOAD_DEFINED_FILTER
- STR_INTERNAL_NAVIGATE
- STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE
- STR_ITEM_CACHE_CONTEXT
- STR_NO_VALIDATE_FILENAME_CHARS
- STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS
- STR_PARSE_AND_CREATE_ITEM
- STR_PARSE_DONT_REQUIRE_VALIDATED_URLS
- STR_PARSE_PARTIAL_IDLIST
- STR_PARSE_PREFER_FOLDER_BROWSING
- STR_PARSE_PREFER_WEB_BROWSING
- STR_PARSE_PROPERTYSTORE
- STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS
- STR_PARSE_SHOW_NET_DIAGNOSTICS_UI
- STR_PARSE_SKIP_NET_CACHE
- STR_PARSE_TRANSLATE_ALIASES
- STR_PARSE_WITH_PROPERTIES
- STR_PROPERTYBAG_PARAM
- STR_SKIP_BINDING_CLSID
- STR_TRACK_CLSID
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2bf8dc681718e64bf8aea059027a50148650635e
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549243"
---
# <a name="bind-context-string-keys"></a>系結內容字串索引鍵

搭配 [**IBindCtx：： RegisterObjectParam**](/windows/win32/api/objidl/nf-objidl-ibindctx-registerobjectparam) 方法用來指定系結內容的一組字串索引鍵。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">常數</th>
<th style="text-align: left;">描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="STR_AVOID_DRIVE_RESTRICTION_POLICY"></span><span id="str_avoid_drive_restriction_policy"></span><dl> <dt><strong>STR_AVOID_DRIVE_RESTRICTION_POLICY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 WINDOWS XP SP2 中引進</strong>。 指定此系結內容，以允許資料來源的用戶端覆寫隱藏的磁碟機號原則，並啟用對被封鎖之磁片磁碟機上資料來源的 view 物件存取權。<br/> 搭配 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder：： BindToObject</strong></a> 或 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem：： BindToHandler</strong></a>使用。<br/> 系統支援系統管理員控制的原則，這些原則會隱藏指定的磁碟機號，以防止使用者透過 Windows 檔案總管存取這些磁片磁碟機。 當這項原則為使用中時，結果是在受原則封鎖的磁片磁碟機上呼叫時，使用 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject"><strong>IShellFolder：： CreateViewObject</strong></a> 方法建立的 view 物件和其他處理常式將會失敗。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_BIND_DELEGATE_CREATE_OBJECT"></span><span id="str_bind_delegate_create_object"></span><dl> <dt><strong>STR_BIND_DELEGATE_CREATE_OBJECT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 Windows Vista 中引進</strong>。 指定此系結內容，讓<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder：： BindToObject</strong></a>方法使用<em>pbc</em>參數所指定的物件來建立目標物件;在此情況下， <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx：： RegisterObjectParam</strong></a>呼叫中<em>punk</em>參數所指定的物件必須執行<a href="/windows/desktop/api/Propsys/nn-propsys-icreateobject"><strong>ICreateObject</strong></a>介面。 <br/> 搭配 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder：： BindToObject</strong></a> 或 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem：： BindToHandler</strong></a>使用。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_BIND_FOLDER_ENUM_MODE"></span><span id="str_bind_folder_enum_mode"></span><dl> <dt><strong>STR_BIND_FOLDER_ENUM_MODE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 Windows 7 中引進</strong>。 傳遞至 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder：</strong></a> 具有 <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folder_enum_mode"><strong>FOLDER_ENUM_MODE</strong></a> 值的:P arsedisplayname，以控制剖析專案的列舉模式。 <strong>FOLDER_ENUM_MODE</strong>值會透過執行<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithfolderenummode"><strong>IObjectWithFolderEnumMode</strong></a>的物件在系結內容中傳遞。 <br/> 具有不同列舉模式的專案會比較標準方式 (SHCIDS_CANONICALONLY) 不同，因為它們會列舉不同的專案集合。<br/> 如果專案不支援列舉模式 (，因為它不是資料夾或未提供列舉模式) 則會以預設列舉模式建立。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_BIND_FOLDERS_READ_ONLY"></span><span id="str_bind_folders_read_only"></span><dl> <dt><strong>STR_BIND_FOLDERS_READ_ONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 Windows 7 中引進</strong>。 傳遞至 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder：:P arsedisplayname</strong></a> 以及 <strong>STR_FILE_SYS_BIND_DATA</strong>。 這會強制簡單剖析，同時也會探查 Desktop.ini 檔案，以及取得當地語系化名稱字串的路徑。 這可避免在路徑中探查資料夾，如果是代表伺服器或共用的資料夾，則可能需要大量的時間和資源。 Desktop.ini 的檔案會在某些位置快取，因此它至少會與 [資料夾] 屬性的探查一樣有效率，然後在該資料夾將 ou 數總計變成隻讀時，探查 Desktop.ini。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE"></span><span id="str_bind_force_folder_shortcut_resolve"></span><dl> <dt><strong>STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 WINDOWS XP SP2 中引進</strong>。 指定此系結內容，以強制資料夾快捷方式解析指向其目標的連結。 <br/> 資料夾快捷方式是指向同一個命名空間中另一個資料夾專案的資料夾專案，使用連結 (快速鍵) 來保存目標的 Idlist.txt。 連結會解決，以追蹤目標以防移動或重新命名。 例如，[Windows XP <strong>我的網路位置</strong> ] 資料夾和 [Windows Vista <strong>電腦</strong> ] 資料夾可以包含使用 [ <strong>新增網路位置</strong> ] wizard 建立的資料夾快捷方式。 為了改善效能， <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder：： BindToObject</strong></a> 方法預設不會解析網路資料夾的連結。<br/> 搭配 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder：： BindToObject</strong></a> 或 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem：： BindToHandler</strong></a>使用。 <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_DONT_PARSE_RELATIVE"></span><span id="str_dont_parse_relative"></span><dl> <dt><strong>STR_DONT_PARSE_RELATIVE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 WINDOWS XP 中引進</strong>。 指定此系結內容以防止呼叫<strong>desktop</strong>資料夾上的<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder：:P arsedisplayname</strong></a>方法，以將相對路徑視為相對於桌面;在這種情況下，指定此系結內容時剖析會失敗。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_DONT_RESOLVE_LINK"></span><span id="str_dont_resolve_link"></span><dl> <dt><strong>STR_DONT_RESOLVE_LINK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 Windows Vista 中引進</strong>。 指定此系結內容，以指示<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>不要解析在<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem：： BindToHandler</strong></a>中使用<strong>BHID_LinkTargetItem</strong> GUID 時所取得的連結目標。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_FILE_SYS_FIND_DATA"></span><span id="str_file_sys_find_data"></span><dl> <dt><strong>STR_FILE_SYS_FIND_DATA</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 WINDOWS XP 中引進</strong>。 指定此系結內容，以提供檔案中繼資料給 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder：:P arsedisplayname</strong></a> 方法，而不是嘗試取出實際的檔案中繼資料。 相關聯的物件必須執行 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>IFileSystemBindData</strong></a> ，而且也可以選擇性地執行 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata2"><strong>IFileSystemBindData2</strong></a>。 根據預設， <strong>IShellFolder：:P arsedisplayname</strong> 方法會驗證檔案是否存在，並使用檔案的實際中繼資料來填入識別碼清單。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_FILE_SYS_BIND_DATA_WIN7_FORMAT"></span><span id="str_file_sys_bind_data_win7_format"></span><dl> <dt><strong>STR_FILE_SYS_BIND_DATA_WIN7_FORMAT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Windows 8.1 引進</strong>。 指定此系結內容，以指出 <strong>STR_FILE_SYS_FIND_DATA</strong> 系結內容中所提供的資料，應該用來以 Windows 7 格式建立 ItemID 清單。&quot;<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GET_ASYNC_HANDLER"></span><span id="str_get_async_handler"></span><dl> <dt><strong>STR_GET_ASYNC_HANDLER</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 Windows 7 中引進</strong>。 當處理常式在與 UI 相同的執行緒上被抓取時，請指定這個系結內容。 需要避免任何需要海量儲存體的活動（例如涉及磁片或網路存取的活動）。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_BESTEFFORT"></span><span id="str_gps_besteffort"></span><dl> <dt><strong>STR_GPS_BESTEFFORT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 Windows Vista 中引進</strong>。 要求 <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> 或 <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> 處理常式時，請指定這個系結內容。 此值會搭配 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder：： BindToObject</strong></a>使用。 如需詳細資訊，請參閱 <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_BESTEFFORT</strong></a> 旗標。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_DELAYCREATION"></span><span id="str_gps_delaycreation"></span><dl> <dt><strong>STR_GPS_DELAYCREATION</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 Windows Vista 中引進</strong>。 要求 <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> 或 <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> 處理常式時，請指定這個系結內容。 此值會搭配 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder：： BindToObject</strong></a>使用。 如需詳細資訊，請參閱 <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_DELAYCREATION</strong></a> 旗標。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_FASTPROPERTIESONLY"></span><span id="str_gps_fastpropertiesonly"></span><dl> <dt><strong>STR_GPS_FASTPROPERTIESONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 Windows Vista 中引進</strong>。 要求 <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> 或 <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> 處理常式時，請指定這個系結內容。 此值會搭配 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder：： BindToObject</strong></a>使用。 如需詳細資訊，請參閱 <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_FASTPROPERTIESONLY</strong></a> 旗標。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_HANDLERPROPERTIESONLY"></span><span id="str_gps_handlerpropertiesonly"></span><dl> <dt><strong>STR_GPS_HANDLERPROPERTIESONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 Windows Vista 中引進</strong>。 要求 <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> 或 <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> 處理常式時，請指定這個系結內容。 此值會搭配 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder：： BindToObject</strong></a>使用。 如需詳細資訊，請參閱 <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_HANDLERPROPERTIESONLY</strong></a> 旗標。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_NO_OPLOCK"></span><span id="str_gps_no_oplock"></span><dl> <dt><strong>STR_GPS_NO_OPLOCK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 Windows 7 中引進</strong>。 要求 <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> 或 <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> 處理常式時，請指定這個系結內容。 此值會搭配 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder：： BindToObject</strong></a>使用。 如需詳細資訊，請參閱 <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_NO_OPLOCK</strong></a> 旗標。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_OPENSLOWITEM"></span><span id="str_gps_openslowitem"></span><dl> <dt><strong>STR_GPS_OPENSLOWITEM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 Windows Vista 中引進</strong>。 要求 <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> 或 <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> 處理常式時，請指定這個系結內容。 此值會搭配 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder：： BindToObject</strong></a>使用。 如需詳細資訊，請參閱 <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_OPENSLOWITEM</strong></a> 旗標。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK"></span><span id="str_ifilter_force_text_filter_fallback"></span><dl> <dt><strong>STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>僅限 Windows Vista。</strong> 指定此系結內容，以呼叫 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder：： BindToObject</strong></a> 方法，該方法會要求檔案系統物件的 <a href="/windows/desktop/api/filter/nn-filter-ifilter"><strong>IFilter</strong></a> 介面（如果沒有其他可用的篩選準則，則會傳回文字篩選）。 此值未定義為 Windows 7。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_IFILTER_LOAD_DEFINED_FILTER"></span><span id="str_ifilter_load_defined_filter"></span><dl> <dt><strong>STR_IFILTER_LOAD_DEFINED_FILTER</strong></dt> </dl></td>
<td style="text-align: left;"><strong>僅限 Windows Vista。</strong> 如果找不到任何已註冊的篩選準則，請指定這個系結內容，使 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder：： BindToObject</strong></a> 方法的呼叫要求檔案系統物件的 <a href="/windows/desktop/api/filter/nn-filter-ifilter"><strong>IFilter</strong></a> 介面不會傳回回溯篩選。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_INTERNAL_NAVIGATE"></span><span id="str_internal_navigate"></span><dl> <dt><strong>STR_INTERNAL_NAVIGATE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 Windows Vista 中引進</strong>。 指定此系結內容，可在呼叫 <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768216(v=vs.85)"><strong>IPersistHistory：： LoadHistory</strong></a> 方法時，啟用從資料流程進行內部流覽的記錄載入。 內部導覽是相同視圖內的導覽。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE"></span><span id="str_internetfolder_parse_only_urlmon_bindable"></span><dl> <dt><strong>STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 Windows 7 中引進</strong>。 當用戶端想要 Internet Shell 資料夾處理常式為任何有效的 URL 產生 Idlist.txt 時，如果無法建立該 URL 的 DAV 類型資料夾，請使用 STR_PARSE_PREFER_FOLDER_BROWSING 指定這個系結內容。 未驗證 URL 是否存在;只會檢查其語法，並且具有已註冊的通訊協定處理常式。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_ITEM_CACHE_CONTEXT"></span><span id="str_item_cache_context"></span><dl> <dt><strong>STR_ITEM_CACHE_CONTEXT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 Windows 7 中引進</strong>。 指定此系結內容來指示 IShellFolder 的實作為 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>：:P arsedisplayname</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex"><strong>IPersistFolder3：： InitializeEx</strong></a> ，以快取可在 shell 專案的具現化之間存在的記憶體密集型 helper 物件，而不是每次建立 shell 專案時重新建立這些物件。 相關聯的物件是另一個系結內容物件，一開始是空的。 這應該會產生個別的系結內容物件，此物件是透過 <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam"><strong>IBindCtx：： GetObjectParam</strong></a> 或 <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx：： Register. ObjectParam</strong></a>來存取。 <br/> 呼叫 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a>時，呼叫端必須提供此系結內容參數，以加入宣告這項行為。 如此一來，您就可以將系結的行為優化為連續的多個剖析名稱。 系結內容物件的存留期應該跨多個 Shell 專案和其個別系結內容的實例。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_NO_VALIDATE_FILENAME_CHARS"></span><span id="str_no_validate_filename_chars"></span><dl> <dt><strong>STR_NO_VALIDATE_FILENAME_CHARS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 Windows Vista 中引進</strong>。 指定此系結內容，以允許檔案名中出現不正確檔案名字元。 根據預設， <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder：:P arsedisplayname</strong></a> 方法的呼叫會拒絕檔案名中不合法的字元。 這個系結內容只有在搭配 STR_FILE_SYS_FIND_DATA 系結內容時才有意義。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS"></span><span id="str_parse_allow_internet_shell_folders"></span><dl> <dt><strong>STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 Windows Vista 中引進</strong>。 指定此系結內容，以在<strong>桌面</strong>資料夾上啟用<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder：:P arsedisplayname</strong></a>方法的呼叫，以剖析 url。 如果指定這個系結內容，它會覆寫 <strong><strong>STR_PARSE_PREFER_WEB_BROWSING</strong></strong>。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_AND_CREATE_ITEM"></span><span id="str_parse_and_create_item"></span><dl> <dt><strong>STR_PARSE_AND_CREATE_ITEM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 Windows 7 中引進</strong>。 指定此系結內容，以指示資料來源的 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder：:P arsedisplayname</strong></a> 的執行方式，以優化 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a>的行為。 <br/> 一般情況下， <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a> 會在要剖析的名稱上執行兩個系結作業：逐一至 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder：:P arsedisplayname</strong></a> ，另一個則用來建立 Shell 專案。 當支援 <strong>STR_PARSE_AND_CREATE_ITEM</strong> 系結內容時，會在 IShellFolder 期間建立 shell 專案來避免第二個系結 <strong>：:P arsedisplayname</strong> 系結，並透過 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iparseandcreateitem-setitem"><strong>IParseAndCreateItem：： SetItem</strong></a>儲存 shell 專案。 <strong>SHCreateItemFromParsingName</strong> 接著會使用預存 Shell 專案，而不是建立一個專案。<br/> 此參數會套用至所剖析名稱的最後一個元素。 例如，在名稱C:\Folder1\File.txt 中 &quot; ，資料會套用至 File.txt。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_DONT_REQUIRE_VALIDATED_URLS"></span><span id="str_parse_dont_require_validated_urls"></span><dl> <dt><strong>STR_PARSE_DONT_REQUIRE_VALIDATED_URLS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>僅限 Windows Vista。</strong> 指定當剖析 URL 時，此系結內容不應要求 URL 存在，才能產生它的 Idlist.txt。 當用戶端想要在無法針對指定的 URL 建立 DAV 資料夾時，當用戶端想要<strong>Internet Shell</strong>資料夾處理常式產生 URL 的 idlist.txt 時，請指定這個系結內容和<strong><strong>STR_PARSE_PREFER_FOLDER_BROWSING</strong></strong> 。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_PARTIAL_IDLIST"></span><span id="str_parse_partial_idlist"></span><dl> <dt><strong>STR_PARSE_PARTIAL_IDLIST</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 Windows Vista 中引進</strong>。 指定此系結內容，以在該專案儲存為同時執行<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>IParentAndItem</strong></a>介面的<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>物件時，傳遞正在重新剖析的原始專案。 在 Windows 7 之前，此值未定義在標頭檔中。 它可由呼叫端定義，或傳遞為其字串值的<strong>L &quot; ParseOriginalItem &quot; </strong>。 從 Windows 7，此值定義于 Shlobj.h 中。 請注意，這是與其他 STR 常數不同的標頭。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_PREFER_FOLDER_BROWSING"></span><span id="str_parse_prefer_folder_browsing"></span><dl> <dt><strong>STR_PARSE_PREFER_FOLDER_BROWSING</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 WINDOWS XP 中引進</strong>。 指定此系結內容，可讓您在<strong>桌面</strong>資料夾上呼叫<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder：:P arsedisplayname</strong></a>方法，以剖析 url，就像是資料夾一樣。 使用這個系結內容來系結至 WebDAV 伺服器。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_PREFER_WEB_BROWSING"></span><span id="str_parse_prefer_web_browsing"></span><dl> <dt><strong>STR_PARSE_PREFER_WEB_BROWSING</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 Windows Vista 中引進</strong>。 指定此系結內容以防止呼叫<strong>桌面</strong>資料夾表單剖析 Url 的<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder：:P arsedisplayname</strong></a>方法。 <strong><strong>STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS</strong></strong>可以覆寫這個系結內容。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_PROPERTYSTORE"></span><span id="str_parse_propertystore"></span><dl> <dt><strong>STR_PARSE_PROPERTYSTORE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 Windows Vista 中引進</strong>。 指定此系結內容以覆寫 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder：:P arsedisplayname</strong></a> 方法所使用的預設屬性存放區，並改為使用指定為 bind 參數的屬性存放區。 適用于委派資料夾。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS"></span><span id="str_parse_shell_protocol_to_file_objects"></span><dl> <dt><strong>STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 WINDOWS XP SP2 中引進</strong>。 指定此系結內容，可讓您在<strong>桌面</strong>資料夾上呼叫<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder：:P arsedisplayname</strong></a>方法，以使用 &quot; shell： &quot; prefix 標記法來存取檔案。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_SHOW_NET_DIAGNOSTICS_UI"></span><span id="str_parse_show_net_diagnostics_ui"></span><dl> <dt><strong>STR_PARSE_SHOW_NET_DIAGNOSTICS_UI</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 Windows Vista 中引進</strong>。 指定此系結內容，以在網路路徑剖析失敗時，讓 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder：:P arsedisplayname</strong></a> 方法的呼叫顯示 [網路診斷] 對話方塊。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_SKIP_NET_CACHE"></span><span id="str_parse_skip_net_cache"></span><dl> <dt><strong>STR_PARSE_SKIP_NET_CACHE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 Windows Vista 中引進</strong>。 指定此系結內容，以使 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder：:P arsedisplayname</strong></a> 方法的呼叫略過檢查網路共用快取，並直接與網路伺服器聯繫。 快取網路共用的相關資訊以改善效能， <strong>IShellFolder：:P arsedisplayname</strong> 預設會檢查此快取。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_TRANSLATE_ALIASES"></span><span id="str_parse_translate_aliases"></span><dl> <dt><strong>STR_PARSE_TRANSLATE_ALIASES</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 WINDOWS XP 中引進</strong>。 指定此系結內容，將剖析的屬性傳遞至委派命名空間的 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder：:P arsedisplayname</strong></a> 方法。 命名空間可以使用傳遞的屬性，而不是嘗試剖析名稱本身。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_WITH_PROPERTIES"></span><span id="str_parse_with_properties"></span><dl> <dt><strong>STR_PARSE_WITH_PROPERTIES</strong></dt> </dl></td>
<td style="text-align: left;"><strong>僅限 Windows Vista。</strong> 剖析系結內容，在呼叫 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder：:P arsedisplayname</strong></a>時，用來傳遞一組屬性和專案的名稱。 系結內容中的物件會執行 <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> ，並藉由呼叫 <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam"><strong>IBindCtx：： GetObjectParam</strong></a>來取出。<br/> DBFolder 是 Shell 資料來源，代表搜尋結果和查詢型視圖中的專案。 DBFolder 會藉由查詢 Windows Search 系統來抓取這些專案。 搜尋結果中的專案是透過通訊協定配置來識別，例如 &quot; file： &quot; 或 &quot; mapi： &quot; 。 DBFolder 會委派給針對這些通訊協定所建立的 Shell 資料來源，以提供這些專案的行為。 如需詳細資訊，請參閱 <a href="/previous-versions/bb233544(v=msdn.10)">開發通訊協定處理常式增益集</a> 。<br/> 當 DBFolder 將其剖析作業委派給支援 Windows Search 通訊協定的 Shell 資料來源時，這個系結內容會提供對該專案之查詢結果中所傳回值的存取權。 其中包括下列項目：<br/>
<ul>
<li><a href="/windows/desktop/properties/props-system-itemtype">系統</a> (PKEY_ItemType) </li>
<li><a href="/windows/desktop/properties/props-system-parsingpath">ParsingPath</a> (PKEY_ParsingPath) </li>
<li><a href="/windows/desktop/properties/props-system-itempathdisplay">ItemPathDisplay</a> (PKEY_ItemPathDisplay) </li>
<li><a href="/windows/desktop/properties/props-system-itemnamedisplay">ItemNameDisplay</a> (PKEY_ItemNameDisplay) </li>
</ul>
<br/> 如果用戶端有一組定義專案的屬性，也可以使用這個系結內容來剖析 DBFolder 專案。 在此情況下，應該將空的名稱傳遞至 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder：:P arsedisplayname</strong></a>。<br/> 在 Windows 7 之前，此值未定義在標頭檔中。 它可由呼叫端定義或傳遞為其字串值： <code>L&quot;ParseWithProperties&quot;</code> 。 從 Windows 7，此值定義于 Shlobj.h 中。 請注意，這是不同的標頭，也就是定義其他 STR 常數的位置。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PROPERTYBAG_PARAM"></span><span id="str_propertybag_param"></span><dl> <dt><strong>STR_PROPERTYBAG_PARAM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Windows 8 引進</strong>。 指定此系結內容，表示系結內容參數是屬性包 (<a href="/windows/win32/api/oaidl/nn-oaidl-ipropertybag"><strong>IPropertyBag</strong></a>) 用來在系結內容中傳遞變異值。 如需詳細資料，請參閱「備註」一節。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_SKIP_BINDING_CLSID"></span><span id="str_skip_binding_clsid"></span><dl> <dt><strong>STR_SKIP_BINDING_CLSID</strong></dt> </dl></td>
<td style="text-align: left;"><strong>在 WINDOWS XP 中引進</strong>。 指定此系結內容，以在剖析或系結時，讓呼叫 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder：:P arsedisplayname</strong></a> 或 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder：： BindToObject</strong></a> 方法略過特定的 Shell 命名空間延伸模組。 要忽略的命名空間 CLSID 是由 bind 參數的 <a href="/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid"><strong>IPersist：： GetClassID</strong></a> 方法所提供。 <br/>
<blockquote>
[!Note]<br />
在 Windows 2000 SP3 中引進，此值是在 Shlobj.h 中定義，直到 Windows XP 移至 Shobjidl.h。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_TRACK_CLSID"></span><span id="str_track_clsid"></span><dl> <dt><strong>STR_TRACK_CLSID</strong></dt> </dl></td>
<td style="text-align: left;">未使用。<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>備註

系結內容可用來將選擇性參數傳遞至具有 IBindCtx 參數的函式 \* 。 這些參數會以 COM 物件的形式表示，而且可能會執行用來建立參數資料模型的介面。 某些系結內容代表布林值，其中 **TRUE** 表示只會執行 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 的物件，而 FALSE 表示沒有任何物件存在。

[**IShellFolder：:P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname)、 [**IShellFolder：： BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) 和 [**IShellItem：： BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) 會取得系結內容，而且您可以透過該系結內容傳遞這些參數。

某些系結內容是特定資料來源執行或處理常式類型專屬的。

系結內容參數是定義來與特定的函式或方法搭配使用。

透過 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)要求屬性存放區時，您可以傳遞 null [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx)參數來指定對等的 [**GPS \_ 預設值**](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags)。 您也可以在系結 \_ 內容中傳遞 STGM READWRITE STGM 的模式，藉以指定 GPS READWRITE 的對等專案 \_ \| \_ 。

**STR \_ PROPERTYBAG \_ PARAM** 系結內容物件所指定的屬性包包含其他值，您可以使用 [**IPropertyBag：： Read**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768197(v=vs.85))和 [**IPropertyBag：： Write**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768198(v=vs.85))方法來存取這些值。



| 屬性名稱                                 | 類型     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| STR \_ 列舉 \_ 專案 \_ 旗標                       | VT \_ UI4  | **Windows 8 引進**。 當您呼叫 [**IShellItem：： BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler)與 **BHID \_ EnumItems** 時，指定要傳遞至 [**IShellFolder：： EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects)的 [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf)值。                                                                                                                                                                                                                         |
| STR \_ 剖析 \_ 明確 \_ 關聯 \_ 成功 | VT \_ BOOL | **在 Windows 7 中引進**。 [**IShellFolder：:P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname)方法會設定這個屬性，告知呼叫端所傳回的 idlist.txt 已系結至使用 str parse 指定的 [progid](fa-progids.md) （具有 **明確的 \_ \_ \_ \_ ProgID** ），或使用以 str parse 指定的應用程式搭配 **\_ \_ \_ 明確的 \_ ASSOCAPP**。 當 **STR \_ 剖析 \_ 明確 \_ 關聯 \_ 成功** 時，ProgID 或應用程式未系結至 idlist.txt。 |
| \_ \_ 使用 \_ 明確 ASSOCAPP 進行 \_ STR 剖析          | VT \_ BSTR | **在 Windows 7 中引進**。 指定這個屬性可讓 [**IShellFolder：:P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) 方法的呼叫傳回系結至應用程式之檔案類型關聯處理常式的 idlist.txt。                                                                                                                                                                                                                                          |
| \_ \_ 具有 \_ 明確 PROGID 的 \_ STR 剖析            | VT \_ BSTR | **在 Windows 7 中引進**。 指定這個屬性可讓 [**IShellFolder：:P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) 方法的呼叫傳回系結至所提供 [ProgID](fa-progids.md)之檔案關聯處理常式的 idlist.txt。                                                                                                                                                                                                                          |



 

如需使用系結內容值的範例，請參閱使用 [參數剖析範例](samples-parsingwithparameters.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Shobjidl.h。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shobjidl.h .idl</dt> </dl> |



 

 
