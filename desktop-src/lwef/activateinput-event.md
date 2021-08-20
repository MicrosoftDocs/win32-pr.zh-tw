---
title: ActivateInput 事件
description: ActivateInput 事件
ms.assetid: bc395750-5da0-4379-8eca-3195e936052c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db21d605a014002063a7c5aa42554a06adb1ed35296242944de789daeb3155c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610678"
---
# <a name="activateinput-event"></a>ActivateInput 事件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

當用戶端變成輸入主動時發生。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

**Sub** *Agent* \_ ActivateInput **(ByVal** *CharacterID * * * )**



| 部分          | 描述                                                                    |
|---------------|--------------------------------------------------------------------------------|
| *CharacterID* | 傳回用戶端變成輸入活動的字元識別碼。 |



 

</dd> </dl>

### <a name="remarks"></a>備註

輸入-主動用戶端會接收伺服器所提供的滑鼠和語音輸入事件。 伺服器只會將此事件傳送給變成進入主動輸入的用戶端。

當使用者切換至您的 [命令](the-command-object.md) 物件（例如，在 [命令] 視窗中選擇命令物件專案，或在字元的快顯功能表中選擇）時，就會發生此事件。 當使用者選取字元 (時，也可能會發生此問題，方法是按一下或說出其名稱) 、當字元變成可見時，以及其他用戶端應用程式的字元變成隱藏時。 您也可以呼叫 [啟動方法](activate-method.md) (，將 **狀態** 設定為 2) 以明確地將字元設為最上層，這會導致您的用戶端應用程式變成輸入主動，並觸發此事件。 但是，如果您只使用 Activate 方法方法來指定用戶端是否為字元的作用中用戶端，就不會發生此事件。

### <a name="see-also"></a>另請參閱

[**DeactivateInput** 事件](deactivateinput-event.md)， [ **Activate** 方法](activate-method.md)


 

 




