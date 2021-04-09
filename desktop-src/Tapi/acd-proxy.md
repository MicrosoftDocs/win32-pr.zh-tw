---
description: 自動呼叫散發 (ACD) server 是一種硬體和軟體的組合，可將撥入電話分類、佇列，並將其散發給代理程式或對線路發出的呼叫。
ms.assetid: 29fb0bd7-0ca9-4490-82d2-39550f00a97b
title: ACD Proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c345fbcac3ac3471098e964336a0c3135fd1f582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944735"
---
# <a name="acd-proxy"></a>ACD Proxy

自動呼叫散發 (ACD) server 是一種硬體和軟體的組合，可將撥入電話分類、佇列，並將其散發給代理程式或對線路發出的呼叫。

伺服器 ACD 應用程式是 TAPI proxy 應用程式，其最高效率應該在與電話語音服務提供者 (TSP) 的相同伺服器上執行。 使用傳統的 ACD 參數，proxy 應用程式會介面切換至交換器的內部 ACD，並公開其作業。 以軟體為基礎或「虛擬」的 ACD proxy 應用程式會完全負責追蹤呼叫、佇列、群組和代理程式，並且會使用標準的 TAPI 介面來控制切換硬體。 代理程式用戶端應用程式通常會在個別代理程式的工作站上執行，並利用 TAPI 遠端服務提供者來與伺服器電腦上的 TAPISRV 進行通訊，因此是 proxy 應用程式。

撥入電話的分類是設計來呼叫能夠有效處理該代理程式的代理程式。 分類可能是以撥號的號碼為基礎， (IVR) 系統或其他準則的互動式語音辨識。 TAPI 使用 [ACD 群組](about-call-center-controls.md) 的概念來代表這項作業。

佇列是一種正常且預期的方式，可讓話務中心處理大量的載入時間。 佇列通常會與 ACD 群組相關聯，但可以建立來處理連出行或等候 IVR 應用程式的連入呼叫。 如需詳細資訊，請參閱 [佇列](about-call-center-controls.md) 。

代理程式或代理程式群組的呼叫散發可能是一致的，但通常是以呼叫資訊、代理程式可用性和能力等資料為基礎。 TAPI 的 [代理程式處理常式](about-call-center-controls.md) 可讓您存取代理程式呼叫的資訊，例如代理程式可用性和位址。

除了基本呼叫分佈之外，ACD 系統還提供管理和報告系統效能的功能。 在呼叫佇列、群組和代理程式上收集的統計資料會用來精簡和強化系統的效能，而且通常會用來做為代理程式 remuneration 的基礎。

 

 



