---
title: 速度屬性
description: 速度屬性
ms.assetid: 43d0480b-d3a5-4992-a2a5-80eba37221e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaca342dde91965ab381f95671a39c4ba9fdcae040835f09867b3fabf5899a6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745950"
---
# <a name="speed-property"></a>速度屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回長整數，指定字元語音輸出的目前速度。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "**_CharacterID_*_" ) 的字元。速度_*

</dd> </dl>

## <a name="remarks"></a>備註

這個屬性會傳回字元的目前說話輸出速度設定。 針對使用 TTS 輸出的字元，屬性會傳回字元的實際 TTS 輸出設定。 如果未啟用 TTS 或字元不支援 TTS 輸出，此設定會反映輸出速度的使用者設定。

雖然您的應用程式無法寫入此值，但您可以在輸出文字中包含 **Spd** (速度) 標記，以暫時加速特定語句的輸出。 不過，使用 **Spd** 標記變更字元的讀出輸出並不會影響 **速度** 屬性設定。 如需詳細資訊，請參閱 [語音輸出標記](microsoft-agent-speech-output-tags.md)。

 

 




