---
title: 藍牙和通訊端選項
description: 適用于 Windows 的 Bluetooth 支援下列通訊端選項。
ms.assetid: e2e305c2-e749-4566-8e24-c07a7a29c612
keywords:
- 藍牙和通訊端選項藍牙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84040a98c3dae1fec292e4f0a7086f11d1ee546c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933328"
---
# <a name="bluetooth-and-socket-options"></a>藍牙和通訊端選項

適用于 Windows 的 Bluetooth 支援下列通訊端選項。 您可以分別使用 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 和 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 函數來設定和查詢通訊端選項。 下列所有選項都可以搭配 **setsockopt** 函式使用，但只有 **SO \_ BTH \_ MTU** 選項可以搭配 **getsockopt** 函式使用。

使用藍牙通訊端選項時需要下列設定：

-   *S* 參數必須是藍牙通訊端。
-   *Level* 參數必須是 **SOL \_ RFCOMM**。

## <a name="so_bth_authenticate"></a>\_BTH \_ 驗證

針對已中斷連線的通訊端， **\_ BTH \_** authentication 會指定需要驗證才能讓 [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) 或 [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) 作業順利完成。 如果兩部 Bluetooth 裝置先前未經過驗證，則設定此通訊端選項會主動在連線建立期間起始驗證。 金鑰交換的使用者介面（如有必要）是由應用程式內容外的作業系統提供。

針對需要驗證的傳出連接，如果驗證失敗， [**連接**](/windows/desktop/api/winsock2/nf-winsock2-connect) 作業會失敗並出現 **WSAEACCES** 。 在回應中，應用程式可能會提示使用者在連線前先驗證兩部藍牙裝置。

針對連入連線，如果無法建立驗證並傳回 **WSAEHOSTDOWN** 錯誤，則會拒絕連線。 如需有關驗證 Bluetooth 裝置的詳細資訊，請參閱 [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)。

針對 **\_ BTH \_ 驗證** 通訊端選項， *optval* 是指向 ULONG bAuthenticate 的指標，且必須為 **TRUE**。 *optlen* 相當於 "SIZEOF (ULONG) "。

**WINDOWS XP SP2： \_BTH \_** authentication 會開始驗證連接的通訊端，並在連線的通訊端連接時強制執行驗證。 若為連入連接，如果無法執行驗證，則會拒絕連線。

## <a name="so_bth_encrypt"></a>\_BTH \_ 加密

在未連線的通訊端上， **\_ BTH \_ ENCRYPT** 通訊端選項會強制加密以建立連線。 加密僅適用于已驗證的連接。 針對連入連線，無法建立加密的連線會自動被拒絕，並傳回 **WSAEHOSTDOWN** 做為錯誤。 若為傳出連接，如果無法建立加密， [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) 函式會失敗並出現 **WSAEACCES** 。 在回應中，應用程式可能會提示使用者在連線前先驗證兩部藍牙裝置。 如需有關驗證 Bluetooth 裝置的詳細資訊，請參閱 [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)。

針對 \_ BTH \_ ENCRYPT 通訊端選項， *OPTVAL* 是指向 ULONG **bEncrypt** 的指標，且必須為 **TRUE**; *optlen* 相當於 SIZEOF (ULONG) 。

**WINDOWS XP SP2：** 針對已連線和已驗證的通訊端 **， \_ BTH \_** encryption 會開始加密。

## <a name="so_bth_mtu"></a>\_BTH \_ MTU

**SO \_ BTH \_ MTU** 通訊端選項是主要用於驗證的 advanced 選項。 **SO \_ BTH \_ MTU** 選項會取得或設定預設的 RFCOMM mtu (傳輸單位) 的最大傳輸單位，以與 RFCOMM 通訊協定預設值不同的值進行連接協調。

由於 RFCOMM MTU 受到基礎 L2CAP MTU 和通訊協定和應用程式最小值和最大值所影響， **因此， \_ BTH \_ MTU** 的預設值只是與遠端對等互連的起點，而最終的協商 mtu 可能會因預設值而異。 設定 **SO \_ BTH \_ MTU** 值可能會對輸送量造成負面影響，因此任何修改都應該以基礎藍牙通訊協定的知識來執行。

您可以在已連線的通訊端上執行 **SO \_ BTH \_ MTU** 通訊端選項，但如果協商已完成，就不會有任何作用。 在接聽的 (server) 通訊端上進行設定不會有任何作用。

應用程式可以在單一通訊端呼叫中傳送或接收的資料量不會受到 MTU 的影響;MTU 只會影響基礎 Windows 通訊端服務提供者如何分割傳輸的封包。 建議的 MTU 和最終協商的 MTU 都必須介於 **RFCOMM \_ MIN \_ mtu** 與 **RFCOMM \_ MAX \_ mtu** 之間，如 Ws2bth .h 標頭檔中所定義。

針對 **SO \_ BTH \_ mtu** 通訊端選項， *optval* 是指向 ULONG MTU 的指標; *optlen* 相當於 "SIZEOF (ULONG) "。

## <a name="so_bth_mtu_max"></a>\_BTH \_ MTU \_ MAX

**SO \_ BTH \_ MTU \_ MAX** socket 選項是主要用於驗證的 advanced 選項。 **SO \_ BTH \_ mtu \_ MAX** 通訊端選項會將最大的 RFCOMM mtu 設定為連線協商 (的傳輸單位) 上限。 RFCOMM MTU 等於或大於此值的連接會在 [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) / [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept)進程期間失敗。 連接的通訊端可以設定此通訊端選項，如果協商已完成，它就不會有任何作用。 在接聽通訊端上設定此通訊端選項，會傳播所有連入連線的值。 最大 MTU 值必須介於 **RFCOMM \_ MIN \_ mtu** 與 **RFCOMM \_ MAX \_ mtu** 之間，如 Ws2bth .h 標頭檔中所定義。

針對「 **\_ BTH \_ MTU \_ 最大值** 通訊端」選項， *optval* 是指向 ULONG 最大 mtu 的指標 \_ ; *optlen* 相當於 "SIZEOF (ULONG) "。

## <a name="so_bth_mtu_min"></a>\_BTH \_ MTU \_ MIN

**SO \_ BTH \_ MTU \_ MIN** socket 選項是主要用於驗證的 advanced 選項。 **SO \_ BTH \_ mtu \_ MIN** 通訊端選項會將最小的 RFCOMM mtu 設定為連線協商 (的最大傳輸單位) 。 RFCOMM MTU 小於此值的連接會在 [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) / [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept)進程期間失敗。 連接的通訊端可以設定此通訊端選項，如果協商已完成，它就不會有任何作用。 在接聽通訊端上設定此通訊端選項，會傳播所有連入連線的值。

只有接聽通訊端可以向下修改 MTU，因此如果連接通訊端所提議的值小於在接聽通訊端上針對 **\_ BTH \_ MTU \_ MIN** 設定的值，則會拒絕連接。 最小 MTU 必須介於 **RFCOMM \_ MIN \_ mtu** 與 **RFCOMM \_ MAX \_ mtu** 之間，如 Ws2bth .h 標頭檔中所定義。

針對 SO \_ BTH \_ mtu \_ min socket 選項， *optval* 是指向 ULONG 最小 mtu 的指標 \_ ; *optlen* 相當於 "SIZEOF (ULONG) "。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)
</dt> <dt>

[**連線**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**接受**](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 