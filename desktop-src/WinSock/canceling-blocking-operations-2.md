---
description: 執行緒隨時都可以呼叫 WSAIsBlocking 來判斷封鎖呼叫是否正在進行中。
ms.assetid: 6213ded4-feab-404f-86a0-3db9a0a42769
title: 取消封鎖作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5064948fe7c1c1262acb9f4f8ef25a3ad3e721e77a188f313541595ef75f9ce9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030688"
---
# <a name="canceling-blocking-operations"></a>取消封鎖作業

執行緒隨時都可以呼叫 [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) 來判斷封鎖呼叫是否正在進行中。  (此函式會在 Windows 通訊端1.1 相容性填充碼內執行，因此不會有 SPI 對應項。只有在虛擬封鎖（而不是真正的封鎖）正在由服務提供者運用時，才有可能發生這種情況 ) 。 必要時，可以隨時呼叫 [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) ，以取消任何目前的虛擬封鎖作業。

 

 
