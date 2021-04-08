---
title: State 屬性
description: State 屬性會在某個時間點描述物件的狀態。 所有物件都支援 State 屬性。
ms.assetid: 6a56070f-7913-45b2-b693-3c0a8b7fa2f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151f09fca6c31abaaa98a19139d3e22eb28ec90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840744"
---
# <a name="state-property"></a>State 屬性

**State** 屬性會在某個時間點描述物件的狀態。 所有物件都支援 **State** 屬性。

藉由呼叫 [**IAccessible：： get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)，即可抓取 **State** 屬性。

Microsoft Active Accessibility 提供在 oleacc 中定義的 [物件狀態常數](object-state-constants.md)，這些常數會合並以識別物件的狀態。 建議伺服器開發人員使用這些預先定義的狀態值。 如果傳回預先定義的狀態值，用戶端會使用 [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) 來取出描述狀態的當地語系化字串。

偶而動畫的圖形應該將 [ **狀態** ] 屬性設定為 [ [**狀態 \_ 系統 \_ 動畫**](object-state-constants.md) ]，並將 [ [**角色**](role-property.md) ] 屬性設定為 [ [**角色 \_ 系統 \_ 圖形**](object-roles.md)]。

 

 




