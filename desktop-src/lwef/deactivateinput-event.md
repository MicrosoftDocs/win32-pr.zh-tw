---
title: DeactivateInput 事件
description: DeactivateInput 事件
ms.assetid: 59747932-82be-45d5-8465-73798904e8a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b2fe1ff13b599fe5fbcf2dac22e548a0432f415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932336"
---
# <a name="deactivateinput-event"></a>DeactivateInput 事件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

當用戶端變成非輸入-主動時發生。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

**子***代理程式 * * * \_ DeactivateInput* *  **(ByVal** *CharacterID * * * )**



| 部分          | 描述                                                                    |
|---------------|--------------------------------------------------------------------------------|
| *CharacterID* | 傳回讓用戶端變成非輸入-主動的字元識別碼。 |



 

</dd> </dl>

### <a name="remarks"></a>備註

非輸入-主動用戶端不再接收來自伺服器 (的滑鼠或語音事件，除非它再次變成) 的輸入活動。 伺服器只會將此事件傳送給變成非輸入-主動的用戶端。

當您的用戶端應用程式為輸入-主動，且使用者在字元的快顯功能表或 [語音命令] 視窗中選擇另一個用戶端的標題，或是您呼叫 [**Activate**](activate-method.md) 方法並將 **State** 參數設定為0時，就會發生此事件。 當使用者按一下或說話來選取其他字元的名稱時，也可能會發生此問題。 當您隱藏字元或顯示其他字元時，也會收到此事件。

### <a name="see-also"></a>另請參閱

[**ActivateInput 事件**](activateinput-event.md)


 

 




