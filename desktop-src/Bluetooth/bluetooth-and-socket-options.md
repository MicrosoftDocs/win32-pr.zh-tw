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
# <a name="bluetooth-and-socket-options"></a><span data-ttu-id="a7fcf-104">藍牙和通訊端選項</span><span class="sxs-lookup"><span data-stu-id="a7fcf-104">Bluetooth and Socket Options</span></span>

<span data-ttu-id="a7fcf-105">適用于 Windows 的 Bluetooth 支援下列通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-105">Bluetooth for Windows supports the following socket options.</span></span> <span data-ttu-id="a7fcf-106">您可以分別使用 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 和 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 函數來設定和查詢通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-106">Socket options are set and queried using the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) and [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) functions, respectively.</span></span> <span data-ttu-id="a7fcf-107">下列所有選項都可以搭配 **setsockopt** 函式使用，但只有 **SO \_ BTH \_ MTU** 選項可以搭配 **getsockopt** 函式使用。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-107">All of the following options can be used with the **setsockopt** function, but only the **SO\_BTH\_MTU** option is available for use with the **getsockopt** function.</span></span>

<span data-ttu-id="a7fcf-108">使用藍牙通訊端選項時需要下列設定：</span><span class="sxs-lookup"><span data-stu-id="a7fcf-108">The following settings are required for working with Bluetooth socket options:</span></span>

-   <span data-ttu-id="a7fcf-109">*S* 參數必須是藍牙通訊端。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-109">The *s* parameter must be a Bluetooth socket.</span></span>
-   <span data-ttu-id="a7fcf-110">*Level* 參數必須是 **SOL \_ RFCOMM**。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-110">The *level* parameter must be **SOL\_RFCOMM**.</span></span>

## <a name="so_bth_authenticate"></a><span data-ttu-id="a7fcf-111">\_BTH \_ 驗證</span><span class="sxs-lookup"><span data-stu-id="a7fcf-111">SO\_BTH\_AUTHENTICATE</span></span>

<span data-ttu-id="a7fcf-112">針對已中斷連線的通訊端， **\_ BTH \_** authentication 會指定需要驗證才能讓 [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) 或 [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) 作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-112">For disconnected sockets, the **SO\_BTH\_AUTHENTICATE** specifies that authentication is required for a [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) or [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) operation to complete successfully.</span></span> <span data-ttu-id="a7fcf-113">如果兩部 Bluetooth 裝置先前未經過驗證，則設定此通訊端選項會主動在連線建立期間起始驗證。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-113">Setting this socket option actively initiates authentication during connection establishment, if the two Bluetooth devices were not previously authenticated.</span></span> <span data-ttu-id="a7fcf-114">金鑰交換的使用者介面（如有必要）是由應用程式內容外的作業系統提供。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-114">The user interface for passkey exchange, if necessary, is provided by the operating system outside the application context.</span></span>

<span data-ttu-id="a7fcf-115">針對需要驗證的傳出連接，如果驗證失敗， [**連接**](/windows/desktop/api/winsock2/nf-winsock2-connect) 作業會失敗並出現 **WSAEACCES** 。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-115">For outgoing connections that require authentication, the [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) operation fails with **WSAEACCES** if authentication is not successful.</span></span> <span data-ttu-id="a7fcf-116">在回應中，應用程式可能會提示使用者在連線前先驗證兩部藍牙裝置。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-116">In response, the application may prompt the user to authenticate the two Bluetooth devices before connection.</span></span>

<span data-ttu-id="a7fcf-117">針對連入連線，如果無法建立驗證並傳回 **WSAEHOSTDOWN** 錯誤，則會拒絕連線。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-117">For incoming connections, the connection is rejected if authentication cannot be established and returns a **WSAEHOSTDOWN** error.</span></span> <span data-ttu-id="a7fcf-118">如需有關驗證 Bluetooth 裝置的詳細資訊，請參閱 [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-118">For more information about authenticating Bluetooth devices, see [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice).</span></span>

<span data-ttu-id="a7fcf-119">針對 **\_ BTH \_ 驗證** 通訊端選項， *optval* 是指向 ULONG bAuthenticate 的指標，且必須為 **TRUE**。 *optlen* 相當於 "SIZEOF (ULONG) "。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-119">For the **SO\_BTH\_AUTHENTICATE** socket option, *optval* is a pointer to ULONG bAuthenticate and must be **TRUE**; *optlen* is equivalent to "sizeof(ULONG)".</span></span>

