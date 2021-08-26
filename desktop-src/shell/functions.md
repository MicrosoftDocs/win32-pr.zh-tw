---
description: 本節說明 Windows Shell 函數。
title: Shell 函數
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f4d6c0c4-8db3-4721-80f5-2a73bb57cd99
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fce7bc2b7a6669afd42f7d4b8883aff937615ae0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476594"
---
# <a name="shell-functions"></a>Shell 函數

\[此函式已不再實作為。\]

本節說明 Windows Shell 函數。

## <a name="in-this-section"></a>本節內容




| 主題 | 描述 | 
|-------|-------------|
| <a href="intsafe-h-functions-bumper.md">Intsafe .h 函數</a><br /> | 
| <a href="library-functions-bumper.md">程式庫函式</a><br /> | 
| <a href="path-functions.md">路徑函式</a><br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses"><strong>AssocCreateForClasses</strong></a><br /> | 抓取可實 <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a> 介面的物件。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-assocgetdetailsofpropkey"><strong>AssocGetDetailsOfPropKey</strong></a><br /> | 使用 <a href="nse-works.md">命名空間延伸</a>模組所提供的檔案關聯資訊，抓取指定屬性索引鍵的值。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2"><strong>CDefFolderMenu_Create2</strong></a><br /> | 建立所選檔案資料夾物件群組的內容功能表。<br /> | 
| <a href="/windows/win32/api/ntquery/nf-ntquery-cishutdown"><strong>CIShutdown</strong></a><br /> | 關閉內容索引器，並關閉所有開啟的目錄。 <br /><blockquote>[!Note]<br />Windows 8 不支援這個函數。</blockquote><br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-commandlinetoargvw"><strong>CommandLineToArgvW</strong></a><br /> | 剖析 Unicode 命令列字串，並傳回命令列引數的指標陣列，以及這類引數的計數，其方式類似于標準 C 執行時間 <em>argv</em> 和 <em>argc</em> 值。<br /> | 
| <a href="/windows/desktop/api/cpl/nc-cpl-applet_proc"><strong>APPLET_PROC</strong></a><br /> | 作為主控台應用程式的進入點。 這是程式庫定義的回呼函數。<br /> | 
| <a href="/windows/desktop/api/Userenv/nf-userenv-createappcontainerprofile"><strong>CreateAppContainerProfile</strong></a><br /> | 針對 Windows Store 應用程式建立每個使用者的個別應用程式佈建檔。<br /> | 
| <a href="/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock"><strong>CreateEnvironmentBlock</strong></a><br /> | 抓取指定使用者的環境變數。 然後可以將這個區塊傳遞給 <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera"><strong>CreateProcessAsUser</strong></a> 函數。<br /> | 
| <a href="createmrulist.md"><strong>CreateMRUListW</strong></a><br /> | 建立最近使用的新 (MRU) 清單。<br /> | 
| <a href="/windows/desktop/api/Userenv/nf-userenv-createprofile"><strong>CreateProfile</strong></a><br /> | 建立新的使用者設定檔。<br /> | 
| <a href="/windows/desktop/api/Scrnsave/nf-scrnsave-defscreensaverproc"><strong>DefScreenSaverProc</strong></a><br /> | 提供螢幕保護裝置應用程式未處理之任何訊息的預設處理。<br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-defsubclassproc"><strong>DefSubclassProc</strong></a><br /> | 呼叫視窗子類別鏈中的下一個處理常式。 子類別鏈中的最後一個處理常式會呼叫視窗的原始視窗程式。<br /> | 
| <a href="/windows/desktop/api/Userenv/nf-userenv-deleteappcontainerprofile"><strong>DeleteAppContainerProfile</strong></a><br /> | 刪除指定的每個使用者、個別應用程式佈建檔。<br /> | 
| <a href="/windows/desktop/api/Userenv/nf-userenv-deleteprofilea"><strong>DeleteProfile</strong></a><br /> | 從指定的電腦刪除使用者設定檔和所有使用者相關的設定。 呼叫端必須具有系統管理許可權，才能刪除使用者的設定檔。<br /> | 
| <a href="/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock"><strong>DestroyEnvironmentBlock</strong></a><br /> | 釋放 <a href="/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock"><strong>CreateEnvironmentBlock</strong></a> 函數所建立的環境變數。<br /> | 
| <a href="/windows/desktop/api/Userenv/nf-userenv-deriveappcontainersidfromappcontainername"><strong>DeriveAppContainerSidFromAppContainerName</strong></a><br /> | 取得指定設定檔的 SID。<br /> | 
| <a href="/windows/desktop/api/userenv/nf-userenv-deriverestrictedappcontainersidfromappcontainersidandrestrictedname"><strong>DeriveRestrictedAppContainerSidFromAppContainerSidAndRestrictedName</strong></a><br /> | DeriveRestrictedAppContainerSidFromAppContainerSidAndRestrictedName 已保留供日後使用。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><em>DLLGETVERSIONPROC</em></a><br /> | 由許多 Windows Shell dll 所執行，可讓應用程式取得 DLL 特定的版本資訊。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles"><strong>DragAcceptFiles</strong></a><br /> | 註冊視窗是否接受已卸載的檔案。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-dragfinish"><strong>DragFinish</strong></a><br /> | 釋放系統組態用來將檔案名傳送至應用程式的記憶體。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea"><strong>DragQueryFile</strong></a><br /> | 抓取成功拖放作業所產生之已卸載檔案的名稱。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint"><strong>DragQueryPoint</strong></a><br /> | 在拖放作業期間卸載檔案時，捕獲滑鼠指標的位置。<br /> | 
| <a href="/windows/desktop/api/shellapi/nf-shellapi-duplicateicon"><strong>DuplicateIcon</strong></a><br /> | 建立重複的指定圖示。<br /> | 
| <a href="/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera"><strong>ExpandEnvironmentStringsForUser</strong></a><br /> | 使用針對指定使用者所建立的環境區塊來展開來源字串。<br /> | 
| <a href="/windows/desktop/api/shellapi/nf-shellapi-extractassociatedicona"><strong>ExtractAssociatedIcon</strong></a><br /> | 取得在檔案中儲存為資源之圖示的控制碼，或儲存在檔案相關聯的可執行檔中的圖示。<br /> | 
| <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticona"><strong>ExtractIcon</strong></a><br /> | 從指定的可執行檔、DLL 或圖示檔取得圖示的控制碼。 <br /> 若要取出大型或小型圖示的控制碼陣列，請使用 <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>ExtractIconEx</strong></a> 函數。<br /> | 
| <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>ExtractIconEx</strong></a><br /> | <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>ExtractIconEx</strong></a>函式會針對從指定的可執行檔、DLL 或圖示檔解壓縮的大型或小型圖示，建立控點的陣列。<br /> | 
| <a href="fileiconinit.md"><strong>FileIconInit</strong></a><br /> | 初始化或重新初始化系統映射清單。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-findexecutablea"><strong>FindExecutable</strong></a><br /> | 抓取與特定檔檔相關聯之可執行檔 (.exe) 檔案的名稱和控制碼。<br /> | 
| <a href="/windows/desktop/api/syncmgr/nf-syncmgr-freeconfirmconflictitem"><strong>FreeConfirmConflictItem</strong></a><br /> | 釋出已配置給 <a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_item"><strong>CONFIRM_CONFLICT_ITEM</strong></a> 結構的資源。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarray"><strong>FreeIDListArray</strong></a><br /> | 釋出項目識別碼清單的指標所使用的記憶體 (PIDL) 清單陣列。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarraychild"><strong>FreeIDListArrayChild</strong></a><br /> | 釋放子專案 Id 之指標陣列的記憶體空間。 這會釋放陣列內的 PITEMID_CHILDs 以及陣列本身。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarrayfull"><strong>FreeIDListArrayFull</strong></a><br /> | 釋放 PIDL 陣列的記憶體空間。 這會釋放陣列內的 PIDLIST_ABSOLUTEs 以及陣列本身。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeknownfolderdefinitionfields"><strong>FreeKnownFolderDefinitionFields</strong></a><br /> | 釋放 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getfolderdefinition"><strong>IKnownFolder：： GetFolderDefinition</strong></a>結果中的配置欄位。<br /> | 
| <a href="freemrulist.md"><strong>FreeMRUList</strong></a><br /> | 釋出與 MRU 清單相關聯的控制碼，並將快取的資料寫入登錄中。<br /> | 
| <a href="/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya"><strong>GetAllUsersProfileDirectory</strong></a><br /> | 抓取目錄根目錄的路徑，其中包含所有使用者共用的程式資料。<br /> | 
| <a href="/windows/desktop/api/Userenv/nf-userenv-getappcontainerfolderpath"><strong>GetAppContainerFolderPath</strong></a><br /> | 取得指定之應用程式容器的本機應用程式資料檔案夾的路徑。<br /> | 
| <a href="/windows/desktop/api/Userenv/nf-userenv-getappcontainerregistrylocation"><strong>GetAppContainerRegistryLocation</strong></a><br /> | 取得與應用程式容器相關聯之登錄儲存體的位置。<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/jj152005(v=vs.85)"><strong>GetContractDelegateWindow</strong></a><br /> | 抓取已設定為應用程式主要前景視窗之委派的視窗，目的是要讓委派視窗與應用程式的合約產生關聯。 如果您是在原生 c + + 中撰寫 Windows Store 應用程式的開發人員，請使用此函數。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-getcurrentprocessexplicitappusermodelid"><strong>GetCurrentProcessExplicitAppUserModelID</strong></a><br /> | 抓取目前進程的應用程式定義、明確應用程式使用者模型識別碼 (AppUserModelID) 。<br /> | 
| <a href="/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya"><strong>GetDefaultUserProfileDirectory</strong></a><br /> | 抓取預設使用者設定檔之根目錄的路徑。<br /> | 
| <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiforshelluicomponent"><strong>GetDpiForShellUiComponent</strong></a><br /> | 根據目前的縮放比例和<a href="/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness"><strong>PROCESS_DPI_AWARENESS</strong></a>，抓取<a href="/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-shell_ui_component"><strong>SHELL_UI_COMPONENT</strong></a>所佔用的每英寸 (DPI) 的點。<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-getmenucontexthelpid"><strong>GetMenuCoNtextHelpId</strong></a><br /> | 抓取與指定功能表相關聯的說明內容識別碼。<br /> | 
| <a href="/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya"><strong>GetProfilesDirectory</strong></a><br /> | 抓取儲存使用者設定檔之根目錄的路徑。<br /> | 
| <a href="/windows/desktop/api/Userenv/nf-userenv-getprofiletype"><strong>GetProfileType</strong></a><br /> | 抓取為目前使用者載入的配置檔案類型。<br /> | 
| <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorfordevice"><strong>GetScaleFactorForDevice</strong></a><br /> | 取得顯示裝置的慣用縮放比例。<br /> | 
| <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorformonitor"><strong>GetScaleFactorForMonitor</strong></a><br /> | 取得特定監視器的縮放比例。 此函數會取代 <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorfordevice"><strong>GetScaleFactorForDevice</strong></a>。<br /> | 
| <a href="/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya"><strong>GetUserProfileDirectory</strong></a><br /> | 抓取指定使用者設定檔之根目錄的路徑。<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-getwindowcontexthelpid"><strong>GetWindowCoNtextHelpId</strong></a><br /> | 抓取與指定視窗相關聯的說明內容識別碼（如果有的話）。<br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-getwindowsubclass"><strong>GetWindowSubclass</strong></a><br /> | 抓取所指定視窗子類別回呼的參考資料。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-idlistcontainerisconsistent"><strong>IDListContainerIsConsistent</strong></a><br /> | 驗證 Idlist.txt 的容器結構是否有效。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilappendid"><strong>ILAppendID</strong></a><br /> | 將 <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> 結構附加或附加至 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclone"><strong>ILClone</strong></a><br /> | 複製 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonechild"><strong>ILCloneChild</strong></a><br /> | 複製子 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonefirst"><strong>ILCloneFirst</strong></a><br /> | 複製<a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a>結構中的第一個<a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a>結構。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonefull"><strong>ILCloneFull</strong></a><br /> | 複製完整或絕對的 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilcombine"><strong>ILCombine</strong></a><br /> | 結合兩個 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilcreatefrompath"><strong>ILCreateFromPath</strong></a><br /> | 傳回與指定檔案路徑相關聯的 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfindchild"><strong>ILFindChild</strong></a><br /> | 判斷指定的 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構是否為另一個 <strong>ITEMIDLIST</strong> 結構的子系。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfindlastid"><strong>ILFindLastID</strong></a><br /> | 傳回<a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a>結構中最後一個<a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a>結構的指標。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree"><strong>ILFree</strong></a><br /> | 釋放由 Shell 配置的 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilgetnext"><strong>ILGetNext</strong></a><br /> | 捕獲<a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a>結構中的下一個<a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a>結構。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilgetsize"><strong>ILGetSize</strong></a><br /> | 傳回 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構的大小（以位元組為單位）。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisaligned"><strong>ILIsAligned</strong></a><br /> | 驗證常數 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 是否對齊指標界限，也就是32位架構上的 <strong>DWORD</strong> 和64位架構上的 <strong>QWORD</strong> 。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilischild"><strong>ILIsChild</strong></a><br /> | 驗證 PIDL 是否為子 PIDL，也就是只有一個 <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a>的 PIDL。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisempty"><strong>ILIsEmpty</strong></a><br /> | 確認 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構是否為空白。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisequal"><strong>ILIsEqual</strong></a><br /> | 測試兩個 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構是否相等於二進位比較。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisparent"><strong>ILIsParent</strong></a><br /> | 測試 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構是否為另一個 <strong>ITEMIDLIST</strong> 結構的父代。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilnext"><strong>ILNext (PCUIDLIST_RELATIVE) </strong></a><br /> | 捕獲<a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a>結構中的下一個<a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a>結構。<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/bb776455(v=vs.85)"><strong>ILNext (PUIDLIST_RELATIVE) </strong></a><br /> | 捕獲<a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a>結構中的下一個<a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a>結構。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilremovelastid"><strong>ILRemoveLastID</strong></a><br /> | 從<a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a>結構移除最後一個<a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a>結構。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilsavetostream"><strong>ILSaveToStream</strong></a><br /> | 將 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構儲存至資料流程。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilskip"><strong>ILSkip (PCUIDLIST_RELATIVE，UINT) </strong></a><br /> | 略過常數、未對齊、相對 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構中指定的位元組數目。<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/bb776459(v=vs.85)"><strong>ILSkip (PUIDLIST_RELATIVE，UINT) </strong></a><br /> | 略過未對齊、相對 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構中指定的位元組數目。<br /> | 
| <a href="/windows/desktop/api/Intshcut/nf-intshcut-inetisoffline"><strong>InetIsOffline</strong></a><br /> | 判斷系統是否已連線到網際網路。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol"><strong>InitNetworkAddressControl</strong></a><br /> | 初始化網路位址控制視窗類別。<br /> | 
| <a href="/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea"><strong>LoadUserProfile</strong></a><br /> | 載入指定的使用者設定檔。 設定檔可以是 <a href="local-user-profiles.md">本機使用者配置</a> 檔或 <a href="roaming-user-profiles.md">漫遊使用者設定檔</a>。<br /> | 
| <a href="/windows/desktop/api/Intshcut/nf-intshcut-mimeassociationdialoga"><strong>MIMEAssociationDialog</strong></a><br /> | 執行 [未註冊的 MIME 內容類型] 對話方塊。<br /><blockquote>[!Note]<br />WindowsXP Service Pack 2 (SP2) 或更新版本：不再支援此功能。</blockquote><br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathmakeuniquename"><strong>PathMakeUniqueName</strong></a><br /> | 從範本建立唯一的路徑名稱。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathyetanothermakeuniquename"><strong>PathYetAnotherMakeUniqueName</strong></a><br /> | 根據現有的檔案名建立唯一的檔案名。<br /> | 
| <a href="/windows/desktop/api/appnotify/nf-appnotify-registerappstatechangenotification"><strong>RegisterAppStateChangeNotification</strong></a><br /> | 可讓應用程式註冊回呼函式，以通知其程式庫即將進入或離開暫停狀態。 應用程式可以使用此資訊來執行任何必要的作業，例如在該時間點執行的保留狀態。<br /> | 
| <a href="/windows/desktop/api/Scrnsave/nf-scrnsave-registerdialogclasses"><strong>RegisterDialogClasses</strong></a><br /> | 註冊螢幕保護裝置程式的設定對話方塊所需的任何非標準視窗類別。<br /> | 
| <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>RegisterScaleChangeEvent</strong></a><br /> | 註冊當調整規模可能變更時所觸發的事件。 此函數會取代 <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangenotifications"><strong>RegisterScaleChangeNotifications</strong></a>。<br /> | 
| <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangenotifications"><strong>RegisterScaleChangeNotifications</strong></a><br /> | 註冊視窗，以在調整資訊變更時接收回呼。<br /><blockquote>[!Note]<br />Windows 8.1 不支援這個函數。 請改用 <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>RegisterScaleChangeEvent</strong></a> 。</blockquote><br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass"><strong>RemoveWindowSubclass</strong></a><br /> | 從視窗中移除子類別回呼。<br /> | 
| <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-revokescalechangenotifications"><strong>RevokeScaleChangeNotifications</strong></a><br /> | 撤銷視窗的註冊，防止它在調整資訊變更時接收回呼。<br /><blockquote>[!Note]<br />Windows 8.1 不支援這個函數。 請改用 <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-unregisterscalechangeevent"><strong>UnregisterScaleChangeEvent</strong></a> 。</blockquote><br /> | 
| <a href="/windows/desktop/api/Scrnsave/nf-scrnsave-screensaverconfiguredialog"><strong>ScreenSaverConfigureDialog</strong></a><br /> | 接收傳送至螢幕保護裝置程式之 [設定] 對話方塊的訊息。 允許使用者設定的螢幕保護裝置必須定義此功能。<br /> | 
| <a href="/windows/desktop/api/Scrnsave/nf-scrnsave-screensaverproc"><strong>ScreenSaverProc</strong></a><br /> | 接收傳送到指定螢幕保護裝置視窗的訊息。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcontractdelegatewindow"><strong>SetContractDelegateWindow</strong></a><br /> | 將主要前景視窗以外的應用程式視窗與應用程式的合約產生關聯。 如果您是在原生 c + + 中撰寫 Windows Store 應用程式的開發人員，請使用此函數。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid"><strong>SetCurrentProcessExplicitAppUserModelID</strong></a><br /> | 指定唯一的應用程式定義 AppUserModelID，識別工作列目前的進程。 此識別碼可讓應用程式在單一工作列按鈕下將其相關聯的進程和視窗分組。<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-setmenucontexthelpid"><strong>SetMenuCoNtextHelpId</strong></a><br /> | 讓說明內容識別碼與功能表產生關聯。<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-setwindowcontexthelpid"><strong>SetWindowCoNtextHelpId</strong></a><br /> | 將說明內容識別碼與指定的視窗產生關聯。<br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass"><strong>SetWindowSubclass</strong></a><br /> | 安裝或更新視窗子類別回呼。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a><br /> | 通知系統已存取專案，目的是要追蹤最近和最常使用的專案。 此函式也可用來清除所有使用方式資料。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage"><strong>SHAppBarMessage</strong></a><br /> | 將 appbar 訊息傳送至系統。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shassocenumhandlers"><strong>SHAssocEnumHandlers</strong></a><br /> | 傳回指定的一組副檔名處理常式的列舉物件。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shassocenumhandlersforprotocolbyapplication"><strong>SHAssocEnumHandlersForProtocolByApplication</strong></a><br /> | 取得列舉介面，這個介面可讓您存取與指定通訊協定相關聯的處理常式。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparent"><strong>SHBindToFolderIDListParent</strong></a><br /> | 指定以資料夾格式指定的 Shell 命名空間專案，以及相對於該資料夾的專案識別碼清單，此函式會系結至命名空間專案的父系，並選擇性地將指標傳回至專案識別碼清單的最後一個元件。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparentex"><strong>SHBindToFolderIDListParentEx</strong></a><br /> | 藉由允許呼叫端指定系結內容來擴充 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparent"><strong>SHBindToFolderIDListParent</strong></a> 函數。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoobject"><strong>SHBindToObject</strong></a><br /> | 使用 Shell 命名空間 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder：： BindToObject</strong></a> 方法，來抓取並系結至指定的物件。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent"><strong>SHBindToParent</strong></a><br /> | 取得完整專案識別碼清單的指標 (PIDL) ，並傳回父物件上的指定介面指標。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera"><strong>SHBrowseForFolder</strong></a><br /> | 顯示可讓使用者選取 Shell 資料夾的對話方塊。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotification_lock"><strong>SHChangeNotification_Lock</strong></a><br /> | 鎖定與 Shell 變更通知事件相關聯的共用記憶體。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotification_unlock"><strong>SHChangeNotification_Unlock</strong></a><br /> | 將變更通知的共用記憶體解除鎖定。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify"><strong>SHChangeNotify</strong></a><br /> | 通知系統已執行應用程式的事件。 如果應用程式執行的動作可能會影響 Shell，則應該使用此函式。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyderegister"><strong>SHChangeNotifyDeregister</strong></a><br /> | 從接收 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify"><strong>SHChangeNotify</strong></a> 訊息中取消註冊用戶端的視窗進程。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister"><strong>SHChangeNotifyRegister</strong></a><br /> | 註冊視窗，以從檔案系統或 Shell 接收通知（如果檔案系統支援通知）。<br /> | 
| <a href="/windows/desktop/api/Shlobj/nf-shlobj-shchangenotifyregisterthread"><strong>SHChangeNotifyRegisterThread</strong></a><br /> | 啟用執行緒的非同步登錄和取消註冊。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateassociationregistration"><strong>SHCreateAssociationRegistration</strong></a><br /> | 根據 Windows 所提供介面的內建執行，建立<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>IApplicationAssociationRegistration</strong></a>物件。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedataobject"><strong>SHCreateDataObject</strong></a><br /> | 在父資料夾中建立資料物件。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>SHCreateDefaultCoNtextMenu</strong></a><br /> | 建立物件，這個物件表示 Shell 的預設內容功能表執行。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreatedefaultextracticon"><strong>SHCreateDefaultExtractIcon</strong></a><br /> | 建立標準圖示解壓縮解壓縮，可透過 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultextracticoninit"><strong>IDefaultExtractIconInit</strong></a> 介面進一步設定其預設值。<br /> | 
| <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-shcreatedefaultpropertiesop"><strong>SHCreateDefaultPropertiesOp</strong></a><br /> | 建立檔案作業，此作業會在 Shell 專案上設定尚未設定的預設屬性。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromidlist"><strong>SHCreateItemFromIDList</strong></a><br /> | 從 PIDL 建立並初始化 Shell 專案物件。 產生的 shell 專案物件支援 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> 介面。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a><br /> | 從剖析名稱建立並初始化殼層項目物件。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromrelativename"><strong>SHCreateItemFromRelativeName</strong></a><br /> | 從相對剖析名稱建立並初始化 Shell 專案物件。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateiteminknownfolder"><strong>SHCreateItemInKnownFolder</strong></a><br /> | 針對存在於已知資料夾內的單一檔案，建立 Shell 專案物件。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemwithparent"><strong>SHCreateItemWithParent</strong></a><br /> | 建立 Shell 專案，指定父資料夾和子專案識別碼。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a><br /> | 建立預設 Shell 資料夾 view 物件 (DefView) 的新實例。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex"><strong>SHCreateShellFolderViewEx</strong></a><br /> | 建立預設 Shell 資料夾 view 物件的新實例。 建議您使用 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a> ，而不是使用此函數。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellitem"><strong>SHCreateShellItem</strong></a><br /> | 建立 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> 物件。 <br /><blockquote>[!Note]<br />建議您使用 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemwithparent"><strong>SHCreateItemWithParent</strong></a> 或 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromidlist"><strong>SHCreateItemFromIDList</strong></a> ，而不是使用此函數。</blockquote><br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarray"><strong>SHCreateShellItemArray</strong></a><br /> | 建立 Shell 專案陣列物件。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject"><strong>SHCreateShellItemArrayFromDataObject</strong></a><br /> | 從資料物件建立 Shell 專案陣列物件。 <br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromidlists"><strong>SHCreateShellItemArrayFromIDLists</strong></a><br /> | 從 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構的清單建立 Shell 專案陣列物件。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromshellitem"><strong>SHCreateShellItemArrayFromShellItem</strong></a><br /> | 從單一 Shell 專案建立一個元素的陣列。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shdefextracticona"><strong>SHDefExtractIcon</strong></a><br /> | 提供預設的處理常式，從檔案中解壓縮圖示。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop"><strong>SHDoDragDrop</strong></a><br /> | 執行拖放操作。 支援視需要拖曳來源建立，以及拖曳影像。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona"><strong>Shell_NotifyIcon</strong></a><br /> | 將訊息傳送至工作列的狀態區域。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect"><strong>Shell_NotifyIconGetRect</strong></a><br /> | 取得通知圖示周框的螢幕座標。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellabouta"><strong>ShellAbout</strong></a><br /> | 顯示 [ <strong>ShellAbout</strong> ] 對話方塊。<br /> | 
| <a href="shellddeinit.md"><strong>ShellDDEInit</strong></a><br /> | 在目前的進程中註冊 Shell 動態資料交換 (DDE) 服務，通知系統目前的進程希望裝載 DDE 物件。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea"><strong>ShellExecute</strong></a><br /> | 在指定的檔案上執行操作。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a><br /> | 在指定的檔案上執行操作。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shemptyrecyclebina"><strong>SHEmptyRecycleBin</strong></a><br /> | 清空指定磁片磁碟機上的資源回收筒。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shenumerateunreadmailaccountsa"><strong>SHEnumerateUnreadMailAccounts</strong></a><br /> | 列舉具有未讀取電子郵件的使用者帳戶。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shevaluatesystemcommandtemplate"><strong>SHEvaluateSystemCommandTemplate</strong></a><br /> | 對 <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> 或 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea"><strong>ShellExecute</strong></a>的呼叫中所使用的參數強制執行嚴格驗證。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a><br /> | 複製、移動、重新命名或刪除檔案系統物件。 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a>已在 Windows Vista 中取代此函式。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfreenamemappings"><strong>SHFreeNameMappings</strong></a><br /> | 釋放 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> 函式所取出的檔案名對應物件。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdatafromidlista"><strong>SHGetDataFromIDList</strong></a><br /> | 從相對識別碼清單抓取擴充屬性資料。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder"><strong>SHGetDesktopFolder</strong></a><br /> | 抓取桌面資料夾的 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> 介面，也就是 Shell 命名空間的根目錄。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetdiskfreespaceexa"><strong>SHGetDiskFreeSpaceEx</strong></a><br /> | 捕獲磁片區的磁碟空間資訊。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetdrivemedia"><strong>SHGetDriveMedia</strong></a><br /> | 傳回指定磁片磁碟機中的媒體類型。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetfileinfoa"><strong>SHGetFileInfo</strong></a><br /> | 抓取檔案系統中物件的相關資訊，例如檔案、資料夾、目錄或磁片磁碟機根目錄。<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/mt757093(v=vs.85)"><strong>SHGetFolderPathEx</strong></a><br /> | 抓取資料夾的 <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a>所識別之已知資料夾的完整路徑。 這可讓您設定字串緩衝區的初始大小，藉此擴充 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath"><strong>SHGetKnownFolderPath</strong></a> 。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgeticonoverlayindexa"><strong>SHGetIconOverlayIndex</strong></a><br /> | 傳回系統映射清單中覆迭圖示的索引。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetidlistfromobject"><strong>SHGetIDListFromObject</strong></a><br /> | 抓取物件的 PIDL。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetimagelist"><strong>SHGetImageList</strong></a><br /> | 抓取影像清單。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetinstanceexplorer"><strong>SHGetInstanceExplorer</strong></a><br /> | 抓取允許裝載 Shell 擴充和其他元件的介面，以防止其主機進程提前關閉。 主機進程通常 Windows 檔案總管或 Windows Internet Explorer，但其他應用程式也可以使用此函式。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromdataobject"><strong>SHGetItemFromDataObject</strong></a><br /> | 根據<a href="/windows/desktop/api/objidl/nn-objidl-idataobject"><strong>IDataObject</strong></a>指定的專案，建立<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>或相關的物件。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromobject"><strong>SHGetItemFromObject</strong></a><br /> | 抓取物件的 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> 。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist"><strong>SHGetKnownFolderIDList</strong></a><br /> | 以 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構的形式抓取已知資料夾的路徑。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderitem"><strong>SHGetKnownFolderItem</strong></a><br /> | 抓取代表已知資料夾的 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> 物件。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath"><strong>SHGetKnownFolderPath</strong></a><br /> | 抓取資料夾的 <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a>所識別之已知資料夾的完整路徑。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetlocalizedname"><strong>SHGetLocalizedName</strong></a><br /> | 抓取 Shell 資料夾中檔案的當地語系化名稱。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetnamefromidlist"><strong>SHGetNameFromIDList</strong></a><br /> | 抓取其 Idlist.txt 所識別之專案的顯示名稱。<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/bb762192(v=vs.85)"><strong>SHGetNameFromPropertyKey</strong></a><br /> | 根據指定的 <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a>，抓取屬性的正式名稱。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetnewlinkinfoa"><strong>SHGetNewLinkInfo</strong></a><br /> | 根據快捷方式的建議目標，建立新快速鍵的名稱。 此函式不會建立快捷方式，只會建立名稱。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista"><strong>SHGetPathFromIDList</strong></a><br /> | 將專案識別碼清單轉換成檔案系統路徑。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlistex"><strong>SHGetPathFromIDListEx</strong></a><br /> | 將專案識別碼清單轉換成檔案系統路徑。 此函式可讓您設定字串緩衝區的初始大小，並宣告下列選項，藉以擴充 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista"><strong>SHGetPathFromIDList</strong></a> 。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsettings"><strong>SHGetSettings</strong></a><br /> | 抓取目前的 Shell 選項設定。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>SHGetStockIconInfo</strong></a><br /> | 抓取系統定義之 Shell 圖示的相關資訊。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgettemporarypropertyforitem"><strong>SHGetTemporaryPropertyForItem</strong></a><br /> | 抓取指定專案的暫存屬性。 暫存屬性是一種讀取/寫入存放區，只保留 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> 物件存留期的屬性，而不是保存回專案中。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetunreadmailcountw"><strong>SHGetUnreadMailCount</strong></a><br /> | 抓取任何或所有電子郵件帳戶的指定使用者未讀取訊息計數。<br /> | 
| <a href="/windows/desktop/api/shellapi/nf-shellapi-shisfileavailableoffline"><strong>SHIsFileAvailableOffline</strong></a><br /> | 判斷檔案或資料夾是否可供離線使用。 此函式也會決定要從網路、本機離線檔案快取或從這兩個位置開啟檔案。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shloadinproc"><strong>SHLoadInProc</strong></a><br /> | 從 Shell 進程的內容中，建立指定之物件類別的實例。 <br /><strong>Windows Vista</strong>和更新版本：此函式已停用，並傳回 E_NOTIMPL。<br /> | 
| <a href="/windows/desktop/api/shellapi/nf-shellapi-shloadnonloadediconoverlayidentifiers"><strong>SHLoadNonloadedIconOverlayIdentifiers</strong></a><br /> | 表示在下一次執行需要重迭資訊的作業期間，應該載入可能無法建立或不存在於啟動時建立的圖示重迭識別碼。 已載入的識別碼不會受到影響。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shlocalstrdupa"><strong>SHLocalStrDup</strong></a><br /> | 在新配置的記憶體中建立字串的複本。<br /> | 
| <a href="/windows/desktop/api/Shlobj/nf-shlobj-shmultifileproperties"><strong>SHMultiFileProperties</strong></a><br /> | 顯示一組檔案的合併屬性工作表。 會顯示所有檔案通用的屬性值，而不同的屬性值會顯示 <strong> (多個值) </strong>的字串。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenfolderandselectitems"><strong>SHOpenFolderAndSelectItems</strong></a><br /> | 開啟 Windows 檔案總管視窗，其中已選取特定資料夾中的指定專案。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenwithdialog"><strong>SHOpenWithDialog</strong></a><br /> | 顯示 [ <strong>開啟方式</strong> ] 對話方塊。<br /> | 
| <a href="/windows/desktop/shell/showsharefolderui"><strong>ShowShareFolderUI</strong></a><br /> | 在 [內容] 工作表上，顯示指定資料夾的 [ <strong>資料夾共用</strong> ] 索引標籤。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shparsedisplayname"><strong>SHParseDisplayName</strong></a><br /> | 將 Shell 命名空間物件的顯示名稱轉譯為專案識別碼清單，並傳回物件的屬性。 此函數是將字串轉換成 PIDL 的慣用方法。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shpathprepareforwritea"><strong>SHPathPrepareForWrite</strong></a><br /> | 檢查路徑是否存在。 這包括重新掛接對應的網路磁碟機機、提示 ejectable 媒體重新插入、建立路徑、提示媒體格式化，以及提供適當的使用者介面（如有必要）。 系統不會檢查媒體的讀取/寫入權限。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryrecyclebina"><strong>SHQueryRecycleBin</strong></a><br /> | 針對指定的磁片磁碟機抓取資源回收筒的大小和其中的專案數目。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate"><strong>SHQueryUserNotificationState</strong></a><br /> | 檢查目前使用者電腦的狀態，以判斷傳送通知是否適當。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shremovelocalizedname"><strong>SHRemoveLocalizedName</strong></a><br /> | 移除 Shell 資料夾中檔案的當地語系化名稱。<br /> | 
| <a href="/windows/desktop/api/Shlobj/nf-shlobj-shruncontrolpanel"><strong>SHRunControlPanel</strong></a><br /> | 開啟主控台專案。 <br /><blockquote>[!Note]<br />Windows Vista 不支援此功能</blockquote><br /> | 
| <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-shsetdefaultproperties"><strong>SHSetDefaultProperties</strong></a><br /> | 套用 Shell 專案的預設屬性集。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetinstanceexplorer"><strong>SHSetInstanceExplorer</strong></a><br /> | 提供介面，允許裝載的 Shell 擴充和其他元件，以防止其主機進程提前關閉。 主機進程通常是 Windows 檔案總管或 Internet Explorer，但其他應用程式也可以使用此函數。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath"><strong>SHSetKnownFolderPath</strong></a><br /> | 將已知資料夾重新導向至新的位置。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shsetlocalizedname"><strong>SHSetLocalizedName</strong></a><br /> | 設定 Shell 資料夾中檔案的當地語系化名稱。<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shsettemporarypropertyforitem"><strong>SHSetTemporaryPropertyForItem</strong></a><br /> | 設定指定之專案的暫時屬性。 暫存屬性會保留在讀取/寫入存放區中，只保留 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> 物件存留期的屬性，而不是將它們寫回專案中。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shsetunreadmailcountw"><strong>SHSetUnreadMailCount</strong></a><br /> | 將指定之電子郵件帳戶的目前使用者未讀取訊息計數儲存在登錄中。<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shtesttokenmembership"><strong>SHTestTokenMembership</strong></a><br /> | 使用 <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-checktokenmembership"><strong>CheckTokenMembership</strong></a> 來測試指定的標記是否為具有指定 RID 之本機群組的成員。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shupdateimagea"><strong>SHUpdateImage</strong></a><br /> | 通知 Shell 系統映射清單中的影像已變更。<br /> | 
| <a href="/windows/desktop/api/Shlobj/nf-shlobj-softwareupdatemessagebox"><strong>SoftwareUpdateMessageBox</strong></a><br /> | 顯示標準訊息方塊，可用來通知使用者應用程式已更新。<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-stgmakeuniquename"><strong>StgMakeUniqueName</strong></a><br /> | 從範本建立資料流程或儲存物件的唯一名稱。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstrniw"><strong>StrStrNIW</strong></a><br /> | 在字串中尋找第一個出現的子字串。 此比較不區分大小寫。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstrnw"><strong>StrStrNW</strong></a><br /> | 在字串中尋找第一個出現的子字串。 比較會區分大小寫。<br /> | 
| <a href="/windows/desktop/api/Intshcut/nf-intshcut-translateurla"><strong>TranslateURL</strong></a><br /> | 將一般翻譯套用至指定的 URL 字串，建立新的 URL 字串。<br /> | 
| <a href="/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile"><strong>UnloadUserProfile</strong></a><br /> | 卸載 <a href="/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea"><strong>LoadUserProfile</strong></a> 函數所載入的使用者設定檔。 呼叫端必須具有電腦的系統管理許可權。 如需詳細資訊，請參閱 <strong>LoadUserProfile</strong> 函數的「備註」一節。<br /> | 
| <a href="/windows/desktop/api/appnotify/nf-appnotify-unregisterappstatechangenotification"><strong>UnregisterAppStateChangeNotification</strong></a><br /> | 取消透過 <a href="/windows/desktop/api/appnotify/nf-appnotify-registerappstatechangenotification"><strong>RegisterAppStateChangeNotification</strong></a>註冊的變更通知。<br /> | 
| <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-unregisterscalechangeevent"><strong>UnregisterScaleChangeEvent</strong></a><br /> | 取消註冊透過 <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>RegisterScaleChangeEvent</strong></a>註冊的調整變更事件。 此函數會取代 <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-revokescalechangenotifications"><strong>RevokeScaleChangeNotifications</strong></a>。<br /> | 
| <a href="/windows/desktop/api/Intshcut/nf-intshcut-urlassociationdialoga"><strong>URLAssociationDialog</strong></a><br /> | 叫用未註冊的 [URL 通訊協定] 對話方塊。 此對話方塊可讓使用者選取要與先前未知通訊協定相關聯的應用程式。<br /><blockquote>[!Note]<br />WindowsXP SP2 或更新版本：不再支援此功能。</blockquote><br /> | 
| <a href="/previous-versions/windows/desktop/legacy/bb762266(v=vs.85)"><strong>WinExecError</strong></a><br /> | 如果 <a href="/windows/win32/api/winbase/nf-winbase-winexec">WinExec</a> 函式無法執行指定的應用程式，則抓取產生的錯誤值。 <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-winhelpa"><strong>WinHelp</strong></a><br /> | 啟動 Windows 說明 (Winhelp.exe) 並傳遞其他資料，以指出應用程式所要求之說明的本質。<br /> | 




 

 

 
