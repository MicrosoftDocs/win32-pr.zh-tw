---
title: 列印屬性工作表
description: '[列印] 屬性工作表是標準使用者介面，可讓使用者指定特定列印工作的屬性。'
ms.assetid: b52b71cc-a583-4a21-8a53-501ab442e6f8
keywords:
- Windows消費者介面，使用者輸入
- Windows消費者介面，通用對話方塊程式庫
- 使用者輸入、通用對話方塊程式庫
- 正在捕獲使用者輸入，通用對話方塊程式庫
- 通用對話方塊程式庫
- 通用對話方塊
- '[列印屬性工作表] 對話方塊'
- 自訂列印屬性工作表對話方塊
- 預先定義的對話方塊
- 對話方塊、列印屬性工作表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc54bc8065ada207702755e8fc0a1586620f660db9f3acf2a67e32b56e393143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280504"
---
# <a name="print-property-sheet"></a>列印屬性工作表

[ **列印** ] 屬性工作表是標準使用者介面，可讓使用者指定特定列印工作的屬性。 屬性工作表是由印表機或應用程式一組不同的屬性頁所組成。 若為標準 Windows 內容頁的子集，某些印表機可能會新增驅動程式特定的屬性頁，而某些應用程式可能會新增應用程式特定的屬性頁。

若要建立和顯示 **列印** 屬性工作表，請初始化 [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) 結構，並將結構傳遞至 [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) 函數。

下圖顯示典型的 **列印** 屬性工作表。

![印表機屬性工作表](images/printerpropertypagexp.png)

[**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)結構的大部分成員都與 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)結構的成員相同。 如需如何使用通用結構成員與對話方塊控制項互動的說明，請參閱 [ [列印] 對話方塊](print-dialog-box.md)。 本主題的其餘部分將描述不同于 [**列印**] 對話方塊的 **列印** 屬性工作表功能。

您可以在 [**一般**] 頁面的下半部指定自訂對話方塊範本，並指定其他屬性頁以遵循 [**一般**] 頁面，以自訂 **列印** 屬性工作表。 如需詳細資訊，請參閱 [自訂列印屬性工作表](#customizing-the-print-property-sheet)。

您可以執行回呼物件，以在顯示內容表時，從 [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) 函式接收通知和訊息。 提供自訂範本或其他頁面的應用程式會使用回呼物件與屬性工作表進行通訊。 如需詳細資訊，請參閱 [Print 屬性工作表的回呼物件](#callback-object-for-the-print-property-sheet)。

[ **列印** ] 屬性工作表提供將多個非連續頁面範圍指定為列印的支援。 [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)結構的 **lpPageRanges** 成員會指定 [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange)結構的陣列，其中每個結構都指定一個頁面範圍。

[**列印** 屬性工作表] 會在選項按鈕群組的 [**頁面範圍**] 群組中顯示 [**目前的頁面**] 選項按鈕。 若要控制 **目前的頁面** 選項按鈕，請在 [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)結構的 **旗標** 成員中使用 **pd \_ CURRENTPAGE** 和 **pd \_ NOCURRENTPAGE** 旗標。

本節將討論下列主題。

-   [自訂列印屬性工作表](#customizing-the-print-property-sheet)
-   [列印屬性工作表的回呼物件](#callback-object-for-the-print-property-sheet)

## <a name="customizing-the-print-property-sheet"></a>自訂列印屬性工作表

您可以透過下列方式自訂 **列印** 屬性工作表：

-   提供 [ **一般** ] 頁面下半部的自訂範本。 這可讓您包含應用程式特有的其他控制項。 [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))函式會使用您的自訂範本來取代預設範本。
-   提供其他屬性頁以遵循 [ **一般** ] 頁面。
-   提供回呼物件。 如需詳細資訊，請參閱 [Print 屬性工作表的回呼物件](#callback-object-for-the-print-property-sheet)。

您無法變更 [ **一般** ] 頁面的上半部。 您無法變更印表機驅動程式所提供的屬性頁。

提供 [一般] 頁面的自訂範本：

1.  藉由修改 Prnsetup 檔案中指定的 PRINTDLGEXORD 範本，為 [ **一般** ] 頁面的下半部建立自訂範本。 一般而言，自訂範本的大小必須與預設範本相同。 但是，如果您指定 **PD \_ USELARGETEMPLATE** 旗標來建立較大的 **一般** 頁面，就可以放大自訂範本。 預設 [ **列印** ] 對話方塊範本中使用的控制項識別碼是在 Dlgs 檔中定義。
2.  使用 [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) 結構來啟用範本，如下所示：
    -   如果您的自訂範本是應用程式或動態連結程式庫中的資源，請在 **旗標** 成員中設定 **PD \_ ENABLEPRINTTEMPLATE** 旗標。 使用結構的 **hInstance** 和 **lpPrintTemplateName** 成員來識別模組和資源名稱。

        -或者-

    -   如果您的自訂範本已在記憶體中，請設定 **PD \_ ENABLEPRINTTEMPLATEHANDLE** 旗標。 您可以使用 **hInstance** 成員來識別包含範本的記憶體物件。

3.  如果您使用自訂範本來定義其他控制項，您必須提供回呼物件來處理控制項的輸入。 回呼物件會執行 [**IPrintDialogCallback：： HandleMessage**](/windows/win32/api/commdlg/nf-commdlg-iprintdialogcallback-handlemessage) 方法，以接收傳送至自訂對話方塊的訊息。

若要提供其他屬性頁

1.  使用函式來建立額外的頁面。
2.  您可以使用 [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)結構的 **lphPropertyPages** 成員，指定其他頁面的控制碼陣列。

    當您建立每個頁面處理傳送至頁面的訊息時，所指定的對話方塊程式。

3.  您可能會想要提供可執行介面的回呼物件。 [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))函式會使用此介面，將指向 [**IPrintDialogServices**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogservices)介面的指標傳遞至應用程式。 其他屬性頁的對話方塊程式可以使用此介面來取得目前所選印表機的相關資訊。

## <a name="callback-object-for-the-print-property-sheet"></a>列印屬性工作表的回呼物件

顯示 **列印** 屬性工作表的應用程式可以執行回呼物件，以在顯示內容表時，從 [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) 函式接收通知和訊息。 若要提供回呼物件，請在 [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)結構的 **lpCallback** 成員中指定物件的指標。

回呼物件必須執行 [**IPrintDialogCallback**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogcallback) 介面。 [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))函數會在下列情況下呼叫 **IPrintDialogCallback** 方法：

-   當對話方塊已初始化時
-   當使用者從屬性工作表所顯示的已安裝印表機清單中選取不同的印表機時
-   當它在屬性工作表的 **[一般** ] 頁面的下半部收到子對話方塊的訊息時

回呼物件也應該執行 [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) 介面。 [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))函式會呼叫方法，以將 [**IPrintDialogServices**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogservices)介面的指標傳遞至應用程式。 [**IPrintDialogCallback**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogcallback)方法可以使用 **IPrintDialogServices** 介面來取得目前所選印表機的相關資訊。 **IPrintDialogServices** 介面也適用于建立其他頁面的應用程式，以遵循 [**列印** 屬性工作表] 的 **[一般**] 頁面。 其他頁面的對話方塊程式可以呼叫 **IPrintDialogServices** 方法。

 

 