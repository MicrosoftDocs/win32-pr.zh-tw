---
title: IAgentCharacterEx SetTTSModeID
description: IAgentCharacterEx SetTTSModeID
ms.assetid: 66ed792a-1693-45dc-b9a8-eebe772c5af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a24195fd177abbde3c6423f966df67ba0faeaf315038d7f8cb0b4ca136f16c3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114718"
---
# <a name="iagentcharacterexsetttsmodeid"></a>IAgentCharacterEx::SetTTSModeID

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT SetTTSModeID(
   BSTR bszModeID  // TTS engine ID
);
```

設定為字元設定的 TTS 引擎的模式識別碼。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*bszModeID*
</dt> <dd>

此字元之 TTS 引擎的模式識別碼設定。

> [!Note]  
> **IAgentCharacterEx：** 如果未安裝 Speech.dll，且您指定的引擎不符合字元的編譯 TTS 模式設定，SetTTSModeID 可能會失敗。

 

</dd> </dl>

此設定會決定字元的朗讀 TTS 輸出的慣用引擎模式。 TTS (文字轉換語音) 引擎的模式識別碼是語音供應商定義的 GUID，可唯一識別引擎的模式 (以大括弧和連字號) 格式化。 如需詳細資訊，請參閱 [Microsoft 語音 SDK 檔](https://msdn.microsoft.com/library/ee705648.aspx)。

如果您設定了 TTS 模式識別碼，它會根據字元編譯的 TTS 模式識別碼、目前的系統語言識別項和字元目前的語言識別項，覆寫伺服器嘗試比對語音引擎。 但是，如果您嘗試在使用者停用 Microsoft Agent 屬性工作表中的語音輸出或未安裝相關聯的引擎時，設定模式識別碼，此呼叫將會失敗。

如果您沒有為字元設定 TTS 引擎模式識別碼，則伺服器會設定符合字元語言設定的引擎， (使用 Microsoft 語音 API 介面) 。 如果尚未載入相關聯的引擎，則設定這個屬性會載入相關聯的引擎。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

Microsoft 代理程式的語音引擎需求是以 Microsoft 語音 API 為基礎。 支援 Microsoft 代理程式的 SAPI 需求的引擎可與代理程式一起安裝和使用。

## <a name="see-also"></a>另請參閱

[**IAgentCharacterEx:GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 




