---
description: 圖形 API 會使用下列回呼：
ms.assetid: a8e083ab-b5e3-4186-99fb-cbb536e9d529
title: 圖形 API 回呼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11f4f559307e457822cd0e7ce18ef4b44119697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026754"
---
# <a name="graphing-api-callbacks"></a>圖形 API 回呼

圖形 API 會使用下列回呼：



| 回呼                                                          | Description                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*PFNPEER \_ 免費的 \_ 安全性 \_ 資料*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_free_security_data) | 指定對等圖形基礎結構呼叫的函式，以釋放 [*PFNPEER \_ SECURE \_ record*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record) 和 [*PFNPEER \_ VALIDATE \_ record*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record) 回呼所傳回的資料。 |
| [*PFNPEER \_ 安全 \_ 記錄*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record)            | 指定對等圖形基礎結構呼叫以保護記錄的函式。                                                                                                                                        |
| [*PFNPEER \_ 驗證 \_ 記錄*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record)        | 指定對等圖形基礎結構呼叫以驗證記錄的函式。                                                                                                                                      |



 

 

 



