---
title: 關於 SysLink 控制項
description: SysLink 控制項是一種視窗，會轉譯標記的文字，並在使用者按一下其內嵌超連結時通知應用程式。 此控制項提供使用 [命令連結] 按鈕的方便替代方法。 如需詳細資訊，請參閱按鈕類型。
ms.assetid: 38cfac3d-de60-4882-a434-4f498330b77d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc4a5d64af48fc0b48b15f22fff55e5cb563339ac8d90446981c74e07f5d4713
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168558"
---
# <a name="about-syslink-controls"></a>關於 SysLink 控制項

SysLink 控制項是一種視窗，會轉譯標記的文字，並在使用者按一下其內嵌超連結時通知應用程式。 此控制項提供使用 [ [**命令連結] 按鈕**](button-styles.md)的方便替代方法。 如需詳細資訊，請參閱 [按鈕類型](button-types-and-styles.md)。

每個 SysLink 控制項都可以支援多個超連結，而且您可以透過以零為基底的索引來存取每個超連結。 SysLink 控制項是在 ComCtl32.dll 第6版中定義，而且需要資訊清單或指示詞，指定應該使用第6版的 DLL （如果有的話）。 如需詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

本文包含下列各節。

-   [SysLink 標記](#syslink-markup)
-   [連結屬性](#link-attributes)
-   [連結狀態](#link-states)
-   [雙向文字顯示的限制](#limitations-on-bidirectional-text-display)

## <a name="syslink-markup"></a>SysLink 標記

SysLink 控制項支援 () 的錨點 &lt; 標記 &gt; 以及屬性 **HREF** 和 **ID**。 **HREF** 可以是任何通訊協定，例如 HTTP、ftp 和 mailto。 **識別碼** 是選擇性的名稱，在 SysLink 控制項內是唯一的，而且與個別連結相關聯。 連結也會根據其在字串中的位置，指派以零為基底的索引。 此索引是用來存取連結。

## <a name="link-attributes"></a>連結屬性

每個連結的屬性都可以在每個連結的錨點標記內設定，或藉由傳送 [**LM \_ SETITEM**](lm-setitem.md) 訊息來設定。 藉由在初始化字串內指定屬性來設定屬性，只會初始化該值。 您可以透過後續使用 **LM \_ SETITEM** 訊息來變更屬性的值。

## <a name="link-states"></a>連結狀態

連結專案可以是三種狀態的其中一種，以下表中的旗標表示。



| 狀態旗標   | 外觀和意義                                            |
|--------------|-------------------------------------------------------------------|
| 以 .LIS 為 \_ 焦點 | 此連結具有鍵盤焦點，按下 Enter 會啟用它。 |
| \_已啟用 .LIS | 連結已啟用。                                              |
| 已 \_ 造訪的 .LIS | 使用者已流覽過連結所代表的 URL。     |



 

## <a name="limitations-on-bidirectional-text-display"></a>雙向文字顯示的限制

某些語言（例如阿拉伯文或希伯來文）是由右至左寫入 (RTL) ;英文是由左至右 (LTR) 撰寫。 將 RTL 與 LTR 合併稱為雙向文字。 將 LTR 和 RTL Unicode 或 HTML 方向標記結構混合在資源字串中，做為控制字元串流程的雙向流程標記，在使用 SysLink 控制項時，可能不會產生預期的結果。 例如，LTR 標記的句子可能無法在 RTL 內容中正確顯示。

> [!Note]  
> 在所有情況下，SysLink 控制項不支援雙向顯示。 只有當您知道簡單的 LTR 或 RTL 配置已足夠時，才使用 SysLink 控制項。 否則，請考慮使用更先進的技術，例如 [MSHTML](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85))。

 

 

 