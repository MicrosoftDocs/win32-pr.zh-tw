---
title: 關於 TB
description: 一種系統服務，可讓您透明共用可信賴平臺模組 (TPM) 資源。
ms.assetid: 5ab3f514-dea9-48f7-97d9-abc774e2a273
keywords:
- TPM 基礎服務 TB、關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a5d40b1fca688676978f274cb976afedb6e6a56
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104185475"
---
# <a name="about-tbs"></a>關於 TB

TPM 基礎服務 (TB) 功能是一種系統服務，可讓您透明共用信賴平臺模組 (TPM) 資源。 它會同時在同一部實體機器上的多個應用程式之間共用 TPM 資源，即使這些應用程式是在不同的虛擬機器上執行也一樣。 從 Windows 8 和 Windows Server 2012 開始，會在所有具有 TPM 的系統上預先安裝 TB。

信賴運算群組 (TCG) 定義了一個可提供密碼編譯功能的可信賴平臺模組，其設計目的是為了在平臺中提供信任。 由於 TPM 是在硬體中執行，因此它具有有限的資源。 TCG 也會定義軟體堆疊，以利用這些資源為應用程式軟體提供受信任的作業。 但是，不會提供與作業系統軟體並存執行 TSS 執行的布建，而作業系統軟體也可能使用 TPM 資源。 TBS 功能可解決此問題，方法是啟用與 TBS 通訊的每個軟體堆疊，以針對可能在電腦上執行的任何其他軟體堆疊使用 TPM 資源檢查。

您可以從取得 TPM 規格和 TCG Software Stack (TSS) 規格 [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/) 。

TBS 會實作為跨進程服務，以接受使用 RPC 服務的命令。 動態連結的程式庫會呈現 C 語言介面，並與「TB」服務進行通訊。

> [!Note]  
> TB 服務只接受來自本機電腦的 RPC 要求。

 

TB 的主要目標是：

-   提供有限 TPM 資源的有效共用，例如金鑰位置、授權會話位置和傳輸位置。
-   在多個 TPM 軟體堆疊實例之間，提供 TPM 資源的優先順序和同步存取。
-   跨電源狀態提供適當的 TPM 資源管理。
-   防止 TPM 軟體堆疊存取應受限制的 TPM 命令，可能是因為平臺限制或系統管理需求。

下圖顯示此 TB 與 TPM 之間的關聯性。

![在核心模式中，在使用者模式與 tpm 之間的 tbs 的關聯性](images/tbs-block-diagram-as11601.png)

 

 




