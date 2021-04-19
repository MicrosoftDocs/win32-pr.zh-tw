---
description: Windows 通訊端 2 (適用于 multipoint 和多播的 Winsock) 介面元素。
ms.assetid: c6f704cf-031b-4714-9f07-2d7715a157a0
title: 適用于 Multipoint 和多播的 Windows 通訊端2介面元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86905fe19c5c4c603db488874039b7cc8a0b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977196"
---
# <a name="windows-sockets-2-interface-elements-for-multipoint-and-multicast"></a>適用于 Multipoint 和多播的 Windows 通訊端2介面元素

已併入 Windows 通訊端2以利用 multipoint 功能的機制可摘要如下：

-   [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構中有三個屬性位。
-   針對 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)的 *dwFlags* 參數定義的四個旗標。
-   一個函式 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)，用於將分葉節點新增至 multipoint 會話。
-   用於控制 multipoint 回送的兩個 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 命令代碼，以及多播傳輸的範圍。

下列各節將更詳細地說明這些介面元素：

-   [聯結 Multipoint 離開的語義](semantics-for-joining-multipoint-leaves-2.md)
-   [現有 Multipoint 通訊協定如何支援這些擴充功能](how-existing-multipoint-protocols-support-these-extensions-2.md)

 

 
