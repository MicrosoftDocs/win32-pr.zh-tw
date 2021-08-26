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
ms.openlocfilehash: 5afaf61e307ce8d5001c2ba5402607b63b1ad6d19317aee044d7a2cac31259b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004298"
---
# <a name="bluetooth-and-socket"></a>藍牙和通訊端

[**通訊端**](/windows/desktop/api/winsock2/nf-winsock2-socket)函式會建立傳入或傳出連線的通訊端。：

若要使用藍牙建立通訊端，請使用下列設定：

-   針對藍牙通訊端， [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket)函式的 *af* 參數一律設定為 **af \_ BTH** 。
-   [**通訊端**](/windows/desktop/api/winsock2/nf-winsock2-socket)函式的 *型* 別參數一律是 **SOCK \_ 資料流程**;**SOCK \_** 藍牙不支援 DGRAM 通訊端。
-   針對 *通訊協定* 參數， **BTHPROTO \_ RFCOMM** 是支援的通訊協定。

如需詳細資訊，請參閱[Windows 通訊端](/windows/desktop/WinSock/windows-sockets-start-page-2)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**插座**](/windows/desktop/api/winsock2/nf-winsock2-socket)
</dt> </dl>

 

 