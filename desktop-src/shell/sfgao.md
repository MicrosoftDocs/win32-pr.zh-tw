---
description: 可以在專案 (檔案或資料夾) 或一組專案上抓取的屬性。
ms.assetid: 4cb85995-cdc8-4474-8c4d-c783ac91c759
title: 'SFGAO (Shobjidl.h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a5ae5dca355b7c22e3075a0ced7640a5bd45a54
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481984"
---
# <a name="sfgao"></a>SFGAO

可以在專案 (檔案或資料夾) 或一組專案上抓取的屬性。




| 常數/值 | Description | 
|----------------|-------------|
| <span id="SFGAO_CANCOPY"></span><span id="sfgao_cancopy"></span><dl><dt><strong>SFGAO_CANCOPY</strong></dt><dt>0x00000001</dt></dl> | 您可以複製指定的專案。<br /> | 
| <span id="SFGAO_CANMOVE"></span><span id="sfgao_canmove"></span><dl><dt><strong>SFGAO_CANMOVE</strong></dt><dt>0x00000002</dt></dl> | 您可以移動指定的專案。<br /> | 
| <span id="SFGAO_CANLINK"></span><span id="sfgao_canlink"></span><dl><dt><strong>SFGAO_CANLINK</strong></dt><dt>0x00000004</dt></dl> | 您可以為指定的專案建立快捷方式。 這個屬性與 <a href="/windows/desktop/com/dropeffect-constants"><strong>DROPEFFECT_LINK</strong></a>的值相同。 <br /> 如果命名空間延伸模組傳回這個屬性，則會在拖放作業期間，將具有預設處理常式的 <strong>建立快捷方式</strong> 專案加入至顯示的快捷方式功能表。 延伸模組也可以針對 <em>連結</em> 動詞來執行自己的處理常式，以取代預設值。 如果延伸模組這麼做，它會負責建立快捷方式。<br /> [<strong>建立快捷方式</strong>] 專案也會加入至<strong>[Windows 檔案總管檔案</strong>] 功能表和一般快捷方式功能表。<br /> 如果選取專案，則會叫用應用程式的<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>ICoNtextMenu：： InvokeCommand</strong></a>方法，並將<a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a>結構的<strong>lpVerb</strong>成員設為<em>連結</em>。 您的應用程式會負責建立連結。<br /> | 
| <span id="SFGAO_STORAGE"></span><span id="sfgao_storage"></span><dl><dt><strong>SFGAO_STORAGE</strong></dt><dt>0x00000008</dt></dl> | 指定的專案可以透過<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder：： BindToObject</strong></a>系結至<a href="/windows/desktop/api/objidl/nn-objidl-istorage"><strong>IStorage</strong></a>物件。 如需命名空間操作功能的詳細資訊，請參閱 <strong>IStorage</strong>。<br /> | 
| <span id="SFGAO_CANRENAME"></span><span id="sfgao_canrename"></span><dl><dt><strong>SFGAO_CANRENAME</strong></dt><dt>0x00000010</dt></dl> | 您可以重新命名指定的專案。 請注意，此值基本上是建議事項;並非所有命名空間用戶端都允許重新命名專案。 但是，必須設定這個屬性。<br /> | 
| <span id="SFGAO_CANDELETE"></span><span id="sfgao_candelete"></span><dl><dt><strong>SFGAO_CANDELETE</strong></dt><dt>0x00000020</dt></dl> | 可以刪除指定的專案。<br /> | 
| <span id="SFGAO_HASPROPSHEET"></span><span id="sfgao_haspropsheet"></span><dl><dt><strong>SFGAO_HASPROPSHEET</strong></dt><dt>0x00000040</dt></dl> | 指定的專案具有屬性工作表。<br /> | 
| <span id="SFGAO_DROPTARGET"></span><span id="sfgao_droptarget"></span><dl><dt><strong>SFGAO_DROPTARGET</strong></dt><dt>0x00000100</dt></dl> | 指定的專案是放置目標。<br /> | 
| <span id="SFGAO_CAPABILITYMASK"></span><span id="sfgao_capabilitymask"></span><dl><dt><strong>SFGAO_CAPABILITYMASK</strong></dt><dt>0x00000177</dt></dl> | 此旗標是功能屬性的遮罩： SFGAO_CANCOPY、SFGAO_CANMOVE、SFGAO_CANLINK、SFGAO_CANRENAME、SFGAO_CANDELETE、SFGAO_HASPROPSHEET 和 SFGAO_DROPTARGET。 呼叫端通常不會使用此值。<br /> | 
| <span id="SFGAO_SYSTEM"></span><span id="sfgao_system"></span><dl><dt><strong>SFGAO_SYSTEM</strong></dt><dt>0x00001000</dt></dl> | <strong>Windows 7 和更新版本</strong>。 指定的專案為系統專案。<br /> | 
| <span id="SFGAO_ENCRYPTED"></span><span id="sfgao_encrypted"></span><dl><dt><strong>SFGAO_ENCRYPTED</strong></dt><dt>0x00002000</dt></dl> | 指定的專案會加密，而且可能需要特殊的簡報。<br /> | 
| <span id="SFGAO_ISSLOW"></span><span id="sfgao_isslow"></span><dl><dt><strong>SFGAO_ISSLOW</strong></dt><dt>0x00004000</dt></dl> | 透過 <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a> 或其他儲存體介面存取 (的專案，) 預期會是很慢的作業。 應用程式應該避免存取以 SFGAO_ISSLOW 標記的專案。 <br /><blockquote>[!Note]<br />開啟專案的資料流程通常是緩慢的作業。 SFGAO_ISSLOW 指出預期的速度特別慢，例如，當網路連線緩慢或離線 (FILE_ATTRIBUTE_OFFLINE) 檔時。 不過，查詢 SFGAO_ISSLOW 本身是一項緩慢的操作。 應用程式應該只在背景執行緒上查詢 SFGAO_ISSLOW。 替代方法（例如，抓取 <a href="/windows/desktop/properties/props-system-fileattributes"><strong>PKEY_FileAttributes</strong></a> 屬性和測試 FILE_ATTRIBUTE_OFFLINE）可以用來取代涉及 SFGAO_ISSLOW 的方法呼叫。</blockquote><br /> | 
| <span id="SFGAO_GHOSTED"></span><span id="sfgao_ghosted"></span><dl><dt><strong>SFGAO_GHOSTED</strong></dt><dt>0x00008000</dt></dl> | 指定的專案會顯示為暗灰色，而且無法供使用者使用。<br /> | 
| <span id="SFGAO_LINK"></span><span id="sfgao_link"></span><dl><dt><strong>SFGAO_LINK</strong></dt><dt>0x00010000</dt></dl> | 指定的專案是快捷方式。<br /> | 
| <span id="SFGAO_SHARE"></span><span id="sfgao_share"></span><dl><dt><strong>SFGAO_SHARE</strong></dt><dt>0x00020000</dt></dl> | 指定的物件是共用的。<br /> | 
| <span id="SFGAO_READONLY"></span><span id="sfgao_readonly"></span><dl><dt><strong>SFGAO_READONLY</strong></dt><dt>0x00040000</dt></dl> | 指定的專案是唯讀的。 如果是資料夾，這表示無法在這些資料夾中建立新專案。 這不應該與<a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumndata"><strong>SHCOLUMNDATA</strong></a>結構中<a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata"><strong>IColumnProvider：： GetItemData</strong></a>所抓取 FILE_ATTRIBUTE_READONLY 旗標所指定的行為混淆。 FILE_ATTRIBUTE_READONLY 對 Win32 檔系統資料夾沒有任何意義。<br /> | 
| <span id="SFGAO_HIDDEN"></span><span id="sfgao_hidden"></span><dl><dt><strong>SFGAO_HIDDEN</strong></dt><dt>0x00080000</dt></dl> | 專案會隱藏，除非在<strong>資料夾設定</strong>中啟用 [<strong>顯示隱藏的檔案和資料夾</strong>] 選項，否則不應顯示此專案。<br /> | 
| <span id="SFGAO_DISPLAYATTRMASK"></span><span id="sfgao_displayattrmask"></span><dl><dt><strong>SFGAO_DISPLAYATTRMASK</strong></dt><dt>0x000FC000</dt></dl> | 請勿使用。<br /> | 
| <span id="SFGAO_NONENUMERATED"></span><span id="sfgao_nonenumerated"></span><dl><dt><strong>SFGAO_NONENUMERATED</strong></dt><dt>0x00100000</dt></dl> | 專案是 nonenumerated 專案，而且應該隱藏。 它們不會透過 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>IShellFolder：： EnumObjects</strong></a> 方法所建立的列舉值來傳回。<br /> | 
| <span id="SFGAO_NEWCONTENT"></span><span id="sfgao_newcontent"></span><dl><dt><strong>SFGAO_NEWCONTENT</strong></dt><dt>0x00200000</dt></dl> | 專案包含新的內容，如特定應用程式所定義。<br /> | 
| <span id="SFGAO_CANMONIKER"></span><span id="sfgao_canmoniker"></span><dl><dt><strong>SFGAO_CANMONIKER</strong></dt></dl> | 不支援。<br /> | 
| <span id="SFGAO_HASSTORAGE"></span><span id="sfgao_hasstorage"></span><dl><dt><strong>SFGAO_HASSTORAGE</strong></dt></dl> | 不支援。<br /> | 
| <span id="SFGAO_STREAM"></span><span id="sfgao_stream"></span><dl><dt><strong>SFGAO_STREAM</strong></dt><dt>0x00400000</dt></dl> | 指出專案具有與其相關聯的資料流程。 您可以透過呼叫 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder：： BindToObject</strong></a> 或 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem：： BindToHandler</strong></a> ，在 <em>riid</em> 參數中使用 IID_IStream 來存取該資料流程。<br /> | 
| <span id="SFGAO_STORAGEANCESTOR"></span><span id="sfgao_storageancestor"></span><dl><dt><strong>SFGAO_STORAGEANCESTOR</strong></dt><dt>0x00800000</dt></dl> | 此專案的子系可透過 <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a> 或 <a href="/windows/desktop/api/objidl/nn-objidl-istorage"><strong>IStorage</strong></a>存取。 這些子系會標示 SFGAO_STORAGE 或 SFGAO_STREAM。<br /> | 
| <span id="SFGAO_VALIDATE"></span><span id="sfgao_validate"></span><dl><dt><strong>SFGAO_VALIDATE</strong></dt><dt>0x01000000</dt></dl> | 當指定為輸入時，SFGAO_VALIDATE 指示資料夾驗證資料夾或 Shell 專案陣列中包含的專案是否存在。 如果其中一或多個專案不存在， <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof"><strong>IShellFolder：： GetAttributesOf</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getattributes"><strong>IShellItemArray：： GetAttributes</strong></a> 會傳回失敗碼。 此旗標絕不會以 [out] 值傳回。<br /> 搭配檔系統資料夾使用時，SFGAO_VALIDATE 會指示資料夾捨棄 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex"><strong>IShellFolder2：： GetDetailsEx</strong></a> 用戶端所抓取的快取屬性，這些用戶端可能已針對指定的專案累積。<br /> | 
| <span id="SFGAO_REMOVABLE"></span><span id="sfgao_removable"></span><dl><dt><strong>SFGAO_REMOVABLE</strong></dt><dt>0x02000000</dt></dl> | 指定的專案位於卸載式媒體或本身為卸載式裝置。<br /> | 
| <span id="SFGAO_COMPRESSED"></span><span id="sfgao_compressed"></span><dl><dt><strong>SFGAO_COMPRESSED</strong></dt><dt>0x04000000</dt></dl> | 指定的專案會壓縮。<br /> | 
| <span id="SFGAO_BROWSABLE"></span><span id="sfgao_browsable"></span><dl><dt><strong>SFGAO_BROWSABLE</strong></dt><dt>0x08000000</dt></dl> | 指定的專案可以裝載在網頁瀏覽器或 Windows 檔案總管框架內。<br /> | 
| <span id="SFGAO_FILESYSANCESTOR"></span><span id="sfgao_filesysancestor"></span><dl><dt><strong>SFGAO_FILESYSANCESTOR</strong></dt><dt>0x10000000</dt></dl> | 指定的資料夾是檔系統資料夾，或包含至少一個子系 (子域、孫版或更新版本的) ，也就是檔案系統 (SFGAO_FILESYSTEM) 資料夾。<br /> | 
| <span id="SFGAO_FOLDER"></span><span id="sfgao_folder"></span><dl><dt><strong>SFGAO_FOLDER</strong></dt><dt>0x20000000</dt></dl> | 指定的專案是資料夾。 某些專案可以用 SFGAO_STREAM 和 SFGAO_FOLDER 標記，例如副檔名為 .zip 的壓縮檔案。 當測試同時為檔案和容器的專案時，某些應用程式可能會包含此旗標。<br /> | 
| <span id="SFGAO_FILESYSTEM"></span><span id="sfgao_filesystem"></span><dl><dt><strong>SFGAO_FILESYSTEM</strong></dt><dt>0x40000000</dt></dl> | 指定的資料夾或檔案是檔案系統的一部分 (也就是) 的檔案、目錄或根目錄。 專案的剖析名稱可以假設為有效的 Win32 檔案系統路徑。 這些路徑可以是以 UNC 或磁碟機號為基礎。<br /> | 
| <span id="SFGAO_STORAGECAPMASK"></span><span id="sfgao_storagecapmask"></span><dl><dt><strong>SFGAO_STORAGECAPMASK</strong></dt><dt>0x70C50008</dt></dl> | 此旗標是儲存功能屬性的遮罩： SFGAO_STORAGE、SFGAO_LINK、SFGAO_READONLY、SFGAO_STREAM、SFGAO_STORAGEANCESTOR、SFGAO_FILESYSANCESTOR、SFGAO_FOLDER 和 SFGAO_FILESYSTEM。 呼叫端通常不會使用此值。<br /> | 
| <span id="SFGAO_HASSUBFOLDER"></span><span id="sfgao_hassubfolder"></span><dl><dt><strong>SFGAO_HASSUBFOLDER</strong></dt><dt>0x80000000</dt></dl> | 指定的資料夾具有子資料夾。 SFGAO_HASSUBFOLDER 屬性只是諮詢，而且可能會由 Shell 資料夾執行所傳回，即使它們不包含子資料夾也一樣。 不過請注意，相反地，無法傳回 SFGAO_HASSUBFOLDER，會明確指出資料夾物件沒有子資料夾。<br /> 當需要很長的時間來判斷是否有任何子資料夾時，建議您傳回 SFGAO_HASSUBFOLDER。 例如，當資料夾位於網路磁碟機機上時，Shell 一律會傳回 SFGAO_HASSUBFOLDER。<br /> | 
| <span id="SFGAO_CONTENTSMASK"></span><span id="sfgao_contentsmask"></span><dl><dt><strong>SFGAO_CONTENTSMASK</strong></dt><dt>0x80000000</dt></dl> | 此旗標是 content 屬性的遮罩，目前只 SFGAO_HASSUBFOLDER。 呼叫端通常不會使用此值。<br /> | 
| <span id="SFGAO_PKEYSFGAOMASK"></span><span id="sfgao_pkeysfgaomask"></span><dl><dt><strong>SFGAO_PKEYSFGAOMASK</strong></dt><dt>0x81044000</dt></dl> | <a href="/windows/desktop/properties/props-system-sfgaoflags">PKEY_SFGAOFlags</a>屬性所使用的遮罩，可判斷被視為導致緩慢計算或缺少內容的屬性： SFGAO_ISSLOW、SFGAO_READONLY、SFGAO_HASSUBFOLDER 和 SFGAO_VALIDATE。 呼叫端通常不會使用此值。<br /> | 




## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Shobjidl.h。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl.h .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IShellFolder::GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof)
</dt> <dt>

[**IShellFolder：:P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname)
</dt> <dt>

[**IShellItemArray：： GetAttributes**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getattributes)
</dt> </dl>

 

 
