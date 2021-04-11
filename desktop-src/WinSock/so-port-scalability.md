---
description: 啟用通訊端的本機埠擴充性。
ms.assetid: c5142baf-9e2d-4c06-8719-9090fd2d9487
title: 'SO_PORT_SCALABILITY (Ws2def) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565caeb472ac5cb15061d32b47a048a9a210885e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113004"
---
# <a name="so_port_scalability"></a>因此， \_ 埠擴充 \_ 性

**SO \_ 埠擴充 \_ 性** 通訊端選項可啟用通訊端的本機埠擴充性。

<dl> <dt>

<span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**因此， \_ 埠擴充 \_ 性**
</dt> <dd> <dl> <dt>

0x3006
</dt> <dt>



**如此埠的擴充 \_ \_ 性** 通訊端選項可讓本機通訊埠可透過針對本機電腦上不同的本機位址通訊埠配對，多次配置萬用字元埠，藉以達到本機埠的擴充性。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

注意：在同時 \_ 支援埠擴充 \_ 性和 \_ 重複使用 UNICASTPORT 的平臺上 \_ ，最好使用，以 \_ 重複使用 \_ UNICASTPORT。

由於本機埠的可用性有限，因此 Proxy 伺服器環境有擴充性問題。 解決此問題的方法之一是將更多 IP 位址新增至電腦。 不過，根據預設，搭配 [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) 函式使用的萬用字元埠會限制為本機電腦上動態埠範圍的大小 (最多64k 的埠，但在本機電腦上的 IP 位址數目通常較不) 。 解決此問題需要應用程式以埠保留或使用啟發學習法來維護其本身的埠集區。

為了避免每個需要擴充的應用程式都能管理自己的埠集區，並允許更大的擴充性，同時維持應用程式相容性，Windows Server 2008 引進了「 **\_ 埠擴充 \_ 性** 通訊端」選項，可協助您最大化萬用字元埠配置。 埠配置可讓應用程式針對每個唯一的本機位址和埠配對配置萬用字元埠，藉以達到最大效益。 因此，如果本機電腦有四個 IP 位址，則可以使用萬用字元系結函式要求配置最多 256 K [**個萬用字元埠**](/windows/desktop/api/winsock/nf-winsock-bind) (64 k 埠×4個 ip 位址) 。

在通訊端上設定 **SO \_ 埠 \_** 擴充通訊端選項，且對 [**指定的位址**](/windows/desktop/api/winsock/nf-winsock-bind) 和萬用字元埠進行系結函式的呼叫時 (*名稱* 參數設定為特定位址，埠為 0) ，Winsock 將配置指定位址的埠。 此配置會以本機電腦上的所有可能 IP 位址和埠/每個位址為基礎。 如果使用 [ **\_ 埠擴充 \_ 性** ] 選項來取得萬用字元埠，則無法由另一個通訊端配置該埠，而不需要使用 [ **埠擴充 \_ \_ 性** ] 選項。 這項限制是為了避免應用程式的回溯相容性問題，而這些應用程式無法重複使用萬用字元本機埠。 請注意，這表示使用的 **\_ 埠擴充 \_ 性** 取得大量埠的應用程式，可以使舊版的埠應用程式。 如果已針對至少一個位址取得 **\_ 埠擴充 \_ 性** 的所有可用暫時埠，則沒有通訊端選項，就無法再進行任何萬用字元配置。

若要有任何效果 [**，在呼叫**](/windows/desktop/api/winsock/nf-winsock-bind)系結函式之前，必須先設定 **SO 埠的擴充 \_ \_ 性** 選項。 在具有兩個位址的電腦上使用此方式的範例如下所示：

-   處理常式會呼叫 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 函數來建立通訊端。
-   呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函式，以啟用新建立之通訊端上的「 **\_ 埠擴充 \_ 性** 通訊端」選項。
-   呼叫[](/windows/desktop/api/winsock/nf-winsock-bind)系結函式，以便在其中一個本機電腦的 IP 位址和埠0上進行系結。
-   接著會呼叫 [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) 函式以連接到遠端 IP 位址。 應用程式會視需要使用通訊端。
-   [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket)函式是由相同的進程呼叫 (可能是不同的執行緒) 來建立第二個通訊端。
-   呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函式，以在新建立的第二通訊端上啟用「 **\_ 埠 \_** 擴充通訊端」選項。
-   使用本機電腦的第二個 IP 位址和埠0呼叫系 [**結函數。**](/windows/desktop/api/winsock/nf-winsock-bind) 即使先前已配置所有埠，此呼叫也會成功，因為本機電腦上有多個可用的 IP 位址，而且在相同的進程中，同時在這兩個通訊端上設定了 **\_ 埠 \_** 擴充通訊端選項。
-   接著會呼叫 [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) 函式以連接到遠端 IP 位址。 應用程式會視需要使用第二個通訊端。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Ws2def。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**SOL \_ 通訊端通訊端選項**](sol-socket-socket-options.md)
</dt> <dt>

[**通訊端選項**](socket-options.md)
</dt> </dl>

 

 




