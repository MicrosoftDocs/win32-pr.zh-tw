---
description: 您所建立的應用程式類型會決定要支援的筆墨保存格式。
ms.assetid: bd0a4382-f014-4f03-990d-d2f96aa76ab8
title: 選擇要支援的格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b8b2197c37db603388a4191e08114800aaba37ee8e89803c7ddfb08be18d3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110998"
---
# <a name="choosing-which-formats-to-support"></a>選擇要支援的格式

您所建立的應用程式類型會決定要支援的筆墨保存格式。

## <a name="single-ink-object-applications"></a>單一筆墨物件應用程式

檔僅包含筆墨的應用程式應該使用筆墨序列化格式 (ISF) 。 它們應該可以複製並貼上筆跡序列化格式 (ISF) 。 例如，用於繪製或注釋的應用程式。 這些應用程式可以使用 [**ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)和 [**ClipboardPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste) 方法。

## <a name="complex-applications"></a>複雜的應用程式

檔中包含其他內容（例如文字）的應用程式，除了 ISF 之外，還應該複製含有嚴加防禦圖形交換格式 (GIF) 檔案的 HTML。 HTML 本身必須由應用程式產生，雖然 Tablet PC 應用程式開發介面 (Api) 產生 GIF 檔。 這些應用程式也應該能夠複製和貼上 ISF，以與上述應用程式交互操作。

## <a name="rtf"></a>RTF

如果需要與 Microsoft Word 2002 或其他繼承應用程式之間的互通性，應用程式應該能夠產生豐富的文字格式 (rtf) 。

## <a name="mime-support"></a>MIME 支援

下表列出建議的多用途網際網路郵件延伸 (MIME) 標頭，以及使用 ISF 或 GIF 保存到檔案的筆墨副檔名。 這些值可在 [**PersistenceFormat**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat) 列舉中找到。



| 持續性格式            | MIME 標頭                                                                                    | 副檔名            |
|-------------------------------|------------------------------------------------------------------------------------------------|---------------------------|
| **Base64Gif**                 | Content-type： application/x-ms-筆墨內容-傳輸-編碼： base64<br/>                | 不適用<br/> |
| **Base64InkSerializedFormat** | Content-type： Content-type： image/gif;格式 = 筆墨內容-傳輸-編碼： base64<br/> | 不適用<br/> |
| **Gif**                       | Content-type： application/x-ms-筆墨<br/>                                                  | .gif<br/>           |
| **InkSerializedFormat**       | Content-type： Content-type： image/gif;format = 筆墨<br/>                                   | isf<br/>           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**PersistenceFormat 列舉**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat)
</dt> </dl>

 

 




