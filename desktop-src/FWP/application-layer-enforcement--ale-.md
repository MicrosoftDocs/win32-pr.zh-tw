---
title: '應用層強制 (ALE) '
description: ALE 是一組 Windows 的篩選平臺 (WFP) 用於可設定狀態之篩選的核心模式層。
ms.assetid: ffebd312-9220-476c-a4ba-28e2e8ac8879
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d74db5fdc231569f65c3b25cb630b306111aa5d6a7e3eb7faad743a5f74db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069468"
---
# <a name="application-layer-enforcement-ale"></a>應用層強制 (ALE) 

ALE 是一組 Windows 的篩選平臺 (WFP) 用於可設定狀態之篩選的核心模式層。

可設定狀態的篩選會追蹤網路連接的狀態，並只允許符合已知連接狀態的封包。 例如，從防火牆後方起始之 TCP 連線的可設定狀態篩選，只允許符合受保護的合作物件所傳送之先前傳出封包的傳入封包。

ALE 層中的篩選準則會授權輸入和輸出連線的建立、通訊埠指派、如 [**接聽 ()**](/windows/desktop/api/winsock2/nf-winsock2-listen)、原始通訊端建立和混合模式接收的通訊端作業。

ALE 層的流量是依每一連線或每個通訊端作業分類。 在非 ALE 層級，篩選準則只能針對每個封包分類流量。

ALE 層是唯一可用來根據應用程式識別（使用正規化的檔案名）或根據使用者身分識別（使用安全描述項）來篩選網路流量的 WFP 層。 如需有關 \_ \_ \_ 正規化檔案名的詳細資訊，請參閱 Windows 驅動程式套件 (WDK) 檔中的 FLT 檔案名資訊 (。 ) 

此外，使用 IPsec 保護連線時，也可以在遠端電腦身分識別和遠端使用者身分識別上執行 ALE 層級的篩選。 遠端電腦和使用者身分識別是從建立 IPsec 會話時所用的認證取得。

基於這個理由，強制執行 (例如「系統管理員」 ) 和/或哪個應用程式 (例如「Internet Explorer」 ) 的原則會在 ALE 層級撰寫。

ALE 提供原則的強制執行，例如「允許 Windows Messenger 所有存取網路，同時封鎖所有其他應用程式」。 在此範例中，當應用程式 "Messenger" 透過網路連線時，ALE 會攔截該事件，並判斷它是由 Messenger 起始，並查詢 WFP 篩選引擎來判斷是否應該允許該通訊端繼續進行。

> [!Note]  
> 由於真正的雙重 IP 通訊端本質，因此可能不會發生 IPv4 ALE 層的分類。 這是設計的，因為針對所有意圖和用途，通訊端是 IPv6 通訊端。 若要查看這類通訊端的 V4 流量，請使用 IPv6 對應位址在 V6 層建立篩選器。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ALE 層](ale-layers.md)
</dt> <dt>

[ALE 具狀態篩選](ale-stateful-filtering.md)
</dt> <dt>

[ALE 多播/廣播流量](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[ALE 重新授權](ale-re-authorization.md)
</dt> <dt>

[ALE Flow 自訂](ale-flow-customization.md)
</dt> </dl>

 

 