<span data-ttu-id="a7fcf-120">**WINDOWS XP SP2： \_BTH \_** authentication 會開始驗證連接的通訊端，並在連線的通訊端連接時強制執行驗證。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-120">**Windows XP with SP2:  SO\_BTH\_AUTHENTICATE** starts authentication for connected sockets, and forces authentication upon connection for unconnected sockets.</span></span> <span data-ttu-id="a7fcf-121">若為連入連接，如果無法執行驗證，則會拒絕連線。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-121">For incoming connections, the connection is rejected if authentication cannot be performed.</span></span>

## <a name="so_bth_encrypt"></a><span data-ttu-id="a7fcf-122">\_BTH \_ 加密</span><span class="sxs-lookup"><span data-stu-id="a7fcf-122">SO\_BTH\_ENCRYPT</span></span>

<span data-ttu-id="a7fcf-123">在未連線的通訊端上， **\_ BTH \_ ENCRYPT** 通訊端選項會強制加密以建立連線。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-123">On unconnected sockets, the **SO\_BTH\_ENCRYPT** socket option enforces encryption to establish a connection.</span></span> <span data-ttu-id="a7fcf-124">加密僅適用于已驗證的連接。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-124">Encryption is only available for authenticated connections.</span></span> <span data-ttu-id="a7fcf-125">針對連入連線，無法建立加密的連線會自動被拒絕，並傳回 **WSAEHOSTDOWN** 做為錯誤。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-125">For incoming connections, a connection for which encryption cannot be established is automatically rejected and returns **WSAEHOSTDOWN** as the error.</span></span> <span data-ttu-id="a7fcf-126">若為傳出連接，如果無法建立加密， [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) 函式會失敗並出現 **WSAEACCES** 。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-126">For outgoing connections, the [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) function fails with **WSAEACCES** if encryption cannot be established.</span></span> <span data-ttu-id="a7fcf-127">在回應中，應用程式可能會提示使用者在連線前先驗證兩部藍牙裝置。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-127">In response, the application may prompt the user to authenticate the two Bluetooth devices before connection.</span></span> <span data-ttu-id="a7fcf-128">如需有關驗證 Bluetooth 裝置的詳細資訊，請參閱 [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-128">For more information about authenticating Bluetooth devices, see [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice).</span></span>

<span data-ttu-id="a7fcf-129">針對 \_ BTH \_ ENCRYPT 通訊端選項， *OPTVAL* 是指向 ULONG **bEncrypt** 的指標，且必須為 **TRUE**; *optlen* 相當於 SIZEOF (ULONG) 。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-129">For the SO\_BTH\_ENCRYPT socket option, *optval* is a pointer to ULONG **bEncrypt** and must be **TRUE**; *optlen* is equivalent to sizeof(ULONG).</span></span>

<span data-ttu-id="a7fcf-130">**WINDOWS XP SP2：** 針對已連線和已驗證的通訊端 **， \_ BTH \_** encryption 會開始加密。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-130">**Windows XP with SP2:** For a socket that is connected and authenticated, **SO\_BTH\_ENCRYPT** starts encryption.</span></span>

## <a name="so_bth_mtu"></a><span data-ttu-id="a7fcf-131">\_BTH \_ MTU</span><span class="sxs-lookup"><span data-stu-id="a7fcf-131">SO\_BTH\_MTU</span></span>

<span data-ttu-id="a7fcf-132">**SO \_ BTH \_ MTU** 通訊端選項是主要用於驗證的 advanced 選項。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-132">The **SO\_BTH\_MTU** socket option is an advanced option used primarily for validation.</span></span> <span data-ttu-id="a7fcf-133">**SO \_ BTH \_ MTU** 選項會取得或設定預設的 RFCOMM mtu (傳輸單位) 的最大傳輸單位，以與 RFCOMM 通訊協定預設值不同的值進行連接協調。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-133">The **SO\_BTH\_MTU** option obtains or sets default RFCOMM MTU (maximum transmission unit) for connection negotiation to a value different than the RFCOMM protocol-default value.</span></span>

