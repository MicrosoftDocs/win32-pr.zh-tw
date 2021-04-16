---
title: 關於 Windows Web 服務
description: Windows Web 服務 API 是多層式 API，如下所示。
ms.assetid: 6e8c23d1-c86b-432d-8e0c-e16982849239
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7546aaa72d58e43d7faefccf394a3e27756f4a96
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "104558046"
---
# <a name="about-windows-web-services"></a>關於 Windows Web 服務

Windows Web 服務 API 是多層式 API，如下所示：

![此圖顯示 Windows Web 服務 API 的圖層和跨層區域。](images/apistack.png)

WWSAPI 是多層式 API。 我們預期大部分的開發人員都是以以方法為基礎的程式設計模型為目標的服務模型。 在服務模型中，服務主機會提供伺服器端程式設計模型，而服務 Proxy 則提供用戶端程式設計模型。

每一層都會公開一組 Api 和類型，可搭配該層的 Api 使用。

## <a name="service-model"></a>服務模型

稱為「 [服務模型](service-model-layer-overview.md) 」的最上層層提供以方法為基礎的程式設計模型，而且是最容易使用的模型。 在服務模型中， [服務主機](service-host.md) 會提供伺服器端程式設計模型，而 [服務 Proxy](service-proxy.md) 則提供用戶端程式設計模型。 [內容](context.md) 會在服務模型內用來將相關的可用狀態傳遞給服務作業，並在叫用時傳遞（或）回呼。 和 [服務合約](contract.md) 用來指定服務上公開之端點的服務合約。 下列元件和作業是服務層的一部分：

-   [服務主機](service-host.md)
-   [服務 Proxy](service-proxy.md)
-   [內容](context.md)
-   [合約](contract.md)
-   [服務中繼資料](service-metadata.md)

## <a name="channel-layer"></a>通道層

服務模型建基於通道層，可提供完整的彈性，但更難使用。 下列元件和作業是通道層的一部分：

-   [訊息](message.md)
-   [通道](channel.md)
-   [接聽程式](listener.md)
-   [錯誤](faults.md)
-   [Url](url.md)
-   [安全性](security-overview.md)
-   [中繼資料匯入](metadata-import.md)

## <a name="xml-layer"></a>XML 層

通道層級接著建基於輕量的 XML 架構，包括 C 資料類型的還原序列化。 下列元件和作業是 XML 層的一部分：

-   [XML 寫入器](xml-writer.md)
-   [XML 讀取器](xml-reader.md)
-   [XML 緩衝區](xml-buffer.md)
-   [序列 化](serialization.md)
-   [XML 語言支援](xml-language-support.md)

## <a name="common-to-all-layers"></a>所有層級通用

以下是適用于三個階層中任一層的主題：

-   [錯誤](errors.md)
-   [非同步模型](asynchronous-model.md)
-   [執行緒安全性](thread-safety.md)
-   [追蹤](tracing.md)
-   [取消](cancellation.md)
-   [公用程式](utilities.md)
-   [偵錯](debugging.md)
-   [Wsutil 編譯器工具](wsutil-compiler-tool.md)
-   [堆積](heap.md)

## <a name="examples"></a>範例

如需 API 元素的詳細資訊，請參閱 [Windows Web 服務參考](windows-web-services-reference.md)。 如需使用 API 的範例，請參閱 [使用 Windows Web 服務](using-windows-web-services.md)。

 

 




