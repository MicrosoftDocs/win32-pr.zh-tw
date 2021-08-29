---
title: IdleOn 屬性
description: IdleOn 屬性
ms.assetid: ba436dec-c7b4-42e8-99d6-c6ff93afd73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e08ada4d48197e3090b5fc821b0c5b9f532f47074985218019bb14be8881e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749505"
---
# <a name="idleon-property"></a>IdleOn 屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定布林值，這個值會判斷伺服器是否管理指定字元的 **閒置** 狀態動畫。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "**_CharacterID_*_" ) 的字元。IdleOn_ *  \[  =  *布林值*\]

</dd> </dl> 

| 部分      | 描述                                                                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | 布林運算式，指定伺服器是否管理閒置模式。 **True** (預設為啟用閒置狀態的) 伺服器處理。 <br/> **False** 閒置狀態的伺服器處理已停用。 <br/> |



 

## <a name="remarks"></a>備註

伺服器會在最後一次播放字元的動畫之後自動設定超時時間。 當此計時器的間隔完成時，伺服器會開始一個字元的 **閒置** 狀態，並定期播放其相關聯的 **閒置** 動畫。 如果您想要停用伺服器，使其無法自動播放 **閒置** 狀態動畫，請將屬性設定為 **False** ，然後播放動畫或呼叫 [**Stop**](stop-method.md) 方法。 設定這個值並不會影響目前字元的動畫狀態。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

 

 





