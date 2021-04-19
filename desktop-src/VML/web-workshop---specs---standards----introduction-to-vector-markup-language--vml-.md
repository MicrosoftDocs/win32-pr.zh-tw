---
title: 'Vector Markup Language (VML) '
description: 'Vector Markup Language (VML) '
ms.assetid: 1f30d60f-3d4f-43e4-9a2b-424a5ee8f852
keywords:
- Vector Markup Language (VML) ，關於
- VML (Vector Markup Language) ，關於
- 向量圖形，關於
- '向量圖形、Vector Markup Language (VML) '
- 'Vector Markup Language (VML) ，全球資訊網協會 (W3C) '
- 'VML (Vector Markup Language) ，全球資訊網協會 (W3C) '
- '向量圖形，全球資訊網協會 (W3C) '
- 向量圖形，VML 優點
- Vector Markup Language (VML) ，優點
- VML (Vector Markup Language) ，優點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0ba51fd041f36915eaafe20201876653f597e04
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "107000510"
---
# <a name="vector-markup-language-vml"></a>Vector Markup Language (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!NOTE]
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

Vector Markup Language (VML) 是以 XML 為基礎的 exchange、編輯和傳遞格式，適用于 Web 上符合生產力使用者和圖形設計專業人員需求的高品質向量圖形。 XML 是一種新興的簡單、彈性且開放的文字語言，可補充 HTML。 如需 XML 的詳細資訊，請參閱 MSDN Library 的 [XML 一節](/documentation/?frame=true) (。 ) 

目前 Microsoft Internet Explorer 5.0 版或更新版本支援 VML。

已將 VML 建議為 W3C 作為 Web 上向量圖形的標準 (請參閱 [Vector Markup Language (VML) ](https://www.w3.org/TR/NOTE-VML)) 。 Microsoft 會繼續在開發和實行以 XML 為基礎的技術方面繼續收取費用， (AutoDesk、Hewlett Packard、Macromedia、Visio) 和 W3C 來推動以網路為基礎的標準。 我們預計在 Web 上使用 W3C 到最後一個標準格式的向量圖形。

Microsoft Office 2000 或更新版本也支援 VML。 Microsoft Word、Microsoft Excel 和 Microsoft PowerPoint 可以用來建立 VML 圖形。

### <a name="using-vml"></a>使用 VML

若要在您的網頁中使用 VML，請使用樣式元素來匯入 VML 行為，如下列程式碼所示。

```
<style>v\: * { behavior:url(#default#VML); display:inline-block }</style>
```

接下來，宣告 VML 命名空間，如下列程式碼範例所示。

```
<xml:namespace ns="urn:schemas-microsoft-com:vml" prefix="v" />
```

最後，新增 VML 元素來定義視覺效果。 例如，下列 VML 程式碼會建立紅色橢圓。

```
<v:oval style="width:100pt;height:50pt" fillcolor="red">
</v:oval>
```

> [!NOTE]
> 若要在使用 strict 模式檔時取得最佳結果，請確定您的標記有效且格式正確。 如需詳細資訊，請參閱！DOCTYPE 參考頁面。


### <a name="benefits-of-vml"></a>VML 的優點

-   VML 讓生產力使用者和作者更容易撰寫。 它可透過剪下和貼上) ，以及在各種生產力和設計應用程式之間進行向量圖形的後續編輯，來促進 exchange (。
-   VML 可提供更快速的圖形下載及更好的使用者體驗。 它可讓您使用以文字為基礎的開放格式，將高品質、完全整合、可擴充的向量圖形傳遞至 Web。 VML 圖形會與 HTML 網頁一起以內嵌方式傳遞，而不是以外部檔案的形式參考圖形，可讓它們與使用者互動進行互動及調整。
-   VML 是開放且以標準為基礎。 它是以 XML 為基礎的格式。 XML 1.0 是一種開放、簡單、以文字為基礎的語言，用來描述 Web 上的結構化資料，並補充 HTML 來顯示。 VML 也支援其他 W3C 標準，例如階層式樣式表 2.0 (CSS) ，它會指定樣式資訊和2D 定位，以及檔物件模型 (DOM) ，可讓開發人員以頁面元素一致地與物件互動。

### <a name="for-additional-information"></a>其他資訊

請參閱下列連結：

-   如需 VML 常見問題的解答，請參閱 [VML 常見問題](frequently-asked-questions-about-vml.md)。
-   如需在 Web 網頁上使用 VML 的教學課程，請參閱 [如何在網頁上使用 vml](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)，以補充提交給 W3C 的 [vml 規格](https://www.w3.org/TR/NOTE-datetime.html) 。
-   如需 VML 資料類型的詳細資訊，請參閱 [基本的 Vml 類型](basic-vml-types.md) 檔。
-   如需 VML 的完整參考，包括如何搭配使用 VML 與標記以及腳本的相關資訊，請參閱 [Vml 參考](msdn-online-vml-introduction.md)。