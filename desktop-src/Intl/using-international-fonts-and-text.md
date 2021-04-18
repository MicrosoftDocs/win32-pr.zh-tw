---
description: 在 Windows 的每個主要版本中，都有新增的字型可支援國際語言和腳本。
ms.assetid: 77b8c200-2682-4651-855a-602f768edc9b
title: 國際字型列舉和選取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e5d0d07a0953f72f097f8578f5e32b3ee49093
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321087"
---
# <a name="international-font-enumeration-and-selection"></a>國際字型列舉和選取

在 Windows 的每個主要版本中，都有新增的字型可支援國際語言和腳本。 請參閱 [windows 中的腳本與字型支援](https://msdn.microsoft.com/globalization/mt791278) ，以瞭解自 windows 2000 之後的每個 windows 版本中新增的字型，以及其支援的腳本、區域和語言。

## <a name="enumfontfamiliesex"></a>EnumFontFamiliesEx

若要列舉應用程式中的國際字型，您可以使用 [**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) 函數。 **EnumFontFamiliesEx** 可讓您將指標傳遞至包含字型名稱和字元集資訊的 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構，以根據字樣名稱和字元集來列舉字型。 若要呼叫 **EnumFontFamiliesEx**，您可以指定字樣名稱或字元集，也可以詢問是否有任何可用的。 將 **LOGFONT** 的字樣名稱設定為 **Null** 會列舉所有的字樣名稱。 將 [字元集] 欄位設定為 [ **預設 \_ 字元集** ] 會列舉所有字元集。

請注意，字元集是對應到預先 Unicode 字元集的舊版概念。 目前沒有任何機制可列舉以 Unicode 支援任意腳本或字元範圍的字型。 由 [**EnumFontFamExProc**](/previous-versions//dd162618(v=vs.85))傳遞的 [**NEWTEXTMETRICEX**](/windows/win32/api/wingdi/ns-wingdi-newtextmetricexa)結構包含 [**FONTSIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-fontsignature)結構，其中包含字型開發人員所提供的更詳細宣告，以做為該字型所支援的字碼頁和 Unicode 範圍。 若要更精確地判斷特定字型所支援的字元範圍，請在裝置內容中選取字型，然後呼叫 [**GetFontUnicodeRanges**](/windows/win32/api/wingdi/nf-wingdi-getfontunicoderanges)。 請注意，此 API 不支援 Unicode 補充平面。

## <a name="choosefont"></a>ChooseFont

您可以使用 [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) 函式來顯示通用對話方塊，讓使用者可以根據字元集選取國際字型。 您可以指定三個旗標中的其中一個，根據字元集（ChooseFont 對話方塊中顯示的字型： **CF \_ SCRIPTSONLY**、 **CF \_ SELECTSCRIPT** 或 **CF \_ NOSCRIPTSEL**）來決定。

**CF \_ SCRIPTSONLY** 旗標會告知 API 針對非符號或 OEM 的所有字元集列出字型。

如果您只想要顯示涵蓋特定字元集的字型，您必須指定旗標 **CF \_ SELECTSCRIPT**。 在呼叫 [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85))之前，請先初始化 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的 *lfCharSet* 欄位。 如果您只想要指定字元集，請將 **LOGFONT** 結構的其他欄位設為 **Null**。 若要讓 **ChooseFont** 查看 **LOGFONT** 結構，您也必須指定 **CF \_ INITTOLOGFONTSTRUCT** 旗標。

最後，如同 [字型] 對話方塊中的任何其他欄位，您可以選擇顯示 [空白腳本] 清單方塊。 如果使用者反白顯示數個橫跨數個字元集的不同字型，這項功能就很有用。 在此情況下，您會使用 **CF \_ NOSCRIPTSEL** 旗標來呼叫 [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) 。

從 Windows 7 開始， [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) 可支援從字型挑選清單隱藏字型。 **ChooseFont** 只會列出顯示的字型，並篩選出隱藏的字型，同時在清單方塊中顯示字型。 [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85))結構之 Flags 成員中的其他旗標 (**CF \_ INACTIVEFONTS**) ，可讓您在 [字型] 清單中顯示所有已安裝的字型，與 Windows 7 之前的 **ChooseFont** 行為相同。 如需 Windows 7 中 **ChooseFont** 函式的行為差異詳細資料，請參閱 [Windows 7 應用程式品質操作手冊](../win7appqual/windows-7-application-quality-cookbook.md)中的 [**ChooseFont () Win32 通用對話方塊**](../win7appqual/choosefont-win32-common-dialog.md)。 請參考 **ChooseFont** 函式和 **ChooseFont** 結構，以瞭解 Windows 7 中的終端使用者體驗差異。

請注意，字元集是對應到預先 Unicode 字元集的舊版概念。 目前沒有任何機制可根據 Unicode 腳本或字元範圍來篩選字型。

## <a name="font-controls-in-windows-scenic-ribbon"></a>Windows Scenic 功能區中的字型控制項

Windows 7 引進了 Windows Scenic 功能區，其中包含一組以字型選取為目標的控制項。 這些字型控制項支援新的 Windows 7 字型隱藏行為。 您可以使用這些字型控制項只列出顯示的字型，並允許使用者選取字型。

> [!Note]  
> 當 Windows Scenic 功能區在 Windows 7 之前的任何平臺上執行時，無法使用隱藏字型的支援。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa)
</dt> <dt>

[**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85))
</dt> <dt>

[**CHOOSEFONT 結構**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**Windows Scenic 功能區中的字型控制項**](../windowsribbon/windowsribbon-element-fontcontrol.md)
</dt> <dt>

[**ChooseFont () Win32 通用對話方塊**](../win7appqual/choosefont-win32-common-dialog.md)
</dt> </dl>

 

 
