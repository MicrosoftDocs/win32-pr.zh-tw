---
title: 內容説明屬性
description: 內容説明屬性
ms.assetid: 18a5fd9b-4ca7-4701-9993-1e0c55f6e232
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d5307abfba0f884261f5b4a21131a75cf87224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673480"
---
# <a name="helpfile-property"></a>內容説明屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定用戶端應用程式所提供之 Microsoft Windows 上下文相關說明檔的路徑和檔案名。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式。***字元 (*** 」CharacterID * * * ) 。* *  \[  =  *檔案名稱*\]



| 部分       | 描述                                                                    |
|------------|--------------------------------------------------------------------------------|
| *檔案名稱* | 字串運算式，指定 Windows 說明檔的路徑和檔案名。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

如果您已為您的應用程式建立 Windows 說明檔，並設定字元的 [協助工具 **] 屬性，** 則當 [**HelpModeOn**](helpmodeon-property.md) 設定為 **True** ，且使用者按一下該字元或從快顯功能表中選取命令時，Agent 會自動呼叫說明。 如果您在所選 [**命令的 [屬性值**](helpcontextid-property.md) ] 屬性中指定內容編號，[說明] 會顯示對應于目前說明內容的主題;否則會顯示「沒有與這個專案相關聯的說明主題」。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

## <a name="see-also"></a>另請參閱

[**HelpModeOn 屬性**](helpmodeon-property.md)， [**屬性內容屬性**](helpcontextid-property.md)


 

 




