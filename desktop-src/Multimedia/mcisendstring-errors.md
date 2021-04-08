---
title: mciSendString 錯誤
description: mciSendString 錯誤
ms.assetid: 286102bd-fcf3-425b-9adc-e0ca2d62e453
keywords:
- MCIERR 傳回值，mciSendString 錯誤
- 多媒體參考，mciSendString 錯誤
- 多媒體、mciSendString 錯誤的參考
- 媒體控制介面 (MCI) ，mciSendString 錯誤
- MCI (媒體控制介面) ，mciSendString 錯誤
- MCI、mciSendString 錯誤的參考
- MCI 參考，mciSendString 錯誤
- 媒體控制介面 (MCI) ，錯誤
- MCI (媒體控制介面) ，錯誤
- MCI 的參考，錯誤
- MCI 參考，錯誤
- mciSendString 錯誤
- mciSendString 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063db1986d3bff2416ad17886afb3b6281e20165
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842216"
---
# <a name="mcisendstring-errors"></a>mciSendString 錯誤

[**MciSendString**](/previous-versions//dd757161(v=vs.85))函式會傳回下列錯誤，但不會由 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))傳回：



| 值                             | 意義                                           |
|-----------------------------------|---------------------------------------------------|
| MCIERR \_ 錯誤 \_ 常數             | 為參數指定的值不明。   |
| MCIERR \_ 錯誤的 \_ 整數              | 命令中的整數無效或遺失。 |
| MCIERR \_ 重複的 \_ 旗標          | 指定了兩次旗標或值。              |
| MCIERR \_ 遺失 \_ 命令 \_ 字串  | 未指定任何命令。                         |
| MCIERR \_ 遺失的 \_ 裝置 \_ 名稱     | 未指定任何裝置名稱。                     |
| MCIERR \_ 遺漏 \_ 字串 \_ 引數 | 命令中遺漏字串值。      |
| MCIERR \_ 新的 \_ 需要 \_ 別名      | 別名必須與「新的」裝置名稱一起使用。 |
| MCIERR \_ 沒有 \_ 右 \_ 引號        | 遺漏右引號。              |
| MCIERR \_ \_ 在 \_ 自動 \_ 開啟時通知    | 「通知」旗標在自動開啟時不合法。      |
| MCIERR \_ 參數 \_ 溢位           | 輸出字串的長度不足。            |
| MCIERR 剖析器 \_ \_ 內部          | 發生內部剖析器錯誤。                |
| MCIERR \_ 無法辨識的 \_ 關鍵字     | 指定了未知的命令參數。       |



 

 

 