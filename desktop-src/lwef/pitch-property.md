---
title: 音調屬性
description: 音調屬性
ms.assetid: 98b2ada3-93c6-4fa1-bf12-353eb229c30c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e346ea0fbb7ebb819d8f00b2fc6aab1ab95e72f391bddc696da18a49f0b2a09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475408"
---
# <a name="pitch-property"></a>音調屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**描述** 
</dt> <dd>

傳回指定字元的語音輸出 (TTS) 音調設定的長整數。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "**_CharacterID_*_" ) 的字元。推銷_*

</dd> </dl>

## <a name="remarks"></a>備註

這個屬性只適用于為 TTS 輸出設定的字元。 如果字元不支援 TTS 輸出，則這個屬性會傳回零 (0) 。

雖然您的應用程式無法寫入此值，但您可以在輸出文字中包含 **Pit** (音調) 標記，以暫時增加特定語句的間距。 不過，使用 **Pit** 標籤來變更間距，並不會變更 [ **音調** ] 屬性設定。 如需詳細資訊，請參閱 [語音輸出標記](pit-tag.md)。

 

 