<span data-ttu-id="a7fcf-134">由於 RFCOMM MTU 受到基礎 L2CAP MTU 和通訊協定和應用程式最小值和最大值所影響， **因此， \_ BTH \_ MTU** 的預設值只是與遠端對等互連的起點，而最終的協商 mtu 可能會因預設值而異。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-134">Because RFCOMM MTU is affected by the underlying L2CAP MTU, and protocol and application minimums and maximums, the default value for **SO\_BTH\_MTU** is only a starting point for negotiation with the remote peer, and the final negotiated MTU is likely to vary from the default.</span></span> <span data-ttu-id="a7fcf-135">設定 **SO \_ BTH \_ MTU** 值可能會對輸送量造成負面影響，因此任何修改都應該以基礎藍牙通訊協定的知識來執行。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-135">Setting the **SO\_BTH\_MTU** value may negatively affect throughput, and as such, any modification should be performed with knowledge of the underlying Bluetooth protocol.</span></span>

<span data-ttu-id="a7fcf-136">您可以在已連線的通訊端上執行 **SO \_ BTH \_ MTU** 通訊端選項，但如果協商已完成，就不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-136">The **SO\_BTH\_MTU** socket option can be performed on connected sockets, but has no effect if the negotiation has already completed.</span></span> <span data-ttu-id="a7fcf-137">在接聽的 (server) 通訊端上進行設定不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-137">Setting it on the listening (server) socket has no effect.</span></span>

<span data-ttu-id="a7fcf-138">應用程式可以在單一通訊端呼叫中傳送或接收的資料量不會受到 MTU 的影響;MTU 只會影響基礎 Windows 通訊端服務提供者如何分割傳輸的封包。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-138">The amount of data that an application can send or receive in a single socket call is not affected by the MTU; MTU only affects how the underlying Windows Sockets service provider segments packets for transport.</span></span> <span data-ttu-id="a7fcf-139">建議的 MTU 和最終協商的 MTU 都必須介於 **RFCOMM \_ MIN \_ mtu** 與 **RFCOMM \_ MAX \_ mtu** 之間，如 Ws2bth .h 標頭檔中所定義。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-139">Both the proposed MTU and the MTU ultimately negotiated must be between **RFCOMM\_MIN\_MTU** and **RFCOMM\_MAX\_MTU**, as defined in the Ws2bth.h header file.</span></span>

<span data-ttu-id="a7fcf-140">針對 **SO \_ BTH \_ mtu** 通訊端選項， *optval* 是指向 ULONG MTU 的指標; *optlen* 相當於 "SIZEOF (ULONG) "。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-140">For the **SO\_BTH\_MTU** socket option, *optval* is a pointer to ULONG mtu; *optlen* is equivalent to "sizeof(ULONG)".</span></span>

## <a name="so_bth_mtu_max"></a><span data-ttu-id="a7fcf-141">\_BTH \_ MTU \_ MAX</span><span class="sxs-lookup"><span data-stu-id="a7fcf-141">SO\_BTH\_MTU\_MAX</span></span>

<span data-ttu-id="a7fcf-142">**SO \_ BTH \_ MTU \_ MAX** socket 選項是主要用於驗證的 advanced 選項。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-142">The **SO\_BTH\_MTU\_MAX** socket option is an advanced option used primarily for validation.</span></span> <span data-ttu-id="a7fcf-143">**SO \_ BTH \_ mtu \_ MAX** 通訊端選項會將最大的 RFCOMM mtu 設定為連線協商 (的傳輸單位) 上限。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-143">The **SO\_BTH\_MTU\_MAX** socket option sets the maximum RFCOMM MTU (maximum transmission unit) for connection negotiation.</span></span> <span data-ttu-id="a7fcf-144">RFCOMM MTU 等於或大於此值的連接會在 [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) / [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept)進程期間失敗。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-144">Connections with an RFCOMM MTU equal to or greater than this value fail during the [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect)/[**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) process.</span></span> <span data-ttu-id="a7fcf-145">連接的通訊端可以設定此通訊端選項，如果協商已完成，它就不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-145">While setting this socket option is allowed for a connected socket, it has no effect if the negotiation has completed.</span></span> <span data-ttu-id="a7fcf-146">在接聽通訊端上設定此通訊端選項，會傳播所有連入連線的值。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-146">Setting this socket option on a listening socket propagates the value for all incoming connections.</span></span> <span data-ttu-id="a7fcf-147">最大 MTU 值必須介於 **RFCOMM \_ MIN \_ mtu** 與 **RFCOMM \_ MAX \_ mtu** 之間，如 Ws2bth .h 標頭檔中所定義。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-147">The MAX MTU value must be between **RFCOMM\_MIN\_MTU** and **RFCOMM\_MAX\_MTU**, as defined in the Ws2bth.h header file.</span></span>

