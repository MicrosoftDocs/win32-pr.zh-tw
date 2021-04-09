---
title: 新增方法
description: 新增方法
ms.assetid: dd258294-33d6-45f5-a6a1-a3a56b12a7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4527dec6014c93bb02b4f080e032266ea40159e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021336"
---
# <a name="add-method"></a>新增方法

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

將 [命令](the-command-object.md) 物件加入至 [命令](the-commands-collection-object.md) 集合。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "*** CharacterID * * *" 的字元 ) 命令。新增* *  *名稱*、*標題*、*語音*、*啟用*、*可見*



| 部分      | 描述                                                                                                                                                                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *名稱*    | 必要。 字串值，對應至您為命令指派的識別碼。                                                                                                                                                                                                                                        |
| *標題* | 選擇性。 當用戶端應用程式為輸入-主動時，對應至將出現在字元快顯功能表和 [命令] 視窗中之名稱的字串值。 如需詳細資訊，請參閱 [命令](the-command-object.md) 物件的 [Caption](caption-property.md) 屬性。                       |
| *語音*   | 選擇性。 字串值，對應于語音引擎用來辨識此命令的單字或片語。 如需格式化字串替代專案的詳細資訊，請參閱 [命令](the-command-object.md) 物件的 [Voice](voice-property.md) 屬性。                                |
| *Enabled* | 選擇性。 指出是否已啟用命令的布林值。 預設值是 **True**。 如需詳細資訊，請參閱 [Command](the-command-object.md) 物件的 [Enabled](enabled-property.md) 屬性。                                                                                              |
| *Visible* | 選擇性。 布林值，指出當用戶端應用程式為輸入-主動時，命令是否會顯示在字元的快顯功能表中。 預設值是 **True**。 如需詳細資訊，請參閱 [命令](the-command-object.md) 物件的 [Visible](visible-property.md) 屬性。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

[命令](the-command-object.md)物件的 [[名稱](name-property.md)] 屬性值在其[命令](the-commands-collection-object.md)集合中必須是唯一的。 您必須先移除命令，才能使用相同的 [名稱] 屬性設定來建立新的命令。 嘗試以已存在的名稱屬性建立命令會引發錯誤。

這個方法也會傳回 [Command](the-command-object.md) 物件。 這可讓您在呼叫 .Validator.addmethod 時宣告物件，並將命令指派給它。


```
   Dim Cmd1 as IAgentCtlCommandEx
   Set Cmd1 = Genie.Commands.Add ("my first command", "Test", "Test", True, True)
   Cmd1.VoiceCaption = "this is a test"
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Insert 方法**](insert-method.md)
</dt> <dt>

[**RemoveAll 方法**](removeall-method.md)
</dt> <dt>

[**Remove 方法**](remove-method.md)
</dt> </dl>

 

 




