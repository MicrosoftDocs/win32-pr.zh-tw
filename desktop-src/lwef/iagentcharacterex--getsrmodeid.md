---
title: IAgentCharacterEx GetSRModeID
description: IAgentCharacterEx GetSRModeID
ms.assetid: 28049680-8245-49f3-9ecd-13c7605f10ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0bba237fb1bc1b5d769f7e8ecf983b58718c18e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "103681487"
---
# <a name="iagentcharacterexgetsrmodeid"></a>IAgentCharacterEx::GetSRModeID

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetSRModeID(
   BSTR * pbszModeID  // address of speech recognition engine ID
);
```

抓取為字元設定的語音辨識引擎的模式識別碼。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*
</dt> <dd>

接收字元的語音辨識引擎模式識別碼設定之 BSTR 的位址。

</dd> </dl>

此設定會傳回針對字元的語音輸入所設定的引擎。 語音辨識引擎的模式識別碼是 GUID (格式的字串表示，並以大括弧和連字號) ，由語音供應商唯一識別引擎。 如需詳細資訊，請參閱 [Microsoft 語音 SDK 檔](https://msdn.microsoft.com/library/ee705648.aspx)。

如果您未設定字元的語音辨識引擎模式識別碼，伺服器會傳回符合字元語言設定的引擎， (使用 Microsoft 語音 API 介面) 。 如果字元沒有相符的語音辨識引擎可供使用，則伺服器會傳回 null (空白的) 字串。

啟用語音輸入時 (在 [先進字元選項] 視窗中) ，查詢或設定這個屬性會載入關聯的引擎 (如果尚未載入) ，然後啟動語音服務。 亦即，接聽鍵可供使用，而且可以顯示接聽提示。  (接聽金鑰和接聽提示只會在先進的字元選項中啟用時才會啟用 ) 。不過，如果您在停用語音時查詢屬性，伺服器就不會啟動語音服務，且會傳回 null 字串 (空白字串) 。

此函數只會傳回用戶端應用程式使用字元的設定;此設定不會反映用戶端應用程式中其他字元或其他字元的用戶端。

如果 [**IAgentSpeechInputProperties：： GetEnabled**](iagentspeechinputproperties--getenabled.md) 傳回 **False**，則此函數不會失敗。

Microsoft 代理程式的語音引擎需求是以 Microsoft 語音 API 為基礎。 支援 Microsoft 代理程式的 SAPI 需求的引擎可與代理程式一起安裝和使用。

## <a name="see-also"></a>另請參閱

[**IAgentCharacterEx::SetSRModeID**](iagentcharacterex--setsrmodeid.md)


 

 




