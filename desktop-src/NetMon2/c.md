---
description: 以字母 C 為開頭網路監視器詞彙的詞彙。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e0b9f77-8a47-4724-b08c-fac3b6e23afc
title: 'C (網路監視器) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06dd8ccd4d4c3382e7f7f7bb4426320bfcd8d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981556"
---
# <a name="c-network-monitor"></a>C (網路監視器) 

<dl> <dt>

<span id="_netmon_capture_gly"></span><span id="_NETMON_CAPTURE_GLY"></span>**捕獲**
</dt> <dd>

在畫面格中收集的網路流量資料。 網路封包提供者 (NPP) 執行捕獲。 另請參閱 [*延遲的捕獲*](d.md)和 *即時捕獲*

</dd> <dt>

<span id="_netmon_capture_file_gly"></span><span id="_NETMON_CAPTURE_FILE_GLY"></span>**capture 檔案**
</dt> <dd>

網路監視器建立以儲存已捕捉資料的檔案。 Cap 副檔名會識別 capture 檔。 網路監視器隨機產生 capture 檔案名，但您可以在儲存 capture 檔案時變更檔案名。

網路監視器會在每次捕捉程式啟動時建立 capture 檔案，然後在捕獲程式期間讓檔案保持開啟。 在停用捕捉程式並關閉 capture 檔案之前，您無法存取 capture 檔案的內容。

</dd> <dt>

<span id="_netmon_capture_filter_gly"></span><span id="_NETMON_CAPTURE_FILTER_GLY"></span>**capture 篩選**
</dt> <dd>

一組網路監視器函式，用來限制網路封包提供者 (NPP) 應用程式所使用的內送框架。

</dd> <dt>

<span id="_netmon_capture_trigger_gly"></span><span id="_NETMON_CAPTURE_TRIGGER_GLY"></span>**capture 觸發程式**
</dt> <dd>

設定為停止 capture 進程的觸發程式事件。 Capture 觸發程式事件可以是暫時的捕獲檔案，該檔案會被導向至已捕捉到的框架中所發生的特定層級或資料模式。

</dd> <dt>

<span id="_netmon_captured_data_gly"></span><span id="_NETMON_CAPTURED_DATA_GLY"></span>**已捕獲資料**
</dt> <dd>

具有一組已定義準則的框架。 資料框架包含在暫時性的捕獲檔案中。

</dd> <dt>

<span id="_netmon_conversation_statistics_gly"></span><span id="_NETMON_CONVERSATION_STATISTICS_GLY"></span>**對話統計資料**
</dt> <dd>

在捕捉期間儲存的網路流量統計資料。 這些統計資料包括捕捉程式啟動時開始的站和會話資訊，並且在捕捉停止時結束。 如果您暫停捕捉程式，網路監視器會在繼續處理時繼續新增統計資料。 若要取得對話統計資料，請針對您所使用的介面呼叫 **GetConversationStatistics** 方法。

</dd> </dl>

 

 



