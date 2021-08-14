---
title: 'Stop 方法 (舊版 Windows 環境功能) '
description: Stop 方法
ms.assetid: 68372f72-db9c-447c-a3e4-488940c730d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572a93db5697aaae0dcfed6b45a834323c106bba447d2d9a8e94109f788af25c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745960"
---
# <a name="stop-method-legacy-windows-environment-features"></a>Stop 方法 (舊版 Windows 環境功能) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

停止指定字元的動畫。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "**_CharacterID_*_" ) 的字元。停止_ *  \[ *要求*\]



| 部分      | 描述                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------|
| *要求* | 選擇性。 指定特定動畫呼叫的 [**Request**](/windows/desktop/lwef/the-request-object) 物件。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

若要指定要求參數，您必須建立變數，並指派您要停止的動畫要求。 如果您未設定 **Request** 參數，伺服器會停止該字元的所有動畫，包括已排入佇列的 [**Get**](get-method.md) 呼叫，並清除其動畫佇列，除非該字元目前現正播放 **隱藏** 或 **顯示** 動畫。 這個方法不會停止未排入佇列的 **Get** 呼叫。

若要停止特定動畫或 [**取得**](get-method.md) 呼叫，請宣告物件變數，並將您的動畫要求指派給該變數：


```
   Dim MyRequest
   Dim Genie

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")

   Genie.Get "state", "Showing"
   Genie.Get "animation", "Greet, GreetReturn"

   Genie.Show
   
   'This animation will never play
   Set MyRequest = Genie.Play ("Greet")
   
   Genie.Stop MyRequest
```



這個方法不會產生 [**Request**](/windows/desktop/lwef/the-request-object) 物件。

## <a name="see-also"></a>另請參閱

[**StopAll 方法**](stopall-method.md)


 

 
