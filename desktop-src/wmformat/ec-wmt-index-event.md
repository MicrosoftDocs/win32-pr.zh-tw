---
title: 'EC_WMT_INDEX_EVENT (Windows Media Format 11 SDK) '
description: EC \_ WMT \_ 索引 \_ 事件
ms.assetid: 46e6a011-7f25-470b-9e10-fa59f0ddbf22
keywords:
- Windows Media Format SDK，EC_WMT_INDEX_EVENT
- DirectShow，EC_WMT_INDEX_EVENT
- EC_WMT_INDEX_EVENT
- Advanced Systems Format (ASF) ，EC_WMT_INDEX_EVENT
- ASF (Advanced Systems Format) ，EC_WMT_INDEX_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f34bca14ed02ac78fcfc77d1b9b716f75115a24f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024423"
---
# <a name="ec_wmt_index_event-windows-media-format-11-sdk"></a>EC_WMT_INDEX_EVENT (Windows Media Format 11 SDK) 

當應用程式使用 ASF 寫入器為 Windows Media 視訊檔案編制索引時，由 Windows Media Format SDK 傳送。

參數

*lParam1*

可以是下列任何一個 **WMT \_ 狀態** 消息。



| 訊息              | 描述                                     |
|----------------------|-------------------------------------------------|
| WMT \_ 已開始         | 索引已開始。 *lParam2* 為零。          |
| WMT \_ 已關閉          | 索引已完成。 *lParam2* 為零。 |
| WMT \_ 索引 \_ 進度 | 正在編制索引。                        |



 

*lParam2*

如果 *lParam1* 是 WMT \_ CLOSED 或 WMT \_ 開始，則 *lParam2* 為零。 如果 *lParam1* 是 WMT \_ INDEX \_ 進度，則 *lParam2* 為 **DWORD** ，會以總下載大小的百分比來表示進度量。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DirectShow QASF 參考**](directshow-qasf-reference.md)
</dt> </dl>

 

 




