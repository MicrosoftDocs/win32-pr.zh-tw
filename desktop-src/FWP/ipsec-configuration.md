---
title: IPsec 設定
description: Windows篩選 platform (WFP) 是具有 Advanced Security Windows 防火牆的基礎平臺。
ms.assetid: d54b5caa-daea-4231-9909-7a8d388df661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34cf20fc8c95aafe3c387195b02468cec3ce884cc97287adde44a594305ee189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069010"
---
# <a name="ipsec-configuration"></a>IPsec 設定

Windows篩選 platform (WFP) 是具有 Advanced Security Windows 防火牆的基礎平臺。 WFP 可用來設定網路篩選規則，其中包括使用 IPsec 保護網路流量的規則。 應用程式開發人員可以直接使用 WFP API 來設定 IPsec，以利用更細微的網路流量篩選模型，而不是透過 Microsoft Management Console (MMC) 嵌入式管理單元（適用于具有 Advanced Security 的 Windows 防火牆）所公開的模型。

## <a name="what-is-ipsec"></a>什麼是 IPsec

網際網路通訊協定安全性 (IPsec) 是一組安全性通訊協定，可用來跨網際網路傳輸 IP 封包。 IPsec 對於所有 IPv6 執行都是必要的，而針對 IPv4 則是選擇性的。

安全的 IP 流量有兩個選用的 IPsec 標頭，可識別套用至 IP 封包的密碼編譯保護類型，並包含解碼受保護封包的資訊。

封裝安全性承載 (ESP) 標頭是用來執行驗證和選擇性加密，以提供隱私權和保護以防止惡意修改。 它可用於流經 (NAT) 路由器的網路位址轉譯的流量。

驗證標頭 (AH) 僅用來保護執行驗證的惡意修改。 它無法用於流經 NAT 路由器的流量。

如需 IPsec 的詳細資訊，另請參閱：

<dl>

[IPsec 技術參考](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))  
</dl>

## <a name="what-is-ike"></a>什麼是 IKE

網際網路金鑰交換 (IKE) 是 IPsec 通訊協定集一部分的金鑰交換通訊協定。 IKE 是在設定安全連線時使用，並在不需要使用者介入的情況下完成安全的秘密金鑰和其他保護相關參數的交換。

如需有關 IKE 的詳細資訊，另請參閱：

<dl>

[網際網路金鑰交換](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))  
</dl>

## <a name="what-is-authip"></a>什麼是 AuthIP

驗證的網際網路通訊協定 (AuthIP) 是新的金鑰交換通訊協定，可依下列方式展開 IKE。

<dl> 雖然 IKE 只支援電腦驗證認證，但 AuthIP 也支援：

-   使用者認證： NTLM、Kerberos、憑證。
-   網路存取保護 (NAP) 健康情況憑證。
-   匿名認證，用於選擇性驗證。
-   認證的組合;例如，電腦和使用者 Kerberos 認證的組合。

  
AuthIP 具有驗證重試機制，可在連線失敗之前確認所有已設定的驗證方法。  
AuthIP 可以搭配安全通訊端使用，以執行以應用程式為基礎的 IPsec 安全流量。 它提供：

-   每一通訊端的驗證和加密。 如需詳細資訊，請參閱 [**WSASetSocketSecurity**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) 。
-   用戶端模擬。  (IPsec 會模擬建立通訊端所用的安全性內容。 ) 
-   輸入和輸出對等名稱驗證。 如需詳細資訊，請參閱 [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) 。

  
</dl>

如需 AuthIP 的詳細資訊，另請參閱：

<dl>

[Windows Vista 中的 AuthIP](https://www.microsoft.com/technet/community/columns/cableguy/cg0806.mspx)  
</dl>

## <a name="what-is-an-ipsec-policy"></a>什麼是 IPsec 原則

IPsec 原則是一組規則，可決定需要使用 IPsec 保護哪些類型的 IP 流量，以及如何保護該流量。 一次只能在一部電腦上使用一個 IPsec 原則。

若要深入瞭解如何執行 IPsec 原則，請開啟 [本機安全性原則] MMC 嵌入式管理單元， (secpol.msc]) 中按 F1 鍵顯示 [說明]，然後選取 [目錄] 中的 [建立和使用 IPsec 原則]。

