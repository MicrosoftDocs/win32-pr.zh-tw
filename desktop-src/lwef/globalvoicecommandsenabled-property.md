---
title: GlobalVoiceCommandsEnabled 屬性
description: GlobalVoiceCommandsEnabled 屬性
ms.assetid: d4f74019-fa33-41fc-abe7-01791ff188f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f523171187c9956a7741afc0fabcc7ec794071
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933249"
---
# <a name="globalvoicecommandsenabled-property"></a>GlobalVoiceCommandsEnabled 屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定是否已啟用代理程式全域命令的語音。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理。***字元 (*** 」CharacterID * * * ") GlobalVoiceCommandsEnabled**

\[ = *布林*\]



| 部分      | 描述                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | 指出是否已啟用代理程式全域命令之語音參數的布林運算式。 **True** (預設值) 啟用語音參數。 <br/> **False** 語音參數已停用。<br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

Microsoft 代理程式會自動新增語音參數 (文法) 來開啟和關閉 [語音命令] 視窗，以及顯示和隱藏字元。 如果您將 **GlobalVoiceCommandsEnabled** 設定為 **False**，Agent 會停用這些命令的任何語音參數，以及其他用戶端 [**命令**](/windows/desktop/lwef/the-commands-collection-object)物件的 [**標題**](caption-property.md)的語音參數。 這可讓您從用戶端目前的活動文法中排除這些。 不過，因為這可能會封鎖其他用戶端的語音存取，所以在處理使用者的語音輸入之後，請將此屬性重設為 **True** 。

停用此屬性並不會影響該字元的快顯功能表。 伺服器所加入的全域命令仍會出現。 您無法從快顯功能表中移除它們。

 

