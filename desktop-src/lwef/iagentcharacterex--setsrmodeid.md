---
title: IAgentCharacterEx SetSRModeID
description: IAgentCharacterEx SetSRModeID
ms.assetid: 8f9072ec-1f64-4f5c-972d-cd6799ce028c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7fcfbf4aff25c1af0fbdb1f40471f6b54c4731f22fb2c736da42fe462eb390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750415"
---
# <a name="iagentcharacterexsetsrmodeid"></a>IAgentCharacterEx::SetSRModeID

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT SetSRModeID(
   BSTR bszModeID  // speech recognition engine ID
);
```

設定為字元設定的語音辨識引擎的模式識別碼。

-   傳回 \_ [確定] 表示作業成功。

bszModeID

字元的語音辨識引擎的模式識別碼設定。

此設定會設定字元語音輸入的引擎。 語音辨識引擎的模式識別碼是語音供應商定義的 GUID，可唯一識別引擎的模式 (使用大括弧和連字號) 來格式化。 如需詳細資訊，請參閱 [Microsoft 語音 SDK 檔](https://msdn.microsoft.com/library/ee705648.aspx)。

如果您指定的模式識別碼不符合字元的語言設定，則如果使用者已停用 [Microsoft 代理程式] 屬性工作表中的 [語音辨識] () ，或未安裝引擎，此呼叫將會失敗。 如果您未設定字元的語音辨識引擎模式識別碼，伺服器會將符合字元語言設定的識別碼， (使用 Microsoft 語音 API 介面) 。

在 [代理程式] 屬性工作表中啟用語音輸入時 ([Advanced Character Options]) ，設定此屬性會載入相關聯的引擎 (如果尚未載入) ，然後啟動 [語音服務]。 亦即，接聽鍵可供使用，而且可以顯示接聽提示。  (接聽鍵和接聽提示只會在先進的字元選項中啟用時才會啟用 ) 。不過，如果您在停用語音時查詢屬性，伺服器就不會啟動語音服務。

這個屬性只適用于字元的用戶端;此設定不會反映其他用戶端的其他字元或用戶端字元的設定。

Microsoft 代理程式的語音引擎需求是以 Microsoft 語音 API 為基礎。 支援 Microsoft 代理程式的 SAPI 需求的引擎可與代理程式一起安裝和使用。

## <a name="see-also"></a>另請參閱

[**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md)


 

 




