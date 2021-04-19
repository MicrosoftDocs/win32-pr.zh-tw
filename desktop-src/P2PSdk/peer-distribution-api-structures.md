---
description: Microsoft 對等散發服務支援下列結構。
ms.assetid: 26badfe6-3a5a-4c2e-9ef1-534c2e8573d0
title: 對等散發 API 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc9fbf86c242406aa86b7dd30497ba4c5085488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977326"
---
# <a name="peer-distribution-api-structures"></a>對等散發 API 結構

Microsoft 對等散發服務支援下列結構。



| 結構                                                              | Description                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PEERDIST \_ 用戶端 \_ 基本 \_ 資訊**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_client_basic_info)    | 指出是否有許多用戶端同時下載相同的內容。                                                                                                                                                                                             |
| [**PEERDIST \_ 內容 \_ 標記**](/windows/win32/api/peerdist/ns-peerdist-peerdist_content_tag)                 | 包含用戶端提供的標記，這是 [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)的輸入值。 此標記與內容區段相關聯，並用於內容管理 Api，例如 [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent)。 |
| [**PEERDIST \_ 發行集 \_ 選項**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_publication_options) | 包含發行集選項，包括 API 版本資訊和可能的選項旗標。                                                                                                                                                                                           |
| [**對等抓取 \_ \_ 選項**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_retrieval_options)         | 包含要取出的內容資訊版本。                                                                                                                                                                                                                                 |
| [**PEERDIST \_ 狀態 \_ 資訊**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_status_info)                 | 包含本機電腦上 BranchCache 服務目前狀態和功能的相關資訊。                                                                                                                                                                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[對等散發 API 參考](peer-distribution-api-reference.md)
</dt> </dl>

 

 



