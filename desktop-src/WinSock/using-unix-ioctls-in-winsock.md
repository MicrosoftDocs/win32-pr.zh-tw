---
description: 使用命令 SIO \_ 取得介面清單，以 WSAIoctl 和 WSPIoctl 函式的形式支援大多數 UNIX 實作為的 SIOCGIFCONF 命令 \_ \_ 。 此命令會傳回已設定之介面及其參數的清單。
ms.assetid: c5028dae-052a-444c-837c-cd8d6d901b6c
title: 在 Winsock 中使用 UNIX Ioctls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da517adb6480a1bd20100a3d9a6d0896f544c1b541ce547a0f76e5c88aa24210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558860"
---
# <a name="using-unix-ioctls-in-winsock"></a>在 Winsock 中使用 UNIX Ioctls

使用命令 **SIO \_ 取得 \_ 介面 \_ 清單**，以 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)和 [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))函式的形式支援大多數 UNIX 實作為的 **SIOCGIFCONF** 命令。 此命令會傳回已設定之介面及其參數的清單。

> [!Note]  
> 此命令的支援是 Windows 通訊端2相容 tcp/ip 服務提供者的必要項。

 

參數 *lpvOutBuffer* 會指向緩衝區，而 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 和 [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) 會在其中儲存介面的相關資訊。 您可以根據 *lpcbBytesReturned* 中傳回的輸出緩衝區實際長度，判斷 *lpvOutBuffer*) 中所傳回之結構的介面數目 (。

 

 
