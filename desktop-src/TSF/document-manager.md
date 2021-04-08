---
title: 檔管理員
description: 檔管理員
ms.assetid: e30087b6-524a-481e-845d-0348bac3830a
keywords:
- '檔案管理員文字服務架構 (TSF) '
- TSF (文字服務架構) ，檔管理員
- 文字服務，檔管理員
- TSF 啟用應用程式，檔管理員
- 檔管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2182782218ad6a8aa0a70f296f639560307249
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672143"
---
# <a name="document-manager"></a>檔管理員

## <a name="applications"></a>應用程式

若要建立檔管理員物件，應用程式會呼叫 [ITfThreadMgr：： CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr)。 應用程式會針對應用程式所維護的每個個別檔建立個別的檔管理員物件。 應用程式會使用 [檔案管理員] 來建立編輯內容、將內容加入內容堆疊，以及從內容堆疊中移除內容。

## <a name="text-services"></a>文字服務

文字服務永遠不會建立檔管理員物件。 相反地，文字服務會藉由呼叫 [ITfThreadMgr：： GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)來取得目前使用中的檔管理員物件。 文字服務會使用檔管理員來取得堆疊頂端的內容。

文字服務也可以使用 [檔案管理員] 來建立自己的內容，並將它從內容堆疊中加入和移除。 這通常是在文字服務必須顯示某些強制回應使用者介面時完成，例如，當顯示單字清單讓使用者選取單字時。 當清單顯示時，文字服務會將自己的內容放在堆疊上。 當 word 清單關閉時，文字服務會將其內容從堆疊中移除。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[ITfThreadMgr：： CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr)
</dt> <dt>

[ITfThreadMgr：： GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> </dl>

 

 




