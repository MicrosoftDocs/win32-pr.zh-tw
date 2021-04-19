---
description: 大部分 UNIX 執行所提供的 SIOCGIFCONF 命令都支援使用命令 SIO \_ GET INTERFACE LIST 形式的 WSAIoctl 和 WSPIoctl 函數 \_ \_ 。 此命令會傳回已設定之介面及其參數的清單。
ms.assetid: c5028dae-052a-444c-837c-cd8d6d901b6c
title: 在 Winsock 中使用 UNIX Ioctls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b52c311ea8c5f67dc374503f00c3ca16c5d053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991872"
---
# <a name="using-unix-ioctls-in-winsock"></a>在 Winsock 中使用 UNIX Ioctls

大部分 UNIX 執行所提供的 **SIOCGIFCONF** 命令都支援使用命令 **SIO \_ GET \_ INTERFACE \_ LIST** 形式的 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)和 [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))函數。 此命令會傳回已設定之介面及其參數的清單。

> [!Note]  
> 對 Windows 通訊端2相容的 TCP/IP 服務提供者，此命令的支援是必要的。

 

參數 *lpvOutBuffer* 會指向緩衝區，而 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 和 [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) 會在其中儲存介面的相關資訊。 您可以根據 *lpcbBytesReturned* 中傳回的輸出緩衝區實際長度，判斷 *lpvOutBuffer*) 中所傳回之結構的介面數目 (。

 

 
