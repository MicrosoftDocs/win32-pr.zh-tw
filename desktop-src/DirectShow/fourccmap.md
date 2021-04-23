---
description: FOURCCMap 類別提供 GUID 媒體子類型與舊樣式 FOURCC 32 位媒體標記之間的轉換。
ms.assetid: f77f1da9-34f6-44a0-9f1a-7db2e5a26268
title: FOURCCMap 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap
api_type:
- COM
api_location: ''
ms.openlocfilehash: b9254986bebadeffafaa832817f59194bfc58e12
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908856"
---
# <a name="fourccmap-class"></a>FOURCCMap 類別

![fourccmap 類別階層](images/fourcc01.png)

**FOURCCMap** 類別提供 **GUID** 媒體子類型與舊樣式 **FOURCC** 32 位媒體標記之間的轉換。 在原始的 Windows 多媒體 Api 中，媒體類型已標記為32位值（從 4 8 位字元建立），也稱為 **FOURCC** s。 DirectShow 媒體類型具有子類型的 **GUID**，部分原因在於建立新 **FOURCC** 的 (建立時，必須向 Microsoft) 註冊。 由於 **FOURCC** 是唯一的，因此您可以配置代表 **FOURCC** 的 4000000000 **GUID** 範圍，藉以進行一對一的對應。 此範圍是所有格式的 **GUID**：

`XXXXXXXX-0000-0010-8000-00AA00389B71`

此類別可簡化 **GUID** s 和 **FOURCC** 之間的轉換。 這僅適用于相容性。 建議所有新的媒體子類型都以 Guidgen.exe 或類似工具所建立的 **GUID** 來表示，而不是藉由對應 **FOURCC**。

物件衍生自 **guid**，沒有額外的資料成員，而且可以轉換成 **guid**。 物件可以在結構時間傳遞 **FOURCC** 。 預設的函式會將 **FOURCC** 初始化為零。

[**GetFOURCC**](fourccmap-getfourcc.md)和 [**SetFOURCC**](fourccmap-setfourcc.md)方法不會檢查 **GUID** 的固定部分是否對應到 **FOURCC** 範圍。 因此，如果您將 **guid** 的指標轉換成 **FOURCC** 的指標，然後設定或取得 **FOURCC** 欄位，您也需要另外檢查 **guid** 是否在 **FOURCC** 範圍內。

## <a name="member-functions"></a>成員函數



| 標籤 | 值 |
|------------------------------------------|----------------------------------------------------------|
| [**FOURCCMap**](fourccmap-fourccmap.md) | 函式方法。                                      |
| [**GetFOURCC**](fourccmap-getfourcc.md) | 從 **FOURCCMap** 物件中抓取 **FOURCC** 。    |
| [**SetFOURCC**](fourccmap-setfourcc.md) | 設定 **FOURCCMap** 物件的 **FOURCC** 部分。 |



 

 

 



