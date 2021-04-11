---
description: 設定錯誤的防火牆可能會導致 WSD 應用程式失敗。
ms.assetid: eba61235-29b4-463a-b7c5-d34d3b39b095
title: 檢查介面卡和防火牆設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490909c9f3acdc3025e72350118f303bfdae73d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318927"
---
# <a name="inspecting-adapter-and-firewall-settings"></a>檢查介面卡和防火牆設定

設定錯誤的防火牆可能會導致 WSD 應用程式失敗。 本主題提供在 WSD 用戶端和主機無法在網路上看到彼此時，所要使用的一些疑難排解程式。 使用任何其他應用程式疑難排解程式之前，應該先檢查防火牆設定。

**檢查介面卡和防火牆設定**

1.  確認已啟用 **網路探索** 例外狀況。
2.  確認沒有任何應用程式特定的防火牆規則封鎖應用程式。
3.  明確啟用用於探索和中繼資料交換的埠。
4.  停用防火牆，然後重新測試應用程式。
    > [!Note]  
    > 完成此步驟之後，應重新啟用防火牆。

     

## <a name="verifying-that-the-network-discovery-exception-is-enabled"></a>確認已啟用網路探索例外狀況

如果有任何 WS-Discovery 的應用程式正在執行，則必須允許 **網路探索** 防火牆例外。

**若要啟用網路探索防火牆例外狀況**

1.  按一下 [ **開始**]，按一下 [ **執行**]，然後輸入 **firewall.cpl**。 這會開啟 **Windows 防火牆主控台** applet。
2.  選擇 [ **允許程式通過 Windows 防火牆**]。
3.  在 [ **例外** ] 索引標籤上，選取 [ **網路探索** ] 核取方塊。
4.  按一下 **[確定]** 關閉防火牆小程式。

進行此防火牆變更之後，請重新測試程式。 如果程式現在可順利運作，就會識別出問題的原因，而不需要進行進一步的疑難排解步驟。 否則，請移至下一個步驟。

## <a name="checking-for-application-specific-firewall-rules"></a>檢查應用程式特定的防火牆規則

Windows 防火牆的 Advanced 設定可以發生在 Microsoft Management Control (MMC) 嵌入式管理單元中，名為 [ **具有 Advanced Security 的 Windows 防火牆**]。 此嵌入式管理單元可以用來針對可疑的防火牆問題進行疑難排解。

開發人員可以使用「 [具有 Advanced 安全性的 Windows 防火牆](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) 」 api 來建立適用于其 WSD 應用程式的防火牆規則。 具體來說， [**INetFwRules**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrules)介面的 [**add**](/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrules-add)方法可以用來加入新的防火牆規則。 如果未正確建立防火牆規則，用戶端和主機可能無法在網路上看到彼此。

**檢查應用程式特定的防火牆規則**

1.  按一下 [ **開始**]，按一下 [ **執行**]，然後輸入 **wf**。
2.  尋找可能會封鎖流量的應用程式特定規則。 如需詳細資訊，請參閱 [具有 Advanced Security 的 Windows 防火牆-診斷和疑難排解工具](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc722062(v=ws.10)?ocid=fwlink)。
3.  移除應用程式特定的規則。

如果找不到特定應用程式的規則，請移至下一個步驟。 如果已找到並移除應用程式專屬的規則，請在進行防火牆變更之後，重新測試程式。 如果程式現在可順利運作，就會識別出問題的原因，而不需要進行進一步的疑難排解步驟。 否則，請移至下一個步驟。

## <a name="enabling-the-ports-used-for-discovery-and-metadata-exchange"></a>啟用用於探索和中繼資料交換的埠

WS-Discovery 使用 UDP 埠3702進行訊息交換。 此外，TCP 通訊埠5357和5358有時也會用於中繼資料交換。 您可以使用在 [Windows 防火牆中開啟埠](https://windowshelp.microsoft.com/Windows/Help/4da18300-9044-47b6-9038-595c78db81ab1033.mspx)所述的程式，在防火牆上明確開啟這些埠。

進行此防火牆變更之後，請重新測試程式。 如果程式現在可順利運作，就會識別出問題的原因，而不需要進行進一步的疑難排解步驟。 否則，請移至下一個步驟。

## <a name="disabling-the-firewall"></a>停用防火牆

您可以停用 Windows 防火牆，以協助針對疑似問題進行疑難排解。 其他適用的防火牆 (例如路由器上的防火牆) 也可基於疑難排解目的而停用。 如需啟用和停用 Windows 防火牆的相關資訊，請參閱 [開啟或關閉 Windows 防火牆](https://windowshelp.microsoft.com/Windows/Help/bfe523a9-7eec-4d3f-add1-2f68b9cfa1c01033.mspx)。

停用任何適用的防火牆之後，請重新測試應用程式。 如果程式現在可順利運作，則防火牆會封鎖流量。 封鎖流量有幾個可能的原因。

-   應用程式特定的例外狀況會封鎖流量。 檢查應用程式特定的防火牆規則，如上所述。
-   裝置花太多時間回應 UDP 要求。 Windows 防火牆可能會在傳送初始要求之後，封鎖傳回超過4秒的 UDP 回應。 遵循 [使用泛型主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md) 所提供的程式，查看問題是否發生在4秒以內回應的主機，以繼續進行疑難排解。

如果在停用防火牆之後，應用程式仍失敗，則防火牆不會導致應用程式失敗。 重新啟用防火牆，並遵循 [使用一般主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md)的程式，繼續進行疑難排解。

疑難排解完成後，應該一律重新啟用防火牆。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WSDAPI 診斷程式](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[使用 WSDAPI 進行疑難排解的開始使用](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 
