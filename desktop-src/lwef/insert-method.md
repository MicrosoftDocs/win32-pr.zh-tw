---
title: Insert 方法
description: Insert 方法
ms.assetid: d58cfe50-ace7-4b0f-8539-c2e13a180c96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74eb6d76c1be9b83b7742255ee5a771ed93c64d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966240"
---
# <a name="insert-method"></a>Insert 方法

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

在 **命令** 集合中插入 **Command** 物件。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "*** CharacterID * * *" 的字元 ) 命令。 Insert* *  *Name*， *RefName*， *Before*\_

*標題*、 *語音、啟用、可見*



| 部分      | 描述                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *名稱*    | 必要。 字串值，對應至您指派給 [**命令**](/windows/desktop/lwef/the-command-object)的識別碼。                                                                                                                                                                                               |
| *RefName* | 必要。 字串值，對應至您要插入新命令的上方或下方命令的名稱 (識別碼) 。                                                                                                                                                                 |
| *之前*  | 選擇性。 布林值，指出是否要在 *RefName* 指定的命令之前插入新的命令。 **True** (預設) 。 新的命令會在參考的命令之前插入。<br/> **False** 新的命令會在參考的命令之後插入。<br/> |
| *標題* | 選擇性。 當用戶端應用程式為輸入-主動時，對應至將出現在字元快顯功能表和 [命令] 視窗中之名稱的字串值。 如需詳細資訊，請參閱 [**命令**](/windows/desktop/lwef/the-command-object) 物件的 [**Caption**](caption-property.md)屬性。    |
| *語音*   | 選擇性。 字串值，對應于語音引擎用來辨識此命令的單字或片語。 如需格式化字串替代專案的詳細資訊，請參閱 [**命令**](/windows/desktop/lwef/the-command-object) 物件的 **Voice** 屬性。                                  |
| *Enabled* | 選擇性。 指出是否已啟用命令的布林值。 預設值是 **True**。 如需詳細資訊，請參閱 [**Command**](/windows/desktop/lwef/the-command-object) 物件的 **Enabled** 屬性。                                                                                                  |
| *Visible* | 選擇性。 指出當用戶端應用程式為輸入-主動時，命令視窗中是否顯示命令的布林值。 預設值是 **True**。 如需詳細資訊，請參閱 [**命令**](/windows/desktop/lwef/the-command-object) 物件的 [**Visible**](visible-property.md) 屬性。       |



 

</dd> </dl>

## <a name="remarks"></a>備註

[**命令**](/windows/desktop/lwef/the-command-object)物件的 [[**名稱**](name-property.md)] 屬性值在其 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中必須是唯一的。 您必須先移除 **命令**，才能使用相同的 [**名稱**] 屬性設定來建立新的 **命令**。 嘗試以已存在的 **名稱** 屬性建立 **命令** 會引發錯誤。

這個方法也會傳回 [**Command**](/windows/desktop/lwef/the-command-object) 物件。 這可讓您宣告物件，並在呼叫 **Insert** 方法時將 **命令** 指派給它。


```
   Dim Cmd2 as IAgentCtlCommandEx
   Set Cmd2 = Genie.Commands.Insert ("my second command", "my first command",_ True, "Test", "Test", True, True)
   Cmd2.VoiceCaption = "this is a test"
```



## <a name="see-also"></a>另請參閱

[**Add 方法**](add-method.md)、 [**Remove 方法**](remove-method.md)、 [**RemoveAll 方法**](removeall-method.md)


 

