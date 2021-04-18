---
title: SRModeID 屬性
description: SRModeID 屬性
ms.assetid: 4c784fc5-d2c2-4e5b-ba5f-f59b4507f40f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898f90a70c29d409eaa12df3d3fde845e35bd5ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106976328"
---
# <a name="srmodeid-property"></a>SRModeID 屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定字元使用的語音辨識引擎。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "*** CharacterID * * *" 的字元 ) 。SRModeID* *  \[  =  *ModeID*\]



| 部分     | 描述                                                             |
|----------|-------------------------------------------------------------------------|
| *ModeID* | 對應至語音引擎之模式識別碼的字串運算式。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

屬性會決定語音輸入的字元所使用的語音辨識引擎。 語音辨識引擎的模式識別碼是由語音供應商定義的格式化字串，可唯一識別引擎。 如需詳細資訊，請參閱 [在程式碼中存取語音引擎](accessing-a-speech-engine-in-your-code.md)。

如果您針對未安裝的語音引擎指定模式識別碼，則如果使用者已停用 [Microsoft 代理程式] 屬性工作表中的 [語音辨識] () ，或是指定之語音引擎的語言不符合字元的 [**LanguageID**](languageid-property.md) 設定，則伺服器會引發錯誤。

如果您查詢此屬性，但尚未成功 () 設定語音辨識引擎，則伺服器會根據字元的 [**LanguageID**](languageid-property.md) 設定，傳回由 SAPI 傳回的引擎模式識別碼。 如果您尚未設定此字元的 **LanguageID**，則 Agent 會根據使用者的預設語言識別項設定，傳回由 SAPI 傳回的引擎模式識別碼。 如果沒有相符的引擎，伺服器會傳回空字串 ( "" ) 。 查詢此屬性不需要該 [**SpeechInput。 Enabled**](https://www.bing.com/search?q=**SpeechInput.Enabled**) 必須設定為 **True**。 但是，如果您在停用語音輸入時查詢屬性，伺服器就會傳回空字串。

啟用語音輸入時 (在 [先進字元選項] 視窗中) ，查詢或設定這個屬性會載入關聯的引擎 (如果尚未載入) ，然後啟動語音服務。 亦即，接聽鍵可供使用，而且可以顯示接聽提示。  (接聽鍵和接聽提示只會在先進的字元選項中啟用時才會啟用 ) 。不過，如果您在停用語音時查詢屬性，伺服器就不會啟動語音服務。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

Microsoft 代理程式的語音引擎需求是以 Microsoft 語音 API 為基礎。 支援 Microsoft 代理程式的 SAPI 需求的引擎可與代理程式一起安裝和使用。

> [!Note]  
> 如果您的系統上未安裝相容的音效支援，這個屬性也會傳回空字串。

 

> [!Note]  
> 查詢此屬性通常不會傳回錯誤。 但是，如果語音引擎的載入異常時間很長，您可能會收到錯誤，指出查詢已超時。

 

## <a name="see-also"></a>另請參閱

[**LanguageID 屬性**](languageid-property.md)


 

 




