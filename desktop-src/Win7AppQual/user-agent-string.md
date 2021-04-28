---
description: 使用者代理程式字串
ms.assetid: bcf0a534-c123-40c4-91b4-645c4912f31a
title: 使用者代理程式字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d227eead5c02f50b689779bd0a8f0ba4b031d06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084176"
---
# <a name="user-agent-string"></a>使用者代理程式字串

*使用者代理程式字串* 包含瀏覽器身分識別的相關資訊。 每次瀏覽器對 web 伺服器提出要求時，使用者代理字串會以 HTTP 標頭的形式回報給 web 伺服器。 您也可以透過用戶端腳本來存取它。 例如，您可以在 Windows Internet Explorer 8 的 [位址列] 中輸入下列 URL 來顯示使用者代理字串： "javascript： alert (userAgent) "。 下圖顯示在 Windows 7 上執行 Internet Explorer 8 的一般結果對話方塊。

![具有使用者代理程式字串之 internet explorer diaog 方塊的螢幕擷取畫面](images/useragent-alert.png)

一般而言，會特別針對 MSIE 子字串剖析使用者代理字串。 根據報告的瀏覽器版本，用戶端或伺服器端程式設計邏輯會採取不同的動作。 如需有關使用者代理程式字串的詳細資訊，請參閱 MSDN Library 中的 [Windows Internet Explorer 會如何報告為 User-Agent 字串？](/previous-versions/cc817582(v=msdn.10)) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用相容性檢視修正 Web 應用程式中的相容性問題](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



