---
title: VML 單位
description: 本文描述 VML 單位。 VML 是 Windows Internet Explorer 9 淘汰的功能。
ms.assetid: f95e65ad-d92a-460f-baeb-30fd8a35f84e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c510bacd2081fb5a051637b6b577fc9415662737d384d10d7c3dd73348c694
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597379"
---
# <a name="vml-units"></a>VML 單位

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

VML 會使用下列 CSS 單位。



相對長度單位

Em

元素字型的高度。

前

字母 "x" 的高度。

px

圖元。

%

百分比。

絕對長度單位

in

英寸 (1 英寸 = 2.54 釐米 ) 。

cm

釐米。

mm

毫米。

pt

點 (1 點 = 1/72 英寸 ) 。

pc

十二點活字 (1 十二點活字 = 12 點 ) 。



 

級聯樣式表 (CSS) 屬性使用長度單位來進行測量和位置。 Internet Explorer 支援兩種類型的長度單位：相對和絕對。

相對長度單位會指定相對於另一個 length 屬性的長度。 相對長度單位會從一個輸出裝置更好地調整為另一個輸出裝置，例如從監視器到印表機。 百分比和關鍵字的執行方式類似。

絕對長度單位會指定絕對量測，例如英寸或釐米。 當已知輸出裝置的實體屬性時，絕對長度單位會很有用。

## <a name="other-units-of-measurement"></a>其他測量單位

**動 車組**

 (英文度量單位) 的 EMU 是最小的實用單位，而且是由 VML 用於內部單位儲存。 點中有914400個每英寸的 EMU 和12700個 EMU。 EMUs 不可為小數。

由於 EMUs 是由32位帶正負號的整數所定義，因此最大的 EMUs 數目是2348英寸 (大約59計量或65碼) 。 因為量測一律會符合螢幕或頁面大小的輸出裝置，所以它們一律會在此範圍內。

**角度**

您可以使用下列尾碼來定義角度度量。



後置詞

Fd

分數。

無

Degrees

度

Degrees

rad

Radians



 

 

 