如需 IPsec 原則的詳細資訊，另請參閱：

<dl>

[IPsec 原則概念總覽](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))  
[IPsec 原則的描述](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))  
</dl>

## <a name="how-to-use-wfp-to-configure-ipsec-policies"></a>如何使用 WFP 設定 IPsec 原則

Microsoft 的 ipsec 執行會使用 Windows 篩選平台來設定 ipsec 原則。 IPsec 原則是藉由在不同的 WFP 層級新增篩選準則來執行，如下所示。

-   在 FWPM \_ LAYER \_ IKEEXT \_ V {4 \| 6} 層新增篩選器，以指定在主要模式 (MM) 交換期間， (IKE/AuthIP) 的加密模組所使用的協商原則。 驗證方法和密碼編譯演算法是在這些層級指定。
-   在 FWPM \_ 層 \_ 中，IPSEC \_ V {4 \| 6} 層新增篩選器，以在快速模式 (QM) 和延伸模式 (EM) 交換時，指定加密模組所使用的協商原則。 IPsec 標頭 (AH/ESP) 和密碼編譯演算法是在這些層級指定。

    協商原則會指定為與篩選準則相關聯的原則提供者內容。 加密模組會根據流量特性列舉原則提供者內容，並取得要用於安全性協調的原則。

    > [!Note]  
    > 您可以使用 WFP API 來直接指定 (SAs) 的安全性關聯，進而忽略金鑰安全模組的協商原則。

     

-   在 FWPM \_ 層的 \_ 輸入 \_ 傳輸 \_ v {4 \| 6} 和 FWPM \_ 層 \_ 輸出 \_ 傳輸 \_ v {4 \| 6} 層中，會新增可叫用標注並決定應保護哪些流量流程的篩選準則。
-   在 FWPM \_ 層的 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6} 個層級新增篩選準則，以執行身分識別篩選和個別應用程式原則。

下圖說明各種 WFP 元件的互動，與 IPsec 作業有關。![使用 windows 篩選平臺進行 ipsec 設定](images/ipsec-configuration.jpg)

IPsec 一經設定，就會與 WFP 整合，並藉由提供資訊，以在應用層強制執行 (ALE) 授權層級的篩選準則，來擴充 WFP 篩選功能。 例如，IPsec 提供遠端使用者和遠端電腦身分識別，而 WFP 會在 ALE connect 和接受授權層級公開。 這項資訊可用於以 WFP 為基礎的防火牆執行，以進行更細緻的遠端身分識別授權。

以下是可能使用 IPsec 來執行的隔離原則範例：

-   FWPM \_ LAYER \_ IKEEXT \_ V {4 \| 6} 層– Kerberos 驗證。
-   FWPM \_ 層 \_ IPSEC \_ V {4 \| 6} 層– AH/sha-1。
-   FWPM \_ 圖層 \_ 輸入 \_ 傳輸 \_ v {4 \| 6} 和 FWPM \_ 層 \_ 輸出 \_ 傳輸 \_ v {4 \| 6} 層級-所有網路流量的協調探索。
-   FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6} 層-所有網路流量都需要 IPsec。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**WFP 層**
</dt> <dt>

[**篩選層識別碼**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[ALE 層](ale-layers.md)
</dt> <dt>

**使用 WFP API 執行的 IPsec 原則案例：**
</dt> <dt>

[傳輸模式](regular-transport-mode.md)
</dt> <dt>

[協商探索傳輸模式](negotiation-discovery-transport-mode.md)
</dt> <dt>

[界限模式中的協商探索傳輸模式](negotiation-discovery-transport-mode-in-boundary-mode.md)
</dt> <dt>

[Tunnel模式](tunnel-mode.md)
</dt> <dt>

[保證加密](guaranteed-encryption.md)
</dt> <dt>

[遠端身分識別授權](remote-identity-authorization.md)
</dt> <dt>

[手動 IPsec SAs](manual-ipsec-sas.md)
</dt> <dt>

[IKE/AuthIP 豁免](ike-exemptions.md)
</dt> <dt>

**IPsec 解決方案：**
</dt> <dt>

[伺服器及網域隔離](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))
</dt> </dl>

 

 