---
description: 執行緒隨時都可以呼叫 WSAIsBlocking 來判斷封鎖呼叫是否正在進行中。
ms.assetid: 6213ded4-feab-404f-86a0-3db9a0a42769
title: 取消封鎖作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 502870b8935dc97c1d6c3714808d1c6532780f7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973270"
---
# <a name="canceling-blocking-operations"></a>取消封鎖作業

執行緒隨時都可以呼叫 [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) 來判斷封鎖呼叫是否正在進行中。  (此函式會在 Windows 通訊端1.1 相容性填充碼內執行，因此不會有 SPI 對應項。 ) 顯然只有在虛擬封鎖（而不是真正的封鎖）由服務提供者所使用時，才可能發生這種情況。 必要時，可以隨時呼叫 [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) ，以取消任何目前的虛擬封鎖作業。

 

 
