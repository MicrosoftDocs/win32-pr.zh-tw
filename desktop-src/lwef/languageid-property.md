---
title: LanguageID 屬性
description: LanguageID 屬性
ms.assetid: f57b0fa1-b3b8-49c8-b441-2a40e564d6ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7a10e6b16f9e35b223bada728871d253685538
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301876"
---
# <a name="languageid-property"></a>LanguageID 屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定字元的語言識別項。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*agent. * * * 字元* * **( "***CharacterID***" ) 。LanguageID** \[  =  *LanguageID*\]



部分

描述

LanguageID

指定字元語言識別項的長整數。 字元的語言識別項 (LANGID) 是由 Windows 定義的16位值，其中包含主要語言識別項和次要語言識別項。 下列範例是 Microsoft Agent 支援之語言的值。 若要判斷其他語言的值，請參閱 *PLATFORM SDK 檔*。

 

阿拉伯文

&H0401

義大利文

&H0410

 

巴斯克文

&H042D

日文

&H0411

 

簡體中文

&H0804

韓文

&H0412

 

繁體中文

&H0404

挪威文

&H0414

 

克羅埃西亞文

&H041A

波蘭文

&H0415

 

捷克文

&H0405

葡萄牙文 (葡萄牙)

&H0816

 

丹麥文

&H0406

葡萄牙文 (巴西)

&H0416

 

荷蘭文

&H0413

羅馬尼亞文

&H0418

 

英文 (英國)

&H0809

俄文

&H0419

 

英文 (美國)

&H0409

斯洛伐克文

&H041B

 

芬蘭文

&H040B

斯洛維尼亞文

&H0424

 

法文

&H040C

西班牙文

&H0C0A

 

德文

&H0407

瑞典文

&H041D

 

希臘文

&H0408

泰文

&H041E

 

Hebrew

&H040D

土耳其文

&H041F

 

匈牙利文

&H040E

 

 



 

</dd> </dl>

## <a name="remarks"></a>備註

如果您未設定字元的 **LanguageID** ，則如果已安裝對應的代理程式語言 DLL，則其語言識別項將會是目前的系統語言識別項，否則，字元的語言會是英文 (US) 。

這個屬性也會決定文字註解文字的語言、字元快顯功能表中的命令，以及語音辨識引擎。 它也會決定 TTS 輸出的預設語言。

如果您嘗試設定字元的 **LanguageID** ，且未安裝該語言的代理程式語言 DLL，或無法使用語言識別項的顯示字型，則代理程式會引發錯誤，而 **LanguageID** 會維持在其最後一個設定。

如果語言沒有相符的語音引擎，則設定這個屬性不會引發錯誤。 若要判斷 **LanguageID** 是否有相容的語音引擎可供使用，請檢查 [**SRModeID**](srmodeid-property.md) 或 [**TTSModeID**](ttsmodeid-property.md)。 如果您未設定 **LanguageID**，則會設定為 [使用者預設語言識別項] 設定。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

> [!Note]  
> 如果您將 **LanguageID** 設定為支援雙向文字 (例如阿拉伯文或希伯來文) 的語言，但是執行應用程式的系統沒有安裝雙向支援，則會以邏輯而非顯示順序來顯示文字。

 

## <a name="see-also"></a>另請參閱

[**SRModeID 屬性**](srmodeid-property.md)， [ **TTSModeID 屬性**](ttsmodeid-property.md)


 

 




