---
description: 來源解析程式
ms.assetid: 93eecf10-308b-4bb4-92f9-fd32d6ecdb04
title: 來源解析程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a844893b0348546d4fd174b0b24405812efcef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318728"
---
# <a name="source-resolver"></a>來源解析程式

來源解析程式會接受 URL 或位元組資料流，然後為該內容建立適當的媒體來源。 來源解析程式是應用程式建立媒體來源的標準方式。

來源解析程式會在內部使用 *處理常式* 物件：

-   *配置處理常式* 會使用 URL，並建立媒體來源或位元組資料流程。
-   *位元組資料流程處理常式* 會採用位元組資料流程並建立媒體來源。

您可以執行自訂處理常式，並將它新增至登錄。 配置處理常式是由 URL 配置所註冊，而位元組資料流程處理常式是由副檔名或 MIME 型別所註冊。

本主題包含下列幾節：

-   [使用來源解析程式](using-the-source-resolver.md)
-   [設定媒體來源](configuring-a-media-source.md)
-   [配置處理常式和 Byte-Stream 處理常式](scheme-handlers-and-byte-stream-handlers.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體來源](media-sources.md)
</dt> </dl>

 

 



