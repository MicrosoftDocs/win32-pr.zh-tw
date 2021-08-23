---
title: 'Name 屬性 (字元物件) '
description: 深入瞭解字元物件的 Name 屬性。 Microsoft 代理程式已于 Windows 7 淘汰。
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08509d5d2a349c56548259db4846203da6f632ff76c86309db87e6aa90583a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608648"
---
# <a name="name-property-characters-object"></a>Name 屬性 (字元物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定字串，這個字串會指定指定字元的預設名稱。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "**_CharacterID_*_" ) 的字元。名稱_ *  \[  =  *字串*\]



| 部分     | 描述                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| *string* | 字串值，對應到目前語言設定)  (的字元名稱。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

字元的 **名稱** 可能取決於字元的 [**LanguageID**](languageid-property.md) 設定。 一種語言的字元名稱可能不同，或使用不同于另一個語言的字元。 使用 Microsoft Agent 字元編輯器來編譯字元時，會定義特定語言的字元預設 **名稱** 。

避免將字元重新命名，尤其是在其他用戶端應用程式可能使用相同字元的情況下使用。 此外，Agent 會使用字元的 **名稱** 自動建立隱藏和顯示字元的命令。

 

 




