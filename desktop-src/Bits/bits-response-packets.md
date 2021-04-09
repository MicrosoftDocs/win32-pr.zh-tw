---
title: BITS 回應封包
description: BITS 回應封包
ms.assetid: 30755476-daa9-42ea-8fb3-5b505fc9dd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755e28b749d201a2c90640ea9e456f012f790453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839368"
---
# <a name="bits-response-packets"></a>BITS 回應封包

下表列出針對上傳和上傳-回復作業傳送至 BITS 用戶端的回應封包。 資料表會列出傳送給用戶端的一般順序中的封包。



| 回應封包                                      | 目的                                                                                                                                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ping 的 Ack](ack-for-ping.md)                     | 認可 [Ping](ping.md) 要求。                                                                                                                                                  |
| [Create-Session 的 Ack](ack-for-create-session.md) | 認可 [建立會話](create-session.md) 的要求，並傳回 BITS 用戶端在所有後續要求中用來識別此檔案傳輸會話的會話識別碼。 |
| [適用于片段的 Ack](ack-for-fragment.md)             | 認可 [片段](fragment.md) 要求，並將片段寫入伺服器上的上傳檔案。                                                                                 |
| [確認是否已關閉會話](ack-for-close-session.md)   | 認可「 [關閉會話](close-session.md) 」要求，並釋放與該會話相關聯的所有資源。                                                                         |
| [Ack 以進行取消-會話](ack-for-cancel-session.md) | 認可 [取消會話](cancel-session.md) 的要求，並釋放與會話相關聯的所有資源。                                                                       |



 

 

 




