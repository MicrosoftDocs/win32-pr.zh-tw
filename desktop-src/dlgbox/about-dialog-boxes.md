---
title: 關於對話方塊
description: 本主題討論如何使用對話方塊來建立應用程式的使用者介面。
ms.assetid: 51960c28-a178-4ad3-b45e-426fec42a945
keywords:
- 對話方塊，關於
- 對話方塊、使用時機
- 強制回應對話方塊
- 非強制回應對話方塊
- 對話方塊，強制回應
- 對話方塊、非模式
- 對話方塊、範本
- 對話方塊、擁有者視窗
- 對話方塊、訊息方塊
- 對話方塊程式
- 訊息方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dd78713c3b87e54e8a992ea9415577c522fc9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023856"
---
# <a name="about-dialog-boxes"></a>關於對話方塊

有許多功能、訊息和預先定義的控制項可協助您建立和管理對話方塊，因此可讓您更輕鬆地開發應用程式的使用者介面。 本總覽描述對話方塊函式和訊息，並說明如何使用它們來建立和使用對話方塊。

本總覽包含下列主題：

-   [使用對話方塊的時機](#when-to-use-a-dialog-box)
-   [對話方塊擁有者視窗](#dialog-box-owner-window)
-   [訊息方塊](#message-boxes)
-   [強制回應對話方塊](#modal-dialog-boxes)
-   [非強制回應對話方塊](#modeless-dialog-boxes)
-   [對話方塊範本](#dialog-box-templates)
    -   [對話方塊範本樣式](#dialog-box-template-styles)
    -   [對話方塊度量](#dialog-box-measurements)
    -   [對話方塊控制項](#dialog-box-controls)
    -   [對話方塊視窗功能表](#dialog-box-window-menu)
    -   [對話方塊字型](#dialog-box-fonts)
    -   [記憶體中的範本](#templates-in-memory)

如需通用對話方塊的詳細資訊，請參閱 [通用對話方塊程式庫](common-dialog-box-library.md)。

## <a name="when-to-use-a-dialog-box"></a>使用對話方塊的時機

大部分的應用程式會使用對話方塊來提示需要使用者輸入的功能表項目的其他資訊。 使用對話方塊是應用程式取得輸入的唯一建議方式。 例如，一般的 **開啟** 功能表項目需要開啟的檔案名，因此應用程式應該使用對話方塊來提示使用者輸入名稱。 在這種情況下，應用程式會在使用者按一下功能表項目時建立對話方塊，並在使用者提供資訊之後立即終結對話方塊。

當使用者在另一個視窗中工作時，許多應用程式也會使用對話方塊來顯示資訊或選項。 例如，文字處理應用程式通常會使用具有文字搜尋選項的對話方塊。 當應用程式搜尋文字時，對話方塊會留在螢幕上。 然後，使用者可以返回對話方塊，然後再次搜尋相同的單字;或者，使用者可以變更對話方塊中的專案，並搜尋新的單字。 以這種方式使用對話方塊的應用程式通常會在使用者按一下功能表項目時建立一個，並在應用程式執行時或使用者明確關閉對話方塊之前，繼續顯示該專案。

為了支援應用程式使用對話方塊的不同方式，有兩種類型的對話方塊：強制回應和非模式。 *強制回應對話方塊* 會要求使用者提供資訊或取消對話方塊，才能允許應用程式繼續進行。 應用程式會使用強制回應對話方塊搭配需要額外資訊的功能表項目，才能繼續進行。 非 *強制回應對話方塊* 可讓使用者提供資訊，並回到上一個工作，而不需要關閉對話方塊。 強制回應對話方塊比非強制回應對話方塊更容易管理，因為它們是建立的、執行其工作，並藉由呼叫單一函式終結。

若要建立強制回應或非強制回應對話方塊，應用程式必須提供對話方塊範本以描述對話方塊樣式和內容;應用程式也必須提供對話方塊程式來執行工作。 *對話方塊範本* 是對話方塊和它所包含之控制項的二進位描述。 開發人員可以建立此範本作為資源，以從應用程式的可執行檔載入，或在應用程式執行時在記憶體中建立。 *對話方塊* 程式是一種應用程式定義的回呼函式，當系統有輸入對話方塊或對話方塊的工作要執行時，系統就會呼叫這個函式。雖然對話方塊程式類似于視窗程式，但它並沒有相同的責任。

應用程式通常會使用 [**對話方塊**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) 或 [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) 函數來建立對話方塊。 **對話方塊** 會建立強制回應對話方塊; **CreateDialog** 會建立非強制回應對話方塊。 這兩個函式會從應用程式的可執行檔中載入對話方塊範本，並建立符合範本規格的快顯視窗。 另外還有其他函式會使用記憶體中的範本來建立對話方塊;他們會在對話方塊建立時，將其他資訊傳遞給對話方塊程式。

對話方塊通常屬於預先定義、專屬的視窗類別。 系統會針對強制回應和非強制回應對話方塊使用此視窗類別和其對應的視窗程式。 呼叫函式時，它會建立對話方塊的視窗，以及對話方塊中控制項的視窗，然後將選取的訊息傳送至對話方塊程式。 當對話方塊顯示時，預先定義的視窗程式會管理所有訊息、處理一些訊息，並將其他訊息傳遞至對話方塊程式，讓程式可以執行工作。 應用程式無法直接存取預先定義的視窗類別或視窗程式，但是可以使用對話方塊範本和對話方塊程式來修改對話方塊的樣式和行為。

## <a name="dialog-box-owner-window"></a>對話方塊擁有者視窗

大部分的對話方塊都有擁有者視窗 (或更簡單的) 擁有者。 建立對話方塊時，應用程式會藉由指定擁有者的視窗控制碼來設定擁有者。 系統會使用擁有者來判斷對話方塊在 Z 順序中的位置，讓對話方塊永遠定位於其擁有者的上方。 此外，系統也可以將訊息傳送至擁有者的視窗程式，在對話方塊中通知事件。

只要隱藏或終結其擁有者，系統就會自動隱藏或終結對話方塊。 這表示對話方塊程式不需要任何特殊的處理，就能偵測擁有者視窗的狀態變更。

由於一般對話方塊會與功能表項目一起使用，因此擁有者視窗通常是包含功能表的視窗。 雖然可以建立沒有擁有者的對話方塊，但不建議您這樣做。 例如，當強制回應對話方塊沒有擁有者時，系統不會停用任何應用程式的其他視窗，而且可讓使用者繼續在其他視窗中執行工作，失去強制回應對話方塊的用途。

當非強制回應對話方塊沒有擁有者時，系統不會在應用程式中的其他視窗隱藏或損毀時隱藏或終結對話方塊。 雖然這不會破壞非強制回應對話方塊的用途，但應用程式需要執行特殊處理，以確保對話方塊在適當的時間隱藏並終結。

## <a name="message-boxes"></a>訊息方塊

訊息方塊是一個特殊對話方塊，可讓應用程式用來顯示訊息並提示輸入簡單的輸入。 訊息方塊通常包含文字訊息和一或多個按鈕。 應用程式會使用 [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) 或 [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) 函式來建立訊息方塊，並指定要顯示的文字和按鈕的數目和類型。 請注意， **MessageBox** 和 **MessageBoxEx** 的運作方式目前沒有任何差異。

雖然訊息方塊是對話方塊，但系統會完全掌控訊息方塊的建立和管理。 這表示應用程式不會提供對話方塊範本和對話方塊程式。 系統會根據針對訊息方塊所指定的文字和按鈕來建立自己的範本，並提供自己的對話方塊程式。

訊息方塊是強制回應對話方塊，系統會使用 [**對話方塊**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) 所使用的相同內建函式來建立它。 如果應用程式在呼叫 [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) 或 [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa)時指定擁有者視窗，系統會停用擁有者。 應用程式也可以指示系統停用所有屬於目前線程的最上層視窗，方法是在建立對話方塊時指定 **MB \_ TASKMODAL** 值。

系統可以將訊息傳送給擁有者，例如 [**wm \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) 和 [**wm \_ 啟用**](/windows/desktop/winmsg/wm-enable)，就像在建立強制回應對話方塊時一樣。 擁有者視窗應該執行這些訊息所要求的任何動作。

## <a name="modal-dialog-boxes"></a>強制回應對話方塊

強制回應對話方塊應該是具有視窗功能表、標題列和粗框線的快顯視窗。也就是說，對話方塊範本應該指定 **ws \_ 快顯視窗**、 **ws \_ SYSMENU**、 **ws \_ 標題** 和 **DS \_ MODALFRAME** 樣式。 雖然應用程式可以指定 **ws \_ 可見** 樣式，但是無論對話方塊範本是否指定 **ws \_ 可見** 樣式，系統一律會顯示模式對話方塊。 應用程式不能建立具有 **WS \_ 子** 樣式的強制回應對話方塊。 具有此樣式的強制回應對話方塊會自行停用，防止任何後續的輸入到達應用程式。

應用程式會使用 [**對話方塊**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) 或 [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) 函數來建立強制回應對話方塊。 **對話方塊** 需要包含對話方塊範本之資源的名稱或識別碼; **DialogBoxIndirect** 需要包含對話方塊範本的記憶體物件控制碼。 [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)和 [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)函數也會建立強制回應對話方塊;它們與先前所述的函式相同，但在建立對話方塊時，會將指定的參數傳遞至對話方塊程式。

建立強制回應對話方塊時，系統會讓它成為使用中視窗。 此對話方塊會保持作用中，直到對話方塊程式呼叫 [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) 函式，或系統在另一個應用程式中啟用視窗為止。 使用者和應用程式都不能讓擁有者視窗變成作用中，直到強制回應對話方塊終結為止。

當擁有者視窗尚未停用時，系統會在建立強制回應對話方塊時，自動停用視窗和任何屬於該視窗的子視窗。 擁有者視窗會保持停用，直到對話方塊損毀為止。 雖然對話方塊程式可能會隨時啟用 [擁有者] 視窗，但讓擁有者無法通過模式對話方塊的目的，也不建議使用。 當對話方塊程式損毀時，系統會再次啟用 [擁有者] 視窗，但只有在強制回應對話方塊造成停用擁有者時才會這樣做。

當系統建立強制回應對話方塊時，它會將 [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) 訊息傳送到視窗 (如果有任何) 正在捕捉滑鼠輸入。 接收此訊息的應用程式應該放開滑鼠捕捉，讓使用者可以將滑鼠移至強制回應對話方塊。 由於系統會停用擁有者視窗，如果擁有者無法在收到此訊息時放開滑鼠，則所有的滑鼠輸入都會遺失。

為了處理強制回應對話方塊的訊息，系統會啟動自己的訊息迴圈，並暫時控制整個應用程式的訊息佇列。 當系統抓取未針對此對話方塊明確的訊息時，它會將訊息分派至適當的視窗。 如果它抓取了 [**WM \_**](/windows/desktop/winmsg/wm-quit) 結束訊息，它會將訊息張貼回應用程式訊息佇列，讓應用程式的主要訊息迴圈最後可以取得訊息。

只要應用程式訊息佇列是空的，系統就會將 [**WM \_ ENTERIDLE**](wm-enteridle.md) 訊息傳送給擁有者視窗。 應用程式可以使用此訊息來執行背景工作，而對話方塊則會留在螢幕上。 當應用程式以這種方式使用訊息時，應用程式必須經常產生控制 (例如，使用 [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) 函數) ，讓強制回應對話方塊可以接收任何使用者輸入。 為了防止強制回應對話方塊傳送 **WM \_ ENTERIDLE** 訊息，應用程式可以在 \_ 建立對話方塊時指定 DS NOIDLEMSG 樣式。

應用程式會使用 [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) 函數來終結強制回應對話方塊。 在大多數情況下，當使用者從對話方塊的 [視窗] 功能表按一下 [**關閉**]，或按一下對話方塊中的 [**確定]** 或 [**取消**] 按鈕時，對話方塊程式就會呼叫 **EndDialog** 。 此對話方塊可以透過 [**對話方塊**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) 函數 (或其他) 建立函式傳回值，方法是在呼叫 **EndDialog** 函數時指定值。 終結對話方塊之後，系統會傳回這個值。 大部分的應用程式會使用這個傳回值來判斷對話方塊是否已順利完成其工作，或使用者已取消。 系統不會從建立對話方塊的函數傳回控制權，直到對話方塊程式呼叫 **EndDialog** 函式為止。

## <a name="modeless-dialog-boxes"></a>非強制回應對話方塊

非強制回應對話方塊應該是具有視窗功能表、標題列和細框線的快顯視窗。也就是說，對話方塊範本應該指定 **ws \_ 快顯視窗**、 **ws \_ 標題**、 **ws \_ 框線** 和 **ws \_ SYSMENU** 樣式。 除非範本指定 **WS \_ 可見** 樣式，否則系統不會自動顯示對話方塊。

應用程式會使用 [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) 或 [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta) 函數來建立非強制回應對話方塊。 **CreateDialog** 需要包含對話方塊範本之資源的名稱或識別碼; **CreateDialogIndirect** 需要包含對話方塊範本的記憶體物件控制碼。 另外兩個函式 [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama) 和 [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)，也建立非強制回應對話方塊;當建立對話方塊時，它們會將指定的參數傳遞至對話方塊程式。

[**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) 和其他建立函數會傳回視窗控制碼給對話方塊。 應用程式和對話方塊程式可以使用此控制碼來管理對話方塊。 例如，如果對話方塊範本中未指定 [ **WS \_ VISIBLE** ]，則應用程式可以將視窗控制碼傳遞至 [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) 函式來顯示對話方塊。

非強制回應對話方塊不會停用擁有者視窗，也不會將訊息傳送給它。 建立對話方塊時，系統會將它變成使用中視窗，但是使用者或應用程式可以隨時變更使用中視窗。 如果對話方塊變成非使用中，即使擁有者視窗為使用中，它仍會以 Z 順序維持在 [擁有者] 視窗的上方。

應用程式會負責將輸入訊息取出並分派至對話方塊。 大部分的應用程式會使用主要訊息迴圈。 不過，若要允許使用者使用鍵盤移至並選取控制項，應用程式必須呼叫 [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) 函數。 如需此函數的詳細資訊，請參閱 [對話方塊鍵盤介面](dlgbox-programming-considerations.md)。

非強制回應對話方塊不能將值當作強制回應對話方塊傳回給應用程式，但是對話方塊程式可以使用 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 函數，將資訊傳送至主控視窗。

應用程式必須在結束之前終結所有非強制回應對話方塊。 它可以使用 [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) 函數來終結非強制回應對話方塊。 在大多數情況下，對話方塊程式都會呼叫 **DestroyWindow** 來回應使用者輸入，例如按一下 [ **取消** ] 按鈕。 如果使用者永遠不會以這種方式關閉對話方塊，則應用程式必須呼叫 **DestroyWindow**。

[**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) 會讓對話方塊的視窗控制碼失效，因此任何後續呼叫使用控制碼的函式都會傳回錯誤值。 若要避免錯誤，對話方塊程式應通知擁有者已終結對話方塊。 許多應用程式會維護包含對話方塊控制碼的全域變數。 當對話方塊程式終結對話方塊時，它也會將全域變數設定為 **Null**，表示對話方塊已不再有效。

對話方塊程式不能呼叫 [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) 函數來終結非強制回應對話方塊。

## <a name="dialog-box-templates"></a>對話方塊範本

對話方塊範本是描述對話方塊、定義其高度、寬度、樣式，以及它所包含之控制項的二進位資料。 若要建立對話方塊，系統會從應用程式的可執行檔中的資源載入對話方塊範本，或使用應用程式在全域記憶體中傳遞給它的範本。 無論是哪一種情況，應用程式都必須在建立對話方塊時提供範本。

開發人員會使用資源編譯器或對話方塊編輯器來建立範本資源。 資源編譯器會將文字描述轉換成二進位資源，而對話方塊編輯器會將以互動方式建立的對話方塊儲存為二進位資源。

> [!Note]  
> 有關如何建立範本資源並將其新增至應用程式可執行檔的說明，已超出此總覽的範圍。 如需建立範本資源並將其新增至可執行檔的詳細資訊，請參閱應用程式開發工具所提供的檔。

 

若要建立不使用範本資源的對話方塊，您必須在記憶體中建立範本，並將它傳遞至 [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama) 或 [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama) 函式，或傳遞至 [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta) 或 [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) 宏。

記憶體中的對話方塊範本是由描述對話方塊的標頭所組成，後面接著一個或多個其他區塊的資料，以描述對話方塊中的每個控制項。 範本可以使用標準格式或延伸格式。 在標準範本中，標頭是 [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) 結構，後面接著額外的可變長度陣列;每個控制項的資料都包含 [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) 結構，後面接著額外的可變長度陣列。 在擴充的對話方塊範本中，標頭會使用 [**DLGTEMPLATEEX**](dlgtemplateex.md) 格式，而控制項定義會使用 [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) 格式。

您可以建立記憶體範本，方法是配置全域記憶體物件，並將它填入標準或擴充的標頭和控制項定義。 範本資源的表單和內容中的記憶體範本完全相同。 許多使用記憶體範本的應用程式會先使用 [**LoadResource**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource) 函式將範本資源載入至記憶體中，然後修改載入的資源以建立新的記憶體範本。 如需有關在記憶體中建立對話方塊範本的詳細資訊，請參閱 [記憶體中的範本](#templates-in-memory)。

下列各節描述對話方塊範本中使用的樣式、測量和其他值。

-   [對話方塊範本樣式](#dialog-box-template-styles)
-   [對話方塊度量](#dialog-box-measurements)
-   [對話方塊控制項](#dialog-box-controls)
-   [對話方塊視窗功能表](#dialog-box-window-menu)
-   [對話方塊字型](#dialog-box-fonts)
-   [記憶體中的範本](#templates-in-memory)

### <a name="dialog-box-template-styles"></a>對話方塊範本樣式

每個對話方塊範本都會指定樣式值的組合，以定義對話方塊的外觀和功能。 樣式值可以是視窗樣式，例如 **WS \_ POPUP** 和 **ws \_ SYSMENU**，以及對話方塊樣式，例如 **DS \_ MODALFRAME**。 範本的樣式數目和類型取決於對話方塊的類型和用途。 如需值清單，請參閱 [**對話方塊樣式**](dialog-box-styles.md)。

當您建立對話方塊時，系統會將範本中指定的所有視窗樣式傳遞給 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式。 系統可能會根據指定的對話方塊樣式，傳遞一或多個擴充樣式。 例如，當範本指定 **DS \_ MODALFRAME** 時，系統會在建立對話方塊時使用 **WS \_ EX \_ DLGMODALFRAME** 。

大部分的對話方塊都是具有視窗功能表和標題列的快顯視窗。 因此，一般範本會指定 **ws \_ POPUP**、 **ws \_ SYSMENU** 和 **ws \_ 標題** 樣式。 此範本也會指定框線樣式：非強制回應對話方塊的 **WS \_ 框線** ，以及用於強制回應對話方塊的 **DS \_ MODALFRAME** 。 範本可以指定快顯 (的視窗類型，例如 WS 重迭) **\_** （如果它建立自訂的視窗，而不是對話方塊）。

無論是否指定了 **WS \_ VISIBLE** 樣式，系統一律會顯示模式對話方塊。 當非強制回應對話方塊的範本指定 **WS \_ 可見** 樣式時，系統會在建立時自動顯示對話方塊。 否則，應用程式會負責使用 [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) 函數來顯示對話方塊。

### <a name="dialog-box-measurements"></a>對話方塊度量

每個對話方塊範本都包含指定對話方塊位置、寬度和高度的度量，以及它所包含之控制項的位置、寬度和高度。 這些測量與裝置無關，因此應用程式可以使用單一範本，為所有類型的顯示裝置建立相同的對話方塊。 這可確保在畫面之間有不同解析度和外觀比例的所有螢幕上，對話方塊的比例和外觀也相同。

對話方塊範本中的度量是在對話方塊範本單位中指定。 若要將度量從對話方塊範本單位轉換為螢幕單位 (圖元) ，請使用 [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) 函式，此函式會將對話方塊所使用的字型納入考慮，並將矩形從對話方塊範本單位正確轉換成圖元。 針對使用系統字型的對話方塊，您可以使用 [**GetDialogBaseUnits**](/windows/desktop/api/Winuser/nf-winuser-getdialogbaseunits) 函式來自行執行轉換計算，雖然使用 **MapDialogRect** 比較簡單。

範本必須指定對話方塊左上角的初始座標。 座標通常是相對於擁有者視窗工作區的左上角。 當範本指定 DS \_ ABSALIGN 樣式，或對話方塊沒有擁有者時，此位置會相對於畫面的左上角。 系統會在建立對話方塊時設定此初始位置，但允許應用程式在顯示對話方塊之前，調整位置。 例如，應用程式可以取出擁有者視窗的維度、計算在主控視窗中將對話方塊置中的新位置，然後使用 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) 函數來設定位置。

範本應該指定不超過畫面寬度和高度的對話方塊寬度和高度，並確保所有控制項都在對話方塊的工作區中。 雖然系統允許對話方塊的大小不限，但建立太小或太大的對話方塊可能會使使用者無法提供輸入，失去對話方塊的用途。 許多應用程式在有大量的控制項時，會使用多個對話方塊。 在這種情況下，初始對話方塊通常會包含一或多個按鈕，讓使用者可以選擇顯示下一個對話方塊。

### <a name="dialog-box-controls"></a>對話方塊控制項

此範本會針對對話方塊中的每個控制項，指定位置、寬度、高度、樣式、識別碼和視窗類別。 系統會將此資料傳遞至 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式，以建立每個控制項。 系統會依照在範本中指定的順序來建立控制項。 範本應該指定適當的數目、類型和控制項順序，以確保使用者可以輸入完成與對話方塊相關聯之工作所需的輸入。

針對每個控制項，範本會指定定義控制面板和操作的樣式值。 每個控制項都是子視窗，因此必須具有 **WS \_ 子** 樣式。 為了確保在對話方塊顯示時可以看到控制項，每個控制項也都必須有 **WS \_ 可見** 的樣式。 其他常用的視窗樣式為具有選用框線的控制項的 **ws \_ 框線** 、 **已 \_ 停用** 的控制項（在對話方塊一開始建立時應停用），以及可使用鍵盤存取之控制項的 **ws \_ TABSTOP** 和 **ws \_ 群組** 。 **Ws \_ TABSTOP** 和 **ws \_ GROUP** 樣式會與本主題稍後所述的對話方塊鍵盤介面一起使用。

此範本也可以指定控制項視窗類別特定的控制項樣式。 例如，指定按鈕控制項的範本必須提供按鈕控制項樣式，例如 **BS \_** 按鈕或 [ **BS \_ ] 核取方塊**。 系統會透過 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create) 訊息，將控制項樣式傳遞給控制視窗程式，讓程式能夠調整控制項的外觀和操作。

系統會將位置座標和寬度和高度度量從對話方塊基底單位轉換成圖元，然後再將它們傳遞給 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)。 當系統建立控制項時，它會將對話方塊指定為父視窗。 這表示系統一律會將控制項的位置座標視為用戶端座標（相對於對話方塊的工作區左上角）。

範本會指定每個控制項的視窗類別。 一般的對話方塊包含屬於預先定義之控制項視窗類別的控制項，例如按鈕和編輯控制項視窗類別。 在此情況下，範本會藉由提供類別的對應預先定義 atom 值，來指定視窗類別。 當對話方塊包含屬於自訂控制項視窗類別的控制項時，此範本會提供該已註冊視窗類別的名稱，或目前與該名稱相關聯的 atom 值。

對話方塊中的每個控制項都必須有唯一的識別碼，才能與其他控制項區別。 控制項會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息，將資訊傳送至對話方塊程式，因此，程式必須有控制項識別碼，才能判斷哪個控制項傳送了指定的訊息。 此規則的唯一例外狀況是靜態控制項的控制項識別碼。 靜態控制項不需要唯一的識別碼，因為它們不會傳送任何 **WM \_ 命令** 訊息。

若要允許使用者關閉對話方塊，範本至少應指定一個 push 按鈕，並為其提供控制項識別碼 **IDCANCEL**。 若要允許使用者在完成或取消與對話方塊相關聯的工作之間進行選擇，範本應該分別指定兩個按下的 **[確定] 和 [** **取消**] 按鈕，分別具有 **IDOK** 和 **IDCANCEL** 的控制項識別碼。

範本也會指定控制項的選擇性文字和建立資料。 文字通常會提供按鈕控制項的標籤，或指定靜態文字控制項的初始內容。 建立資料是一個或多個位元組的資料，系統會在建立控制項時，將該資料傳遞給控制項視窗程式。 如果控制項需要的初始內容或樣式的詳細資訊比其他資料所指定的更多，則建立資料非常有用。 例如，應用程式可以使用建立資料來設定捲軸控制項的初始設定和範圍。

### <a name="dialog-box-window-menu"></a>對話方塊視窗功能表

當範本指定 **WS \_ SYSMENU** 樣式時，系統會在視窗功能表中提供一個對話方塊。 為了避免不適當的輸入，系統會自動停用功能表中的所有專案，但 **Move** 和 **Close** 除外。 使用者可以按一下 [ **移動** ] 來移動對話方塊。 當使用者按一下 [ **關閉**] 時，系統會將 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息傳送至對話方塊程式，並將 *wParam* 參數設定為 **IDCANCEL**。 這等同于使用者按一下 [ **取消** ] 按鈕時所傳送的訊息。 此訊息的建議動作是關閉對話方塊，並取消要求的工作。

雖然不建議對話方塊中的其他功能表，但是對話方塊範本可以藉由提供功能表資源的識別碼或名稱來指定功能表。 在此情況下，系統會載入資源並建立對話方塊的功能表。 使用範本來建立自訂視窗而非對話方塊時，應用程式通常會在範本中使用功能表識別碼或名稱。

### <a name="dialog-box-fonts"></a>對話方塊字型

系統會使用對話方塊字型的平均字元寬度來計算對話方塊的位置和維度。 根據預設，系統會使用 **系統 \_ 字型** 字型來繪製對話方塊中的所有文字。

若要針對預設值以外的對話方塊指定字型，您必須使用對話方塊範本建立對話方塊。 在範本資源中，使用 [FONT 語句](../menurc/font-statement.md)。 在對話方塊範本中，設定 **ds \_ SETFONT** 或 **ds \_ SHELLFONT** 樣式，並指定點大小和字樣名稱。 即使對話方塊範本以這種方式指定字型，系統一律會使用對話方塊標題和對話方塊功能表的系統字型。

當對話方塊具有 **ds \_ SETFONT** 或 **ds \_ SHELLFONT** 樣式時，系統會將 [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) 訊息傳送至對話方塊程式，並在建立控制項時將其傳送至每個控制項。 對話方塊程式會負責儲存以 **WM \_ SETFONT** 訊息傳遞的字型控制碼，並在每次將文字寫入視窗時，選取顯示裝置內容的控點。 預先定義的控制項預設會這樣做。

不同版本的 Windows 可能會有不同的系統字型。 若要讓您的應用程式使用系統字型（不論其執行所在的系統），請使用 **DS \_ SHELLFONT** 搭配字型 MS Shell Dlg，並使用 [DIALOGEX 資源](../menurc/dialogex-resource.md) ，而不是 [對話方塊資源](../menurc/dialog-resource.md)。 系統會對應此字樣，讓您的對話方塊使用 Tahoma 字型。 請注意，如果字樣不是 MS Shell Dlg， **DS \_ SHELLFONT** 不會有任何作用。

### <a name="templates-in-memory"></a>記憶體中的範本

記憶體中的對話方塊範本是由描述對話方塊的標頭所組成，後面接著一個或多個其他區塊的資料，以描述對話方塊中的每個控制項。 範本可以使用標準格式或延伸格式。 在標準範本中，標頭是 [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) 結構，後面接著額外的可變長度陣列。 每個控制項的資料包含 [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) 結構，後面接著額外的可變長度陣列。 在擴充的對話方塊範本中，標頭會使用 [**DLGTEMPLATEEX**](dlgtemplateex.md) 格式，而控制項定義會使用 [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) 格式。

若要區分標準範本和延伸範本，請檢查對話方塊範本的前16位。 在擴充的範本中，第一個 **單字** 是 0xffff;任何其他值則表示標準範本。

如果您在記憶體中建立對話方塊範本，您必須確定每個 [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) 或 [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) 控制項定義都在 **DWORD** 界限上對齊。 此外，任何遵循控制項定義的建立資料都必須對齊 **DWORD** 界限。 對話方塊範本中的所有其他可變長度陣列都必須對齊 **字** 邊界。

### <a name="template-header"></a>範本標頭

在對話方塊的標準和延伸範本中，標頭包含下列一般資訊：

-   對話方塊的位置和維度
-   對話方塊的視窗和對話方塊樣式
-   對話方塊中的控制項數目。 此值會決定範本中的 [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) 或 [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) 控制項定義數目。
-   對話方塊的選擇性功能表資源。 範本可能會指出對話方塊沒有功能表，或者可以指定序數值或以 null 終止的 Unicode 字串，以識別可執行檔中的功能表資源。
-   對話方塊的視窗類別。 這可以是預先定義的對話方塊類別，或是識別已註冊視窗類別的序數值或以 null 終止的 Unicode 字串。
-   以 null 結束的 Unicode 字串，指定對話方塊視窗的標題。 如果字串是空的，則對話方塊的標題列是空白的。 如果對話方塊沒有 **WS \_ 標題** 樣式，系統會將標題設定為指定的字串，但不會顯示它。
-   如果對話方塊具有 **DS \_ SETFONT** 樣式，則標頭會指定字型的點大小和字樣名稱，以用於工作區中的文字以及對話方塊的控制項。

在擴充的範本中， [**DLGTEMPLATEEX**](dlgtemplateex.md) 標頭也會指定下列其他資訊：

-   當系統傳送 [**WM \_**](../shell/wm-help.md) 說明訊息時，對話方塊視窗的說明內容識別碼。
-   如果對話方塊具有 **ds \_ SETFONT** 或 **ds \_ SHELLFONT** 樣式，則標頭會指定字型粗細，並指出字型是否為斜體。

### <a name="control-definitions"></a>控制項定義

在範本標頭之後，會有一或多個控制項定義描述對話方塊的控制項。 在標準和延伸範本中，對話方塊標頭都有一個成員，指出範本中的控制項定義數目。 在標準範本中，每個控制項定義都包含一個 [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) 結構，後面接著額外的可變長度陣列。 在擴充的範本中，控制項定義會使用 [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) 格式。

在標準和延伸範本中，控制項定義包含下列資訊：

-   控制項的位置和維度。
-   控制項的視窗和控制項樣式。
-   控制項識別碼。
-   控制項的視窗類別。 這可以是預先定義之系統類別的序數值，或是指定已註冊視窗類別名稱的以 null 結束的 Unicode 字串。
-   以 null 結束的 Unicode 字串，這個字串會指定控制項的初始文字，或是在可執行檔中識別資源的序數值（例如圖示）。
-   選用的可變長度區塊建立資料。 當系統建立控制項時，它會在傳送至控制項之 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create)訊息的 *lParam* 參數中，傳遞此資料的指標。

在擴充的範本中，當系統傳送 [**WM \_**](../shell/wm-help.md) 說明訊息時，控制項定義也會指定控制項的說明內容識別碼。

 

 