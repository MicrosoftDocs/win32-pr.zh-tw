---
description: 在第一個 Wsock32.dll （32位版本的 Windows 通訊端1.1）中，通訊端函式會以預設設定的重迭屬性來建立通訊端。
ms.assetid: 2ebf71fd-fcb3-4f2f-bf52-14cd13af012f
title: 通訊端之重迭屬性的預設狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bc46fbf08731b0f73d841291f6815b43d02785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113088"
---
# <a name="default-state-for-a-sockets-overlapped-attribute"></a>通訊端之重迭屬性的預設狀態

在第一個 Wsock32.dll （32位版本的 Windows 通訊端1.1）中， [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 函式會以預設設定的重迭屬性來建立通訊端。 為了確保與目前部署 Wsock32.dll 的相容性，這也會持續適用于 Windows 通訊端2。 也就是說，使用 **socket** 函式建立的 Windows 通訊端2通訊端將會有重迭的屬性。 不過，為了與 Windows API 的其餘部分相容，使用 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) 建立的通訊端不會有重迭的屬性。 只有在設定 WSA 旗標重迭位時，才會套用此屬性 \_ \_ 。

 

 



