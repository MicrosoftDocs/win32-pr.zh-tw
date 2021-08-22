---
description: 當使用者以滑鼠右鍵按一下 Shell 物件時，顯示的快捷方式功能表通常會包含屬性專案。
title: 屬性工作表處理常式
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 72233ab5-212d-498c-8df1-1a96c8eda892
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 27327db4718430ba646d9566227116e304d4d5f5770d0119987b32e0cd2adce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719540"
---
# <a name="property-sheet-handlers"></a>屬性工作表處理常式

當使用者以滑鼠右鍵按一下 Shell 物件時，顯示的快捷方式功能表通常會包含 **屬性** 專案。 選取該專案會啟動屬性工作表，讓使用者能夠在某些情況下，修改物件的屬性。 您可以藉由執行和註冊 *屬性工作表處理常式* 來自訂此屬性工作表。

[建立 shell](handlers.md)擴充處理常式時，會討論如何執行和註冊 shell 擴充處理常式的一般程式。 本檔著重于屬性工作表處理常式特定的執行層面。

-   [屬性工作表處理常式的運作方式](#how-property-sheet-handlers-work)
-   [註冊和執行已載入之磁片磁碟機的屬性工作表處理常式](#registering-and-implementing-a-property-sheet-handler-for-a-mounted-drive)
-   [相關主題](#related-topics)

## <a name="how-property-sheet-handlers-work"></a>屬性工作表處理常式的運作方式

下圖顯示 Windows XP 文字檔的屬性工作表。

![屬性工作表](images/propsheethandler1.jpg)

下圖顯示針對任何檔案顯示的 [預設屬性] 屬性工作表。 針對許多這類屬性工作表，您可以藉由執行和註冊屬性工作表處理常式，將一或多個頁面加入至屬性工作表。

屬性工作表處理常式最常針對 [檔案類型](fa-file-types.md)進行註冊。 每個處理常式都可以將一個自訂頁面加入至類別的 [屬性] 屬性工作表。 這些頁面通常會讓使用者存取特定檔案類型的特定屬性。 例如，包含文字檔的檔案類型可以顯示列出標題和作者的頁面，以及檔的摘要。 這種屬性工作表處理常式類型的特殊案例，是用來將頁面新增至載入之磁片磁碟機的 [屬性] 屬性工作表。

屬性工作表處理常式的另一個用法是取代主控台應用程式所顯示之屬性工作表中的頁面。 比方說，滑鼠製造商可以使用屬性工作表處理常式來取代主控台的 **滑鼠屬性**] 屬性頁上的 [**按鈕**] 頁面，以及針對其滑鼠特性自訂的頁面。

就像所有 Shell 擴充處理常式一樣，屬性工作表處理常式也是實作為 Dll (COM) 物件的同進程元件物件模型。 除了 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)： [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) 和 [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)之外，它們還必須匯出兩個介面。

Shell 會使用 [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) 介面來初始化處理常式。 當 Shell 呼叫 [**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)時，它會傳入具有物件名稱的資料物件，而專案識別碼清單的指標 (PIDL 包含該檔案之資料夾的) 。 *HRegKey* 參數未與屬性工作表處理常式一起使用。 **IShellExtInit：： Initialize** 方法必須從資料物件中解壓縮檔案名稱，並儲存名稱和資料夾的 PIDL，以供稍後使用。 For further details, see the *Implementing IShellExtInit* section of [Creating Shell Extension Handlers](handlers.md).

作業的其餘部分會透過處理常式的 [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) 介面進行。 如果屬性工作表與檔案類型相關聯，則 Shell 會呼叫 [**IShellPropSheetExt：： AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) ，以允許處理常式將頁面加入至屬性工作表。 如果屬性工作表與主控台的應用程式相關聯，則 Shell 會呼叫 [**IShellPropSheetExt：： ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) ，以允許處理常式取代頁面。

## <a name="registering-and-implementing-a-property-sheet-handler-for-a-mounted-drive"></a>註冊和執行已載入之磁片磁碟機的屬性工作表處理常式

每個掛接的磁片磁碟機都有一個可由使用者顯示的屬性工作表。 下圖顯示 CD-ROM 光碟機的屬性工作表。

![cd-rom 屬性工作表](images/propsheethandler2.jpg)

有各式各樣的裝置可掛接為磁片磁碟機。 由於預設的屬性工作表（專為磁片磁碟機設計）可能無法滿足某些裝置的需求，因此可以實行屬性工作表處理常式來新增所掛接裝置的特定頁面。 這種類型的屬性工作表處理常式的基本執行 [方式與如何針對檔案類型註冊和執行屬性工作表處理常式](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)中所討論的一樣，有兩個例外狀況。

-   傳遞給處理常式之 [**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) 方法的資料物件可能包含 [CFSTR \_ MOUNTEDVOLUME](clipboard.md) 格式的磁片磁碟機路徑，而不是 [CF \_ HDROP](clipboard.md) 格式。 \_當裝置掛接到磁碟機號時，會使用 CF HDROP 格式。 \_當遠端裝置掛接到資料夾而非磁碟機號時，CFSTR MOUNTEDVOLUME 格式會與 NTFS 檔案系統搭配使用。
-   處理常式的 GUID 會在 **HKEY 類別的 \_ \_ 根** \\ **磁片磁碟機** \\ **shellex** \\ **PropertySheetHandlers** 金鑰下註冊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何註冊及執行檔案類型的屬性工作表處理常式](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)
</dt> <dt>

[如何註冊和執行主控台應用程式的屬性工作表處理常式](how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application.md)
</dt> </dl>

 

 
