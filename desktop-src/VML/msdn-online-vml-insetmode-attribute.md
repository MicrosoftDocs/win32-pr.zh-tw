---
title: VML InsetMode 屬性
description: VML InsetMode 屬性
ms.assetid: 3cdce299-a490-43b9-93f5-09aca443e98b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f3ddee2a3c8060a9aa89dbd17bca329c1a105c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967488"
---
# <a name="vml-insetmode-attribute"></a>VML InsetMode 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義應用程式將如何允許自訂內凹值。 讀取/寫入 **字串**。

**適用於**

[TextBox](msdn-online-vml-textbox-element.md)

**標記語法**

<v： *element* o:insetmode = " *expression* " >

**備註**

數值包括：

-   自動
-   自訂 (預設) 

如果值為 **auto**，則不允許自訂內凹值，而且應用程式會決定 textbox 的內部文字邊界。

*Microsoft Office Extensions 屬性*

 

 