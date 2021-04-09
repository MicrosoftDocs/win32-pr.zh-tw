---
title: 網路原則伺服器擴充功能
description: NPS 擴充功能 API 可讓軟體發展人員撰寫可用於驗證、授權和帳戶處理的擴充 Dll。 NPS 擴充功能 API 支援遠端驗證撥入消費者服務 (RADIUS) 通訊協定。
ms.assetid: f459025f-fe5e-4ffa-a651-c70a4f8234ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd6f9bd0be7479726110b41d6060a7e5c836bb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933466"
---
# <a name="network-policy-server-extensions"></a>網路原則伺服器擴充功能

> [!Note]  
> 從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。 本主題的內容適用于 IAS 和 NPS。 在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。

 

NPS 擴充功能 API 可讓軟體發展人員撰寫可用於驗證、授權和帳戶處理的擴充 Dll。 NPS 擴充功能 API 支援遠端驗證撥入消費者服務 (RADIUS) 通訊協定。

使用 NPS 擴充功能 API 所執行的延伸模組 Dll 可以提供增強的會話控制和帳戶處理。 您可以使用這些 Dll 來控制使用者網路會話的數目、使用狀態伺服器，以及連接到網域驗證資料庫和 Active Directory 服務等案例。 擴充 Dll 可以擴充 NPS 提供的遠端存取授權，方法是在將接受回應傳送回驗證用戶端時，新增自己的授權。

NPS 擴充功能 API 適用于任何運算環境，可改善透過遠端伺服器驗證撥入使用者的效率。 這項技術特別適合 (Isp) 的網際網路服務提供者。

## <a name="in-this-section"></a>本節內容

[概觀](/windows/desktop/Nps/ias-about-internet-authentication-service)

RADIUS 和 NPS 擴充功能 API 的一般資訊。

[使用](/windows/desktop/Nps/ias-using-internet-authentication-service)

示範如何使用 NPS 擴充功能 API 的範例程式碼。

[參考](/windows/desktop/Nps/ias-internet-authentication-service-reference)

組成 NPS 擴充功能 API 的列舉類型、函式和結構的檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[網路原則伺服器 (網際網路驗證服務) ](portal.md)
</dt> <dt>

[可延伸的驗證通訊協定 (EAP)](../eap/eap-start-page.md)
</dt> </dl>

 

 