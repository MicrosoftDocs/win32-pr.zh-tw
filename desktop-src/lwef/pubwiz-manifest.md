---
title: 使用傳送資訊清單
description: Web 發佈嚮導和線上列印順序 Wizard 會使用傳輸資訊清單來傳達用戶端電腦與伺服器網站之間資料傳輸的詳細資料。
ms.assetid: b7bb541c-3bf4-4aab-ac70-c006517e772e
keywords:
- Web 發佈嚮導，傳送資訊清單
- 線上列印訂購嚮導，傳送資訊清單
- 傳送資訊清單
- manifest
- window. external、transfer 資訊清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d7f4ea3f9cd392f4b0bab50e1e558613fc7485d4f44a27472cd48ad898b3ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555848"
---
# <a name="using-the-transfer-manifest"></a>使用傳送資訊清單

Web 發佈嚮導和線上列印順序 Wizard 會使用傳輸資訊清單來傳達用戶端電腦與伺服器網站之間資料傳輸的詳細資料。

## <a name="the-purpose-of-the-transfer-manifest"></a>傳送資訊清單的用途

傳送資訊清單描述傳輸中牽涉到的檔案，包括目的地階層和檔案中繼資料等詳細資料。 伺服器端腳本可以修改資訊清單，方法是從清單中移除不適當的檔案，並新增有關如何以及應該如何傳送檔案的資訊。

資訊清單會公開為屬性 **視窗。 external. property ( "TransferManifest" )**，XML 檔物件模型 (DOM) 檔。 如需有關 XML DOM 的詳細資訊，請參閱 [IXMLDOMDocument/DOMDocument](/previous-versions/windows/desktop/ms756987(v=vs.85))的 MSDN 檔。

傳送資訊清單的最上層組織如下所示：


```
<transfermanifest>
    <filelist/>
    <folderlist/>
    <uploadinfo/>
</transfermanifest>
```



伺服器端 HTML 網頁可以使用資訊清單中的節點來取得要複製之檔案的特定資訊，然後據以修改服務的 UI。 比方說，相片列印網站可能會使用此資訊來顯示所選影像的縮圖，而儲存場所可能會使用此資訊，以確保該使用者有足夠的儲存空間可供使用。 如需有關傳送資訊清單節點和屬性的完整資訊，請參閱 [傳送資訊清單架構](/windows/desktop/shell/interfaces)。

傳送資訊清單架構會以開啟的模型的形式寫入，因此不會在架構中明確定義的元素可能會出現在傳送資訊清單中。 因此，提供者網站可能會新增專屬專案以供自己使用，而不會干擾資訊清單的有效性。 架構也會定義成不限制元素的順序。

> [!Note]  
> 每次選擇新的提供者時，就會重新建立資訊清單，讓提供者有機會將網站資訊儲存在資訊清單中。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[傳送資訊清單架構](/windows/desktop/shell/interfaces)
</dt> </dl>

 

 