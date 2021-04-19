---
title: Role 屬性
description: Role 屬性描述物件的使用者介面元素。 所有物件都支援 Role 屬性。
ms.assetid: f6abf95b-a77a-406d-9ca0-4663adc8245f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f2b285d9242542f83c6b4478df93e888a7a23cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106996146"
---
# <a name="role-property"></a>Role 屬性

**Role** 屬性描述物件的使用者介面元素。 所有物件都支援 **Role** 屬性。

在許多情況下，物件的角色很明顯。 例如，windows 具有 [**角色 \_ 系統 \_ 視窗**](object-roles.md) 角色，而推送按鈕具有 [**角色 \_ 系統 \_ 按鈕**](object-roles.md) 角色。

藉由呼叫 [**IAccessible：： get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)來抓取 **Role** 屬性。

## <a name="identifying-an-objects-role"></a>識別物件的角色

Microsoft Active Accessibility 提供定義于 oleacc 中的 [角色常數](object-roles.md)，用以識別通用物件角色。 建議伺服器開發人員使用這些預先定義的角色值。 如果傳回預先定義的角色常數，用戶端會使用 [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) 函式來取得描述角色的當地語系化字串。

針對動畫控制項（例如複製檔案時顯示的動畫控制項），請使用 [**角色 \_ 系統 \_ 動畫**](object-roles.md)。 偶爾動畫的圖形會描述為 [**角色 \_ 系統 \_ 圖形**](object-roles.md) ，其 [**狀態**](state-property.md) 屬性會設定為「 [**狀態 \_ 系統 \_ 動畫**](object-state-constants.md)」。

請注意，某些角色並不容易描述。 例如，資料夾的大圖示視圖允許任意排列圖示，因此其角色可以描述為 [**角色 \_ 系統 \_ 群組**](object-roles.md)。 或者，提供固定資料列和資料行中之專案的控制項可能具有 [**角色 \_ 系統 \_ 資料表**](object-roles.md) 角色。 因為角色是用來將使用模型傳達給終端使用者，所以請務必使用適當的角色。 例如，如果您的控制項如同按鈕，則使用 [ [**角色 \_ 系統 \_**](object-roles.md)] 按鈕。

 

 




