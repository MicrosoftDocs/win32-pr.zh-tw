---
title: IAgentCharacterEx GetTTSModeID
description: IAgentCharacterEx GetTTSModeID
ms.assetid: e7b3c576-dc3c-40de-8d09-8e7f4b79250b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a77e78755345c0993ed5723080b0b3f4b8297a
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104023119"
---
# <a name="iagentcharacterexgetttsmodeid"></a>IAgentCharacterEx::GetTTSModeID

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetTTSModeID(
   BSTR * pbszModeID  // address of TTS engine ID
);
```

抓取為字元設定的 TTS 引擎的模式識別碼。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*
</dt> <dd>

接收字元之 TTS 引擎的模式識別碼設定之 BSTR 的位址。

</dd> </dl>

此設定會針對字元的語音輸出，傳回 (文字轉換語音) 引擎模式識別碼的 TTS。 TTS 引擎的模式識別碼是 GUID 的字串表示， (以大括弧和連字號來格式化，) 由語音廠商所定義，以唯一識別引擎。 如需詳細資訊，請參閱 [Microsoft 語音 SDK 檔](https://msdn.microsoft.com/library/ee705648.aspx)。 如果尚未載入相關聯的引擎，則查詢此屬性會載入相關聯的引擎。

如果您沒有為字元設定 TTS 引擎模式識別碼，伺服器會嘗試傳回符合 (使用 Microsoft 語音 API 介面的引擎，) 字元的編譯的 TTS 設定和字元的目前語言設定。 如果這些不同，則字元的語言設定會覆寫其撰寫的模式設定。 如果您未設定字元的語言設定，則字元的語言會是使用者預設語言識別項，而伺服器會根據該語言識別項來嘗試相符。

如果 [**IAgentAudioObjectProperties：： GetEnabled**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) 傳回 **False**，則此函數不會失敗。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

Microsoft 代理程式的語音引擎需求是以 Microsoft 語音 API 為基礎。 支援 Microsoft 代理程式的 SAPI 需求的引擎可與代理程式一起安裝和使用。

## <a name="see-also"></a>另請參閱

[**IAgentCharacterEx::SetTTSModeID**](iagentcharacterex--setttsmodeid.md)


 

 




