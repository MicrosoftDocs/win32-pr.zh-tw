---
title: TTSModeID 屬性
description: TTSModeID 屬性
ms.assetid: 9205c37e-e006-466a-9b33-b98408c01ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a720b06362b77418434669146a0d89dea8afd37d7a44c4079b2e12c24fcd2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607958"
---
# <a name="ttsmodeid-property"></a>TTSModeID 屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定用於字元的 TTS 引擎模式。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "**_CharacterID_*_" ) 的字元。TTSModeID_ *  \[  =  *ModeID*\]



| 部分     | 描述                                                             |
|----------|-------------------------------------------------------------------------|
| *ModeID* | 對應至語音引擎之模式識別碼的字串運算式。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

這個屬性會針對字元的讀出輸出，判斷 (文字轉換語音) 引擎模式識別碼的 TTS。 TTS 引擎的模式識別碼是由語音供應商定義的格式化字串，可唯一識別引擎的模式。 如需詳細資訊，請參閱 [在程式碼中存取語音引擎](accessing-a-speech-engine-in-your-code.md)。

設定這個屬性會覆寫伺服器嘗試載入以該字元編譯之 TTS 設定為基礎的引擎，以及字元目前的 [**LanguageID**](languageid-property.md) 設定。 但是，如果您針對未安裝的引擎指定模式識別碼，或使用者已在 Microsoft Agent 屬性工作表中停用語音輸出 (**AudioOutput。 Enabled = False**) ，伺服器會引發錯誤。

如果您未 (或未成功) 為字元設定 TTS 模式識別碼，伺服器會檢查字元的已編譯 TTS 模式設定是否符合字元的 [**LanguageID**](languageid-property.md) 設定，以及是否已安裝相關聯的 tts 引擎。 如果是，則為讀出字元輸出的字元所使用的 TTS 模式，而這個屬性會傳回該模式識別碼。 如果不是，伺服器會要求相容的 SAPI 語音引擎，該引擎會符合字元的 **LanguageID** ，以及字元的已編譯模式識別碼的性別和年齡組。 如果您未設定字元的 **LanguageID**，則其 **LanguageID** 為目前的使用者語言。 如果找不到相符的引擎，則查詢此屬性會傳回引擎模式識別碼的空字串。 同樣地，如果您在使用者已停用 Microsoft Agent 屬性工作表中的語音輸出時查詢此屬性 (**AudioOutput。 Enabled = False**) ，此值將會是空字串。

如果尚未載入關聯的引擎，則查詢或設定這個屬性會將其載入 (（如果尚未載入）) 。 但是，如果已安裝字元編譯的 TTS 設定中指定的引擎，並且符合字元的語言識別項設定，則會在載入字元時載入引擎。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

Microsoft 代理程式的語音引擎需求是以 Microsoft 語音 API 為基礎。 支援 Microsoft 代理程式的 SAPI 需求的引擎可與代理程式一起安裝和使用。

> [!Note]  
> 如果您的系統上未安裝相容的音效支援，這個屬性也會傳回空字串。

 

> [!Note]  
> 如果未安裝 Speech.dll，且您指定的引擎不符合字元的編譯 TTS 模式設定，則設定 **TTSModeID** 可能會失敗。

 

> [!Note]  
> 查詢此屬性通常不會傳回錯誤。 但是，如果語音引擎的載入異常時間很長，您可能會收到錯誤，指出查詢已超時。

 

## <a name="see-also"></a>另請參閱

[**LanguageID 屬性**](languageid-property.md)


 

 




