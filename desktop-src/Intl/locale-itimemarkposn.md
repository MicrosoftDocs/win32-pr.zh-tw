---
description: 地區設定 \_ ITIMEMARKPOSN
ms.assetid: 4aef2631-c05b-41e8-8f4d-f40da4143ab4
title: LOCALE_ITIMEMARKPOSN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802da8f3d1029dd42c14eb536175d16e897d34a11edbd6be0bfe4f30d44c42db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106457"
---
# <a name="locale_itimemarkposn"></a>地區設定 \_ ITIMEMARKPOSN

指定時間標記字串 (AM 或 PM 是否) 在時間字串之前或之後的規範。 登錄值的 iTimePrefix 與舊版 Windows 的相容性。 規範必須有下列其中一個值。 不允許使用者指定的值。 最好讓您的應用程式使用地區設定 [ \_ STIMEFORMAT](locale-stime-constants.md) 常數，而不是地區設定 \_ ITIMEMARKPOSN。



| 值 | 意義        |
|-------|----------------|
| 0     | 使用做為尾碼。 |
| 1     | 使用做為前置詞。 |



 

 

 



