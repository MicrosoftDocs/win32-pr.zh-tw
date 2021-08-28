---
description: PNRP 會使用 WSALookupServiceEnd 函數來執行下列作業。
ms.assetid: 0732929e-ca03-438f-80d9-48a3da0095f7
title: PNRP 和 WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9d91dea87b5a8c41cb5f689d89464bf7fd7e0179b1cad71943c14d107842b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553378"
---
# <a name="pnrp-and-wsalookupserviceend"></a>PNRP 和 WSALookupServiceEnd

PNRP 會使用 [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) 函數來執行下列作業：

-   終止先前呼叫 WSALookupServiceBegin 所起始的查詢[ ](winsock-nsp-reference-links.md)
-   解除封鎖對 [**WSALookupServiceNext**](winsock-nsp-reference-links.md) 的呼叫以停止搜尋

呼叫 [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) 會終止查詢並清除內容。 從呼叫 **WSALookupServiceBegin** 取得的控制碼必須傳遞至 **WSALookupServiceEnd** 的參數。

如需 PNRP 和 [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) 函數的詳細資訊，請參閱 [pnrp 和 WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[PNRP 和 WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[PNRP NSP 錯誤碼](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSALookupServiceNext**](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



