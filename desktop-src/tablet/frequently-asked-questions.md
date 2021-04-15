---
description: 以下是有關針對 Windows Vista SDK 所安裝的 Tablet PC 平臺元件進行開發的常見問題 (常見問題) 。
ms.assetid: eb349493-a2b2-4b58-bcbc-ee09953c8dc8
title: " (Tablet PC 的常見問題) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8722c00fa5aaf2b43494484fc015fa8b3e4c7826
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2020
ms.locfileid: "104383446"
---
# <a name="frequently-asked-questions-about-developing-for-the-tablet-pc-platform"></a>針對 Tablet PC 平臺進行開發的常見問題

以下是有關針對 Windows Vista SDK 所安裝的 Tablet PC 平臺元件進行開發的常見問題 (常見問題) 。

## <a name="q-can-i-use-the-ink-apis-or-controls-in-a-web-page"></a>Q. 我可以在網頁中使用筆墨 Api 或控制項嗎？

A. 是。 Tablet PC 受控程式庫支援部分信任的環境，也就是從網頁執行受管理的元件。

此外，也支援使用 Windows Presentation Foundation 的應用程式的瀏覽器部署。

## <a name="q-do-i-need-a-tablet-pc-to-develop-tablet-pc-applications"></a>Q. 是否需要 Tablet PC 才能開發 Tablet PC 應用程式？

A. 否，Windows SDK 安裝的 Tablet PC 平臺元件包含在桌上型電腦或膝上型電腦上開發 Tablet PC 軟體所需的擴充功能與公用程式。 您可以使用滑鼠或外部平板電腦進行手寫筆和手寫輸入。

Windows SDK 安裝的 Tablet PC 平臺元件可以安裝在 Windows XP Professional 或 Windows Server 2003 上，但您的應用程式可使用較少的功能。 在這些平臺上，您的應用程式可以使用 [**InkCollector**](inkcollector-class.md) 和 [**InkOverlay**](inkoverlay-class.md) 物件來收集筆墨，並且可以進行測試和調試。

此外，只有當 Tablet PC 平臺元件是從 Windows SDK (或舊版 Tablet PC 開發工具組) ）安裝時， [InkEdit](inkedit-control-reference.md) 和 [InkPicture](inkpicture-control-reference.md) 控制項才能在這些作業系統上收集筆跡。這些應用程式不會在未安裝平臺元件的情況下，將應用程式中的筆墨收集至非 Tablet 電腦。

## <a name="q-do-i-need-to-run-a-special-version-of-windows-to-do-handwriting-recognition"></a>Q. 我是否需要執行特殊版本的 Windows 以執行手寫辨識？

