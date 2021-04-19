---
description: 每個視窗都是特定視窗類別的成員。 視窗類別會決定個別視窗用來處理其訊息的預設視窗程式。
ms.assetid: 3a8e8f4e-910d-4863-a4a7-dd37c2dfa402
title: 關於視窗程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f63586b9ca4ac6fe8486ba112316174533b44e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997988"
---
# <a name="about-window-procedures"></a>關於視窗程式

每個視窗都是特定視窗類別的成員。 視窗類別會決定個別視窗用來處理其訊息的預設視窗程式。 所有屬於相同類別的 windows 都使用相同的預設視窗程式。 例如，系統會定義下拉式方塊類別 (**COMBOBOX**) 的視窗程式。然後，所有下拉式方塊都會使用該視窗程式。

應用程式通常會註冊至少一個新視窗類別和其相關聯的視窗程式。 註冊類別之後，應用程式就可以建立該類別的許多視窗，全都使用相同的視窗程式。 因為這表示多個來源可以同時呼叫相同的程式碼，所以從視窗程式修改共用資源時，您必須特別小心。 如需詳細資訊，請參閱 [視窗類別](window-classes.md)。

對話方塊的視窗程式 (呼叫的對話方塊程式) 具有與一般視窗程式類似的結構和功能。 本章節中參考視窗程式的所有點也適用于對話方塊程式。 如需詳細資訊，請參閱 [對話方塊](/windows/desktop/dlgbox/dialog-boxes)。

本節將討論下列主題。

