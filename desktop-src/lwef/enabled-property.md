---
title: 'Enabled 屬性 (Balloon 物件) '
description: 深入瞭解 Enabled Balloon 物件屬性。 Microsoft Agent 已于 Windows 7 淘汰。
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 602d39a9bef7713a92707d8a43050f04a3577b6d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407301"
---
# <a name="enabled-property-balloon-object"></a>Enabled 屬性 (Balloon 物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回是否針對指定的字元啟用文字批註。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "**_CharacterID_*_" ) 的字元。氣球。已啟用_*



| 值     | 描述              |
|-----------|--------------------------|
| **True**  | 批註提示已啟用。  |
| **False** | 批註提示已停用。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

**Enabled** 屬性會傳回布林值，指定是否啟用氣球。 當字元在 Microsoft Agent 字元編輯器中進行編譯時，會將文字氣球預設狀態設定為字元定義的一部分。 如果將字元定義為不支援文字提示字元，則字元的這個屬性一律會是 **False** 。

 

 




