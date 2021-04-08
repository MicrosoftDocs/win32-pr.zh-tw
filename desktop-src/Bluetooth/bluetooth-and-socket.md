---
title: 藍牙和通訊端
description: 建立傳入或傳出連接的通訊端。
ms.assetid: 21b9cf1f-1a85-4a4b-9557-faa4f32c3696
keywords:
- 藍牙藍牙
- 通訊端藍牙
- 藍牙和通訊端藍牙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2c2085ee0c61941bab93ed25dd86f5c102d0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682445"
---
# <a name="bluetooth-and-socket"></a>藍牙和通訊端

[**通訊端**](/windows/desktop/api/winsock2/nf-winsock2-socket)函式會建立傳入或傳出連線的通訊端。：

若要使用藍牙建立通訊端，請使用下列設定：

-   針對 Bluetooth 通訊端， [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket)函式的 *af* 參數一律設定為 **af \_ BTH** 。
-   [**通訊端**](/windows/desktop/api/winsock2/nf-winsock2-socket)函式的 *型* 別參數一律是 **SOCK \_ 資料流程**;**SOCK \_** 藍牙不支援 DGRAM 通訊端。
-   針對 *通訊協定* 參數， **BTHPROTO \_ RFCOMM** 是支援的通訊協定。

如需詳細資訊，請參閱 [Windows 通訊端](/windows/desktop/WinSock/windows-sockets-start-page-2)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**插座**](/windows/desktop/api/winsock2/nf-winsock2-socket)
</dt> </dl>

 

 