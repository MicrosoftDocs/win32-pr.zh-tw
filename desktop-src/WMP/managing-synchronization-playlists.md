---
title: 管理同步播放清單
description: 管理同步播放清單
ms.assetid: 5891ada0-37a6-4256-9885-8aa9dbe98b7c
keywords:
- Windows Media Player，可攜式裝置
- Windows Media Player 物件模型，可攜式裝置
- 物件模型，可攜式裝置
- Windows Media Player ActiveX 控制、可攜式裝置
- ActiveX 控制，可攜式裝置
- Windows Media PlayerMobile ActiveX control、可攜式裝置
- Windows Media Player行動裝置、可攜式裝置
- 可攜式裝置，管理同步播放清單
- 裝置同步處理，播放清單
- 同步處理裝置、播放清單
- Windows Media Player，同步播放清單
- Windows Media Player 物件模型，同步播放清單
- 物件模型，同步處理播放清單
- Windows Media Player行動裝置，同步播放清單
- Windows Media Player ActiveX 控制項、同步播放清單
- Windows Media Player行動 ActiveX 控制項、同步播放清單
- ActiveX 控制項，同步播放清單
- 播放清單，同步處理
- 中繼檔播放清單，同步處理
- Windows媒體中繼檔播放清單，同步處理
- 同步播放清單，管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10253d7f08c618d62079ccc1767fdaf85560861eae68d39cd897e7959eaffcad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996368"
---
# <a name="managing-synchronization-playlists"></a>管理同步播放清單

Windows Media Player 10 或更新版本會使用播放清單來同步處理數位媒體檔案與可攜式裝置。 本節說明如何使用同步播放清單。

本節中的範例程式碼會使用兩個 ListView 控制項來顯示資訊。 第一個 ListView 控制項 (IDC \_ PLVIEW) 會顯示 Windows Media Player 文件庫中所有的播放清單，並先顯示同步播放清單。 目前所選裝置的同步播放清單會以核取記號標示，並以同步處理優先權順序排序。 所有其他播放清單都未核取。 ListView 控制項已設定為單一選取專案。 ListView 控制項中的播放清單順序決定了其同步處理優先權。 個別播放清單的核取狀態會判斷它是否為目前所選裝置的同步播放清單。

第二個 ListView 控制項 (IDC \_ MEDIAVIEW) 會顯示所選播放清單中的媒體專案。 有兩個額外的資料行會顯示文字，指出數位媒體檔案是否複製到裝置，並在發生失敗時，是否因為數位媒體檔案無法容納而導致複製失敗。

下列範例程式碼顯示如何初始化 ListView 控制項：


```C++
STDMETHODIMP CSyncSettings::InitListView()
{
    m_hPlView = GetDlgItem(IDC_PLVIEW);
    m_hMediaView = GetDlgItem(IDC_MEDIAVIEW); 

    ATLASSERT(m_hPlView);
    ATLASSERT(m_hMediaView);

    // Sync playlist information.
    // Selection highlights all rows.
    // Show checkboxes.
    ListView_SetExtendedListViewStyleEx(m_hPlView, 0, LVS_EX_CHECKBOXES | LVS_EX_FULLROWSELECT);
   
    // Add headers.
    LVCOLUMN lvc;
    ZeroMemory(&lvc, sizeof(LVCOLUMN));
    lvc.mask = LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM; 
    lvc.iSubItem = 0;
    
    lvc.pszText = _T("Sync");
    lvc.cx = 40;
    ListView_InsertColumn(m_hPlView, lvc.iSubItem, &lvc);

    lvc.iSubItem++;
    lvc.pszText = _T("Playlist Name");
    lvc.cx = 300;
    ListView_InsertColumn(m_hPlView, lvc.iSubItem, &lvc); 

    // Media information.
    // Selection highlights all rows.
    ListView_SetExtendedListViewStyleEx(m_hMediaView, 0, LVS_EX_FULLROWSELECT);

    // Add headers
    ZeroMemory(&lvc, sizeof(LVCOLUMN));
    lvc.mask = LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM; 
    lvc.iSubItem = 0;
    
    lvc.pszText = _T("Media name");
    lvc.cx = 150;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);

    lvc.iSubItem++;
    lvc.pszText = _T("On Device");
    lvc.cx = 69;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);  

    lvc.iSubItem++;
    lvc.pszText = _T("Fit?");
    lvc.cx = 40;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);  
   
    return S_OK;
}
```



下列字串陣列包含範例中所使用之同步處理屬性的名稱：


```C++
static const TCHAR *g_szSyncAttributeNames[17] = {
        _T("Not used"), // Do not access this one.
        _T("Sync01"),
        _T("Sync02"),
        _T("Sync03"),
        _T("Sync04"),
        _T("Sync05"),
        _T("Sync06"),
        _T("Sync07"),
        _T("Sync08"),
        _T("Sync09"),
        _T("Sync10"),
        _T("Sync11"),
        _T("Sync12"),
        _T("Sync13"),
        _T("Sync14"),
        _T("Sync15"),
        _T("Sync16")};
```



下列成員變數包含包含 Windows Media Player 文件庫中所有播放清單的播放清單。 每個播放清單都會以媒體專案表示。


```C++
CComPtr<IWMPPlaylist> m_spPlaylist;
```



下列各節提供範例程式碼：

-   [列舉同步播放清單](enumerating-synchronization-playlists.md)
-   [依同步處理優先順序排序播放清單](sorting-playlists-by-synchronization-priority.md)
-   [列舉媒體專案](enumerating-the-media-items.md)
-   [判斷播放清單同步處理狀態](determining-playlist-synchronization-state.md)
-   [變更同步處理優先權](changing-synchronization-priority.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用可攜式裝置**](working-with-portable-devices.md)
</dt> </dl>

 

 




