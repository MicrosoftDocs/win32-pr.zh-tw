---
description: 以下是最常見的 HRESULT 值。 Winerror.h 標頭檔中包含更多的值。
ms.assetid: ce52efc3-92c7-40e4-ac49-0c54049e169f
title: 一般 HRESULT 值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a64d042d9531d026cda548b2a699ed60c0bebd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848664"
---
# <a name="common-hresult-values"></a>一般 HRESULT 值

以下是最常見的 HRESULT 值。 Winerror.h 標頭檔中包含更多的值。

以下是依名稱字母順序列出的值。



| Name            | 描述                         | 值      |
|-----------------|-------------------------------------|------------|
| S \_ 確定           | 作業已順利完成                | 0x00000000 |
| E \_ 中止        | 作業已中止                   | 0x80004004 |
| E \_ ACCESSDENIED | 一般拒絕存取錯誤         | 0x80070005 |
| E \_ 失敗         | 未指定的失敗                 | 0x80004005 |
| E \_ 控制碼       | 不正確控制碼            | 0x80070006 |
| E \_ INVALIDARG   | 一或多個引數無效 | 0x80070057 |
| E \_ NOINTERFACE  | 不支援這類介面         | 0x80004002 |
| E \_ >NOTIMPL      | 未實作                     | 0x80004001 |
| E \_ OUTOFMEMORY  | 無法配置所需的記憶體 | 0x8007000E |
| E \_ 指標      | 不正確指標           | 且顯示0x80004003 |
| E 未 \_ 預期   | 未預期的失敗                  | 0x8000FFFF |



 

以下是依值排序的數值順序中所列的值。



| 值      | 名稱            | 描述                         |
|------------|-----------------|-------------------------------------|
| 0x00000000 | S \_ 確定           | 作業已順利完成                |
| 0x80004001 | E \_ >NOTIMPL      | 未實作                     |
| 0x80004002 | E \_ NOINTERFACE  | 不支援這類介面         |
| 且顯示0x80004003 | E \_ 指標      | 不正確指標           |
| 0x80004004 | E \_ 中止        | 作業已中止                   |
| 0x80004005 | E \_ 失敗         | 未指定的失敗                 |
| 0x8000FFFF | E 未 \_ 預期   | 未預期的失敗                  |
| 0x80070005 | E \_ ACCESSDENIED | 一般拒絕存取錯誤         |
| 0x80070006 | E \_ 控制碼       | 不正確控制碼            |
| 0x8007000E | E \_ OUTOFMEMORY  | 無法配置所需的記憶體 |
| 0x80070057 | E \_ INVALIDARG   | 一或多個引數無效 |



 

 

 



