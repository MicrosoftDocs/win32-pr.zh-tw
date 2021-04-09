---
title: 藍牙和 getsockopt
description: 藍牙會使用 getsockopt 函數來查詢與伺服器通道或連接相關聯的各種參數。
ms.assetid: 9593fd6c-b55d-45d8-a9d9-87ebcd09d1bd
keywords:
- Bluetooth
- getsockopt
- 藍牙和 getsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dede19b27eea39b7d1e778b3e92312a5e148c0ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682623"
---
# <a name="bluetooth-and-getsockopt"></a>藍牙和 getsockopt

藍牙會使用 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 函數來查詢與伺服器通道或連接相關聯的各種參數。 使用 **getsockopt** 搭配藍牙有下列需求：

-   [**Getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)的 *s* 參數必須是有效的藍牙通訊端。
-   [**Getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)的 *level* 參數必須是 SOL \_ RFCOMM。

如需可用藍牙通訊端選項的清單，請參閱 [藍牙和通訊端選項](bluetooth-and-socket-options.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> </dl>

 

 