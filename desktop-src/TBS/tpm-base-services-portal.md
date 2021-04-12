---
title: TPM 基本服務
description: TPM 軟體提供服務作為透過遠端程序呼叫所公開的 API。 使用 TPM 來建立 TPM 模組。
ms.assetid: ae6e7fe9-585d-467a-8456-e008b8ea89a0
keywords:
- TPM 基礎服務 TB
- TPM 基礎服務 TB 版，首頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d2cbdfc1f85d6917f2e9a7a5b8e7a0fc25ebdc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376045"
---
# <a name="tpm-base-services"></a>TPM 基本服務

## <a name="purpose"></a>目的

信賴平臺模組 (TPM) 基礎服務 (TB) 功能會跨應用程式集中進行 TPM 存取。

[TB] 功能在 Windows Server 2008、Windows Vista 或更新版本的作業系統中會以系統服務的形式執行。 它會將服務提供給透過遠端程序呼叫（ (RPC) ）公開的 API。 [TB] 功能使用由呼叫應用程式以合作排程 TPM 存取所指定的優先順序。

> [!Note]
>
> TPM 可用於金鑰儲存體作業。 不過，我們鼓勵開發人員改用這些案例的 [金鑰儲存體 api](/windows/desktop/SecCNG/key-storage-and-retrieval) 。 金鑰儲存體 Api 提供的功能，可讓您建立、簽署或加密密碼編譯金鑰，並保存密碼編譯金鑰，而且比起這些目標案例的 TB 更高階且更容易使用。

 

## <a name="developer-audience"></a>開發人員對象

當應用程式開發人員以 Windows 作業系統為基礎時，可使用此 TB。 開發人員應該熟悉 C 和 c + + 程式設計語言和 Microsoft Windows 程式設計環境。

## <a name="run-time-requirements"></a>執行階段需求求

[TB] 功能至少需要 Windows Server 2008 或 Windows Vista 作業系統。 如需特定程式設計專案之執行時間需求的詳細資訊，請參閱該元素之 [參考] 頁面的 [需求] 區段。

## <a name="in-this-section"></a>本節內容



| 主題                                         | 描述                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------|
| [關於 TB](about-tbs.md)<br/>         | 最重要的概念，以及更高階的 TBS 功能觀點。<br/>               |
| [使用 TB](using-tbs.md)<br/>         | 使用 TB API 的最 TB 程式和程式。<br/>                  |
| [TB 參考](tbs-reference.md)<br/> | 有關 TB 函數、結構和傳回碼的檔。<br/> |



 

 