A. 否。 雖然只有 Windows XP Tablet PC Edition 和特定版本的 Windows Vista 包含手寫辨識器，但您可以下載 [WINDOWS Xp TABLET Pc edition 2005 辨識器套件]( https://www.microsoft.com/downloads/details.aspx?FamilyId=080184DD-5E92-4464-B907-10762E9F918B&amp;displaylang=en) ，並將它安裝在 Windows xp Professional 或 windows Server 2003 上，以供開發之用。 您不得將辨識器與您的應用程式一起轉散發。

## <a name="q-what-is-the-difference-between-windows-vista-and-tablet-pc-technology"></a>Q. Windows Vista 和 Tablet PC 技術之間有何差異？

A. Tablet Pc 會執行 Windows Vista 作業系統，並採用 Windows Vista 的所有功能，再加上 Tablet PC 特有的其他功能。 這些 Tablet PC 技術功能可讓使用者使用畫筆、標注檔，以及使用數位筆跡建立手寫檔，來執行 Windows 和 Windows 應用程式。 Tablet PC 技術適用于大部分的 Windows Vista 版本，如果電腦上有可用的 Tablet PC 硬體，功能就會正常運作。

對於舊版不支援筆墨的 Windows 作業系統，您可以轉散發並使用 Tablet PC 筆墨控制項來查看在 Tablet PC 上繪製的筆墨。

## <a name="q-what-is-the-difference-between-windows-xp-tablet-pc-edition-and-windows-xp-tablet-pc-edition-2005"></a>Q. Windows XP Tablet PC Edition 和 Windows XP Tablet PC Edition 2005 之間有何差異？

A. Windows XP Tablet PC Edition 2005 是 Windows XP Tablet PC Edition 的更新版本。

## <a name="q-how-do-i-modify-my-application-to-run-on-a-tablet-pc"></a>Q. 如何? 修改我的應用程式以在 Tablet PC 上執行嗎？

A. 在 Windows XP 桌上型電腦或具有可比較硬體的膝上型電腦上執行的 Microsoft Windows 應用程式，可以在 Tablet PC 上執行而不需要修改。

## <a name="q-i-understand-that-i-dont-need-to-make-any-changes-to-my-application-but-it-is-difficult-to-use-it-with-a-pen-and-speech-what-can-i-do-to-optimize-my-application-for-a-tablet-pc"></a>Q. 我瞭解我不需要對我的應用程式進行任何變更，但很難使用畫筆和語音。 我可以如何針對 Tablet PC 優化我的應用程式？

A. Tablet PC 平臺元件的 API 和筆墨控制項可以用來建立更適合畫筆和手寫輸入的使用者介面。 如需有關您可以改進應用程式之特定方法的詳細資訊，請參閱 [開發人員的行動電腦使用者經驗指導方針](/previous-versions//dd356056(v=vs.85))。

## <a name="q-what-programming-languages-does-the-tablet-support"></a>Q. Tablet 支援哪些程式設計語言？

A. Windows Vista 中的 Tablet PC 技術支援 COM (c + +) 和 managed 程式庫 () 的 Visual Studio .NET 語言套件。

Tablet PC 技術也支援 Windows Presentation Foundation (WPF) 。

## <a name="q-do-i-have-sample-code-that-demonstrates-tablet-platform-capabilities"></a>Q. 我有示範平板電腦平臺功能的範例程式碼嗎？

A. 是的，COM 的範例程式碼和選取的受控語言都包含在 Windows Platform SDK 所安裝的 Tablet PC 平臺元件中。

如需可用的範例應用程式，請參閱：

- [行動電腦和 Tablet PC 範例](mobile-pc-and-tablet-pc-samples.md)
- [數位筆跡範例、Windows Presentation Foundation (WPF) ](/previous-versions/dotnet/netframework-3.0/aa972145(v=vs.85))
- <systemdrive>： \\ Program Files \\ Microsoft sdk \\ Windows \\ v 6.0 \\ 範例 \\ 平板版

## <a name="q-whats-the-base-level-of-tablet-hardware-that-i-should-develop-for"></a>Q. 我應開發的平板電腦硬體基本層級為何？

A. 一般情況下，您應該針對 Windows Vista 相容、舊版的系統設計。

## <a name="q-what-user-interface-guidelines-can-you-provide-for-tablet-applications"></a>Q. 您可以為 Tablet 應用程式提供哪些使用者介面指導方針？

A. 從下拉式功能表方向到螢幕/數位板視差的問題，請參閱 Windows SDK 的行動電腦上的 [開發人員行動電腦使用者經驗指導方針](/previous-versions//dd356056(v=vs.85)) 一節中所述。

## <a name="q-do-you-include-system-level-handwriting-gestures-for-commonly-used-keystrokes-can-i-create-my-own-gestures-for-use-when-an-application-is-running-or-has-focus"></a>Q. 您是否包含常用按鍵的系統層級手寫手勢？ 我可以建立自己的手勢，以在應用程式執行或焦點時使用嗎？

A. 是，我們包含一組滑鼠事件的手勢。 此外，您也可以建立要在應用程式中使用的手勢。 如需筆勢的詳細資訊，請參閱 [使用手勢](using-gestures.md)。

## <a name="q-how-can-i-determine-whether-my-application-is-running-on-a-tablet"></a>Q. 如何判斷我的應用程式是否正在平板電腦上執行？

A. 使用 Windows GetSystemMetricsAPI，並傳入 SM \_ 平板電腦作為索引的值。 SM \_ 平板電腦定義于 Winuser 中。 SM \_ 平板電腦的值為86。

針對 web 程式開發，您應該讀取使用者 \_ 代理 \_ 字串環境變數。 您可以存取此 ServerVariables 集合。

如需如何在執行 Windows Vista 或 Windows XP Tablet PC Edition 的平板電腦上使用 GetSystemMetrics 的詳細資訊，請參閱 [判斷電腦是否為 TABLET pc](determining-whether-a-pc-is-a-tablet-pc.md)。

## <a name="q-how-can-i-determine-whether-tablet-platform-components-are-available"></a>Q. 如何判斷是否可以使用 Tablet platform 元件？

A. Tablet PC 平臺的某些部分可能安裝在非平板電腦版本的 Windows XP Professional、Windows Server 2003 和 Windows 2000 作業系統上。

若要判斷是否已安裝 API 的元件，正確的方式是嘗試建立物件或控制項的實例，並檢查它是否存在，然後再嘗試使用它。

例如，若要判斷 [**InkCollector**](inkcollector-class.md) 物件是否可供使用，請嘗試使用 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)來建立它。

```C++
IInkCollector* pIInkCollector = NULL;
HRESULT hr = CoCreateInstance(CLSID_InkCollector,
 NULL, CLSCTX_INPROC_SERVER, 
 IID_IInkCollector,
 (void **)&pIInkCollector);
if (SUCCEEDED(hr)) 
{ 
  /* InkCollector is usable. */ 
} else 
{
  /* InkCollector unavailable. */
}
```

## <a name="q-how-do-i-run-the-tablet-input-service-on-server-skus"></a>Q. 如何? 在伺服器 Sku 上執行平板電腦輸入服務？

A. TabletInputService 的設計是在安裝用戶端套件時，不會在伺服器 Sku 中自動執行。 用戶端套件會安裝平臺中的所有元件，讓任何 Tablet 用戶端應用程式也可以在伺服器上執行。 Tablet 輸入服務會接聽是否已插入外部數位板的 PnP 通知。 若要在伺服器上啟用平板電腦輸入服務，請使用系統組態公用程式。

從 [ **開始** ] 功能表選取 [ **執行**]。 輸入 "msconfig"，然後按 Enter。 選取 [ **服務** ] 索引標籤，尋找名為「隱藏輸入服務」的服務，選取旁邊的核取方塊， **然後按一下 [** 套用]。 關閉公用程式。

## <a name="q-more-faqs-and-other-resources"></a>Q. 更多常見問題和其他資源

- [Microsoft 開發人員中心](https://developer.microsoft.com)
- [核心 Tablet PC 參考](./core-reference---tablet-pc-com-library.md)