<span data-ttu-id="a7fcf-148">針對「 **\_ BTH \_ MTU \_ 最大值** 通訊端」選項， *optval* 是指向 ULONG 最大 mtu 的指標 \_ ; *optlen* 相當於 "SIZEOF (ULONG) "。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-148">For the **SO\_BTH\_MTU\_MAX** socket option, *optval* is a pointer to ULONG max\_mtu; *optlen* is equivalent to "sizeof(ULONG)".</span></span>

## <a name="so_bth_mtu_min"></a><span data-ttu-id="a7fcf-149">\_BTH \_ MTU \_ MIN</span><span class="sxs-lookup"><span data-stu-id="a7fcf-149">SO\_BTH\_MTU\_MIN</span></span>

<span data-ttu-id="a7fcf-150">**SO \_ BTH \_ MTU \_ MIN** socket 選項是主要用於驗證的 advanced 選項。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-150">The **SO\_BTH\_MTU\_MIN** socket option is an advanced option used primarily for validation.</span></span> <span data-ttu-id="a7fcf-151">**SO \_ BTH \_ mtu \_ MIN** 通訊端選項會將最小的 RFCOMM mtu 設定為連線協商 (的最大傳輸單位) 。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-151">The **SO\_BTH\_MTU\_MIN** socket option sets the minimum RFCOMM MTU (maximum transmission unit) for connection negotiation.</span></span> <span data-ttu-id="a7fcf-152">RFCOMM MTU 小於此值的連接會在 [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) / [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept)進程期間失敗。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-152">Connections with an RFCOMM MTU smaller than this value fail during the [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect)/[**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) process.</span></span> <span data-ttu-id="a7fcf-153">連接的通訊端可以設定此通訊端選項，如果協商已完成，它就不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-153">While setting this socket option is allowed for a connected socket, it has no effect if the negotiation has completed.</span></span> <span data-ttu-id="a7fcf-154">在接聽通訊端上設定此通訊端選項，會傳播所有連入連線的值。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-154">Setting this socket option on a listening socket propagates the value for all incoming connections.</span></span>

<span data-ttu-id="a7fcf-155">只有接聽通訊端可以向下修改 MTU，因此如果連接通訊端所提議的值小於在接聽通訊端上針對 **\_ BTH \_ MTU \_ MIN** 設定的值，則會拒絕連接。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-155">Only a listening socket can revise the MTU downward, therefore if the value proposed by the connecting socket is less than the value set for **SO\_BTH\_MTU\_MIN** on the listening socket, the connection is refused.</span></span> <span data-ttu-id="a7fcf-156">最小 MTU 必須介於 **RFCOMM \_ MIN \_ mtu** 與 **RFCOMM \_ MAX \_ mtu** 之間，如 Ws2bth .h 標頭檔中所定義。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-156">The minimum MTU must be between **RFCOMM\_MIN\_MTU** and **RFCOMM\_MAX\_MTU**, as defined in the Ws2bth.h header file.</span></span>

<span data-ttu-id="a7fcf-157">針對 SO \_ BTH \_ mtu \_ min socket 選項， *optval* 是指向 ULONG 最小 mtu 的指標 \_ ; *optlen* 相當於 "SIZEOF (ULONG) "。</span><span class="sxs-lookup"><span data-stu-id="a7fcf-157">For the SO\_BTH\_MTU\_MIN socket option, *optval* is a pointer to ULONG min\_mtu; *optlen* is equivalent to "sizeof(ULONG)".</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7fcf-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="a7fcf-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7fcf-159">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="a7fcf-159">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="a7fcf-160">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="a7fcf-160">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="a7fcf-161">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="a7fcf-161">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="a7fcf-162">**BluetoothAuthenticateDevice**</span><span class="sxs-lookup"><span data-stu-id="a7fcf-162">**BluetoothAuthenticateDevice**</span></span>](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)
</dt> <dt>

[<span data-ttu-id="a7fcf-163">**連線**</span><span class="sxs-lookup"><span data-stu-id="a7fcf-163">**connect**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[<span data-ttu-id="a7fcf-164">**接受**</span><span class="sxs-lookup"><span data-stu-id="a7fcf-164">**accept**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 