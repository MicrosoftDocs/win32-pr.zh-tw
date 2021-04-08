---
title: 判斷使用者或群組在群組中的成員資格
description: IADsGroup. IsMember 方法可以用來判斷物件是否為群組的成員。
ms.assetid: c7168781-4ae4-4ce3-8d8a-2eefc7def62b
ms.tgt_platform: multiple
keywords:
- 判斷使用者或群組在群組 AD 中的成員資格
- 群組 AD，判斷使用者或群組在群組中的成員資格
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b520146079fdfaa5fa1adc99975b3b25d2e78c05
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023255"
---
# <a name="determining-a-users-or-groups-membership-in-a-group"></a>判斷使用者或群組在群組中的成員資格

[**IADsGroup. IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember)方法可以用來判斷物件是否為群組的成員。 如果指定的物件是群組的直接成員，也就是群組的成員屬性包含指定的物件，則這個方法會傳回 **TRUE** 。

群組可以包含其他群組。 [**IADsGroup. IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember)方法不會以遞迴方式驗證其成員屬性中的群組成員、這些群組內的群組等等。 若要以遞迴方式確認物件是群組的成員、列舉成員屬性中的群組、驗證這些群組的成員，以查看該物件是否為成員，以及這些群組是否包含其他群組，請檢查其成員等等。

> [!Note]  
> 因為群組可以進行嵌套，所以群組成員資格可能會有迴圈。 任何列舉超過許多群組的腳本，如果已經造訪過群組，就應該將群組的內部清單保留為結束遞迴。

 

 

 