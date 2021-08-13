---
description: RegisterTypeLibraries 動作會向系統註冊類型程式庫。 此動作會套用至已排程要安裝之 TypeLib 資料表中所參考的每個檔案。
ms.assetid: 374450bb-316c-4fe6-abb1-cd8a8a31f284
title: RegisterTypeLibraries 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac42c831c8413f297d3df2302523a2372b11d1efcffe82ce0d3a82da722832cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626761"
---
# <a name="registertypelibraries-action"></a>RegisterTypeLibraries 動作

RegisterTypeLibraries 動作會向系統註冊類型程式庫。 此動作會套用至已排程要安裝之 [TypeLib 資料表](typelib-table.md) 中所參考的每個檔案。

## <a name="sequence-restrictions"></a>順序限制

RegisterTypeLibraries 動作必須晚于 [InstallFiles](installfiles-action.md) 動作。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                   |
|-------|----------------------------------------------|
| \[1\] | 已註冊類型程式庫的[GUID](guid.md) 。 |



 

## <a name="remarks"></a>備註

RegisterTypeLibraries 動作需要在 TypeLib 資料表的 Language 欄位中正確撰寫型別程式庫語言。 撰寫不正確的語言欄位可能會導致安裝程式無法註冊另一個有效的類型程式庫。

 

 