-   [視窗程式的結構](#structure-of-a-window-procedure)
-   [預設視窗程式](#default-window-procedure)
-   [視窗程式子類別化](#window-procedure-subclassing)
    -   [實例子類別化](#instance-subclassing)
    -   [全域子類別](#global-subclassing)
-   [視窗程式 Superclassing](#window-procedure-superclassing)

## <a name="structure-of-a-window-procedure"></a>視窗程式的結構

視窗程式是具有四個參數並傳回帶正負號值的函式。 這些參數是由視窗控制碼、 **UINT** 訊息識別碼，以及使用 **WPARAM** 和 **LPARAM** 資料類型宣告的兩個訊息參數所組成。 如需詳細資訊，請參閱 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))。

訊息參數通常會包含其低序位和高序位字組中的資訊。 有幾個宏可供應用程式用來從訊息參數解壓縮資訊。 例如， [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 宏會將低序位字組從 message 參數解壓縮 (位0到 15) 。 其他宏包括 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))、 [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85))和 [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85))。

傳回值的解釋取決於特定的訊息。 請參閱每個訊息的描述，以判斷適當的傳回值。

因為可能會以遞迴方式呼叫視窗程式，所以請務必將它所使用的區域變數數目降到最低。 處理個別訊息時，應用程式應該呼叫視窗程式之外的函式，以避免過度使用本機變數，可能會導致堆疊在深度遞迴期間溢位。

## <a name="default-window-procedure"></a>預設視窗程式

預設的視窗程式函式 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 會定義所有視窗共用的某些基本行為。 預設視窗程式會為視窗提供最基本的功能。 應用程式定義的視窗程式應該將它未處理的任何訊息傳遞至 **DefWindowProc** 函式，以進行預設處理。

## <a name="window-procedure-subclassing"></a>視窗程式子類別化

當應用程式建立視窗時，系統會配置記憶體區塊來儲存視窗的特定資訊，包括處理視窗訊息的視窗程式位址。 當系統需要將訊息傳遞至視窗時，會在視窗特定的資訊中搜尋視窗程式的位址，並將訊息傳遞至該程式。

子類別 *化是一* 種技術，可讓應用程式在視窗有機會處理訊息之前，攔截和處理傳送或張貼至特定視窗的訊息。 藉由子類別化視窗，應用程式可以增強、修改或監看視窗的行為。 應用程式可以子類別屬於系統全域類別的視窗，例如編輯控制項或清單方塊。 例如，應用程式可以將編輯控制項設為子類別，以防止控制項接受某些字元。 不過，您無法將屬於另一個應用程式的視窗或類別設為子類別。 所有子類別化都必須在相同的進程中執行。

應用程式會將視窗的原始視窗程式位址取代為新視窗程式的位址（稱為子 *類別* 程式），以子類別化視窗。 之後，子類別程式就會收到任何傳送或張貼至視窗的訊息。

在接收訊息時，子類別程式可以採取三個動作：它可以將訊息傳遞至原始視窗程式、修改訊息並將它傳遞給原始視窗程式，或處理訊息，而不將它傳遞至原始視窗程式。 如果子類別程式處理訊息，它可以在將訊息傳遞至原始視窗程式之前、之後或前後進行。

系統提供兩種類型的子類別： [instance](#instance-subclassing) 和 [global](#global-subclassing)。 在子類別化的 *實例* 中，應用程式會取代視窗的單一實例的視窗程式位址。 應用程式必須使用實例子類別化現有的視窗。 在 *全域* 子類別中，應用程式會取代視窗類別的 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) 結構中的視窗程式位址。 所有以類別建立的後續視窗都有子類別程式的位址，但是類別的現有視窗則不受影響。

### <a name="instance-subclassing"></a>實例子類別化

應用程式會使用 [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) 函數將視窗的實例子類別。 應用程式會將 **GWL \_ WNDPROC** 旗標、視窗的控制碼傳遞給子類別，以及要 **SetWindowLong** 的子類別程式位址。 子類別程式可以位於應用程式的可執行檔或 DLL 中。

[**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) 會傳回視窗的原始視窗程式位址。 應用程式必須儲存位址，並在後續呼叫 [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) 函式時使用它，以將攔截的訊息傳遞給原始的視窗程式。 應用程式也必須有原始的視窗程式位址，才能從視窗中移除子類別。 若要移除子類別，應用程式會再次呼叫 **SetWindowLong** ，以 **GWL \_ WNDPROC** 旗標和視窗的控制碼傳遞原始視窗程式的位址。

系統擁有系統全域類別，而控制項的各個層面可能會從系統的某個版本變更為下一個版本。 如果應用程式必須將屬於系統全域類別的視窗子類別化，開發人員可能需要在發行新版的系統時更新應用程式。

因為實例子類別發生在建立視窗之後，所以您無法在視窗中加入任何額外的位元組。 子類別化視窗的應用程式應該使用視窗的屬性清單來儲存子類別化視窗實例所需的任何資料。 如需詳細資訊，請參閱 [視窗屬性](window-properties.md)。

當應用程式子類別化的子類別化視窗時，必須以執行的反向順序來移除子類別。 如果未反轉移除順序，則可能會發生無法復原的系統錯誤。

### <a name="global-subclassing"></a>全域子類別

若要全域子類別化視窗類別，應用程式必須具有類別的視窗控制碼。 應用程式也需要控制碼來移除子類別。 若要取得控制碼，應用程式通常會建立要子類別化之類別的隱藏視窗。 取得控制碼之後，應用程式會呼叫 [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) 函式，並指定控制碼、 **GCL \_ WNDPROC** 旗標，以及子類別程式的位址。 **SetClassLong** 會傳回類別的原始視窗程式位址。

原始的視窗程式位址用於全域子類別化，其方式與在實例子類別中使用的方式相同。 子類別程式會藉由呼叫 [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca)，將訊息傳遞至原始視窗程式。 應用程式會從視窗類別移除子類別，方法是再次呼叫 [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) 、指定原始視窗程式的位址、 **GCL \_ WNDPROC** 旗標，以及要子類別化之類別的視窗控制碼。 當應用程式終止時，全域子類別化控制項類別的應用程式必須移除子類別。否則，可能會發生無法復原的系統錯誤。

全域子類別與實例子類別具有相同的限制，加上一些額外的限制。 應用程式不應該將額外的位元組用於類別或視窗實例，而不需要知道原始視窗程式如何使用它們。 如果應用程式必須將資料與視窗建立關聯，則應該使用視窗屬性。

## <a name="window-procedure-superclassing"></a>視窗程式 Superclassing

*Superclassing* 是一種技術，可讓應用程式使用現有類別的基本功能來建立新的視窗類別，加上應用程式所提供的增強功能。 超級類別是以稱為 *基類* 的現有視窗類別為基礎。 基類通常是系統全域視窗類別，例如編輯控制項，但可以是任何視窗類別。

超級類別有自己的視窗程式，稱為「超級類別」程式。 *超級類別* 程式可以在接收訊息時採取三個動作：它可以將訊息傳遞至原始視窗程式、修改訊息並將它傳遞給原始視窗程式，或處理訊息，而不將它傳遞至原始視窗程式。 如果超級類別程式處理訊息，它可以在將訊息傳遞至原始視窗程式之前、之後或前後進行。

與子類別程式不同的是，超級類別程式可以處理 ([**wm \_ NCCREATE**](wm-nccreate.md)、 [**WM \_ 建立**](wm-create.md)等) 的視窗建立訊息，但它也必須將它們傳遞給原始的基類視窗程式，才能讓基類視窗程式執行其初始化程式。

若要將視窗類別設為超類，應用程式會先呼叫 [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa) 函式，以取得基類的相關資訊。 **GetClassInfo** 會以基類的 **WNDCLASS** 結構中的值填滿 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構。 接下來，應用程式會將自己的實例控制碼複製到 **WNDCLASS** 結構的 **hInstance** 成員，並將該超類的名稱複製到 **lpszClassName** 成員中。 如果基底類別具有功能表，則應用程式必須提供具有相同功能表識別碼的新功能表，並將功能表名稱複製到 **lpszMenuName** 成員中。 如果超級類別程式處理了 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息，但未將它傳遞給基類的視窗程式，則功能表不需要有對應的識別碼。 **GetClassInfo** 不會傳回 **WNDCLASS** 結構的 **lpszMenuName**、 **lpszClassName** 或 **hInstance** 成員。

應用程式也必須設定 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構的 **lpfnWndProc** 成員。 [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa)函式會使用類別的原始視窗程式位址來填滿這個成員。 應用程式必須儲存此位址、將訊息傳遞至原始視窗程式，然後將超級類別程式的位址複製到 **lpfnWndProc** 成員中。 如有必要，應用程式可以修改 **WNDCLASS** 結構的任何其他成員。 在填滿 **WNDCLASS** 結構之後，應用程式會將結構的位址傳遞至 [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) 函式，以註冊該類別。 然後可以使用超級類別來建立視窗。

由於 superclassing 會註冊新的視窗類別，因此應用程式可以同時加入額外的類別位元組和額外的視窗位元組。 超級類別不能使用基類或視窗的原始額外位元組，因為實例子類別或全域子類別不應使用它們。 此外，如果應用程式將額外的位元組用於類別或視窗實例，就必須參考相對於原始基類所使用之額外位元組數的額外位元組數。 由於基類所使用的位元組數目可能會與基類的某個版本不同，因此，超類別本身的額外位元組起始位移可能也會與下一個基類版本的不同。

 

 
