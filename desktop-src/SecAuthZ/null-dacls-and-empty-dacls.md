---
description: Null DACL 會授與對要求它的任何使用者的完整存取權。 空白的 DACL 是正確配置且初始化的 DACL，其中不包含任何存取控制專案。 空白的 DACL 不會授與指派給它的物件存取權。
ms.assetid: 26e5c98d-bbdc-4f9f-96e0-18d1c429f1e6
title: 'Null Dacl 和空白的 Dacl (授權) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51c15f9a3aeed120ff91dc19a091232721c623683d90f0c9cdccbc065516eea8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907818"
---
# <a name="null-dacls-and-empty-dacls-authorization"></a>Null Dacl 和空白的 Dacl (授權) 

如果 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) (屬於物件 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 的 DACL) 會設定為 **null**，則會建立 null 的 dacl。 Null DACL 會授與所有要求使用者的完整存取權;對物件而言，不會執行一般的安全性檢查。 Null DACL 不應與空白的 DACL 混淆。 空白的 DACL 是正確配置和初始化的 DACL，其中不包含 (Ace) 的 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) 。 空白的 DACL 不會授與指派給它的物件存取權。

如需如何建立 DACL 的範例，請參閱 [建立 dacl](/windows/desktop/SecBP/creating-a-dacl)。

 

 
