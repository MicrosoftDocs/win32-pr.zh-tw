---
title: EAP 常見問題
description: 尋找有關 EAP Api (常見問題) 常見問題的解答，例如「EAP 驗證的存留期為何？」。
ms.assetid: 4e26df7b-3cce-4522-ab39-e24f06b4c4b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93a8b424ed195d30621c67007fc8e7d1a0882bae6ce676c70a1ca0dc93e8b846
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978528"
---
# <a name="eap-frequently-asked-questions"></a>EAP 常見問題

下列主題提供 EAP Api 常見問題的解答。



| 問題                                                                                        | Answer                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EAP 驗證的存留期為何？                                                  | 在一般情況下，驗證是由呼叫 [**RapEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) 和 [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) 函數之間發生的所有專案所組成。 當使用者選擇在 RRAS 嵌入式管理單元中設定 EAP 提供者時，驗證是由呼叫 [**Initialize 和 Initialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-initialize) [**方法之間**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize) 發生的所有專案所組成。<br/> |
| 什麼是「群組原則」？                                                                         | 如需群組原則的說明，請參閱 [群組原則收集](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10))。                                                                                                                                                                                                                                                                                                                                                    |
| EAP 函數是否可以覆寫群組原則所指定的設定原則？                      | 否，永不。 如果群組原則已在使用中，群組原則設定一律會覆寫 EAP 配置設定。                                                                                                                                                                                                                                                                                                                                                         |
| 我需要警告使用者有不正確 PIN 嘗試次數。 是否可以捕獲不正確 pin 碼？ | 當使用者輸入錯誤的 PIN 時，可延伸驗證 Protocol-Transport 層安全性 (EAP-TLS) 會將錯誤碼傳送給 VPN 要求者。 傳回錯誤碼之後，要求者可以執行其慣用的重試邏輯。                                                                                                                                                                                                                    |
| 什麼是 EAP-Transport 層級的安全性 (EAP-TLS) ？                                                 | EAP-TLS 是一種用戶端-伺服器通訊協定，其中的相異憑證設定檔通常用於用戶端和伺服器。如需詳細資訊，請參閱 [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10))。<br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用可延伸的驗證通訊協定](using-extenstible-authentication-protocol.md)
</dt> </dl>