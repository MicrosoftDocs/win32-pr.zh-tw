---
title: 'Null Dacl 和空白的 Dacl (AD DS) '
description: 在任何物件的 nTSecurityDescriptor 屬性中， (DACL) 的 null 任意存取控制清單是否存在，可能會造成嚴重的安全性風險。
ms.assetid: 32b786d2-e676-4402-ad22-550de9289494
ms.tgt_platform: multiple
keywords:
- Null Dacl 和空白的 Dacl AD
- Dacl AD、Null 和空白
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a41e03917c1190b7926eca11db038e2143bcb91d142e0617d143d4d80bb6e601
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185793"
---
# <a name="null-dacls-and-empty-dacls-ad-ds"></a>Null Dacl 和空白的 Dacl (AD DS) 

在任何物件的 [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) 屬性中， (DACL) 的 null 任意存取控制清單是否存在，可能會造成嚴重的安全性風險。 Null DACL 會授與所有要求使用者的完整存取權;對物件而言，不會執行一般的安全性檢查。 Null DACL 不應與空白的 DACL 混淆。 空白的 DACL 是正確配置和初始化的 DACL，其中不包含 (Ace) 的存取控制專案。 空白的 DACL 不會授與指派給它的物件存取權。

如需詳細資訊，請參閱 [Null dacl 和空白的 dacl](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls)。

 

 