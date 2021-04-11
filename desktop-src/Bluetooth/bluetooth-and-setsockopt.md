---
title: 藍牙和 setsockopt
description: 藍牙使用 setsockopt 函式來設定與伺服器通道或連接相關聯的各種參數。
ms.assetid: ab78baed-5556-4d7b-88a6-e3ceb93afa8c
keywords:
- Bluetooth
- setsockopt
- 藍牙和 setsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 943839a49788b76e597596aee9cba65fa4b8d30d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315343"
---
# <a name="bluetooth-and-setsockopt"></a>藍牙和 setsockopt

藍牙使用 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函式來設定與伺服器通道或連接相關聯的各種參數。 使用 **setsockopt** 搭配藍牙有下列需求：

-   [**Setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)的 *s* 參數必須是有效的藍牙通訊端。
-   [**Setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)的 *level* 參數必須是 SOL \_ RFCOMM。

如需可用藍牙通訊端選項的清單，請參閱 [藍牙和通訊端選項](bluetooth-and-socket-options.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 