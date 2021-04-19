---
description: 地區設定 \_ ITIMEMARKPOSN
ms.assetid: 4aef2631-c05b-41e8-8f4d-f40da4143ab4
title: LOCALE_ITIMEMARKPOSN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0182235754d8f5b6b95bad6c58b4fee87d394d4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997287"
---
# <a name="locale_itimemarkposn"></a>地區設定 \_ ITIMEMARKPOSN

指定時間標記字串 (AM 或 PM 是否) 在時間字串之前或之後的規範。 ITimePrefix 登錄值的方式是與舊版 Windows 的相容性。 規範必須有下列其中一個值。 不允許使用者指定的值。 最好讓您的應用程式使用地區設定 [ \_ STIMEFORMAT](locale-stime-constants.md) 常數，而不是地區設定 \_ ITIMEMARKPOSN。



| 值 | 意義        |
|-------|----------------|
| 0     | 使用做為尾碼。 |
| 1     | 使用做為前置詞。 |



 

 

 



