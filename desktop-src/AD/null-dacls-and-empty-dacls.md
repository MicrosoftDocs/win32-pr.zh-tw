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
ms.openlocfilehash: 2b841bb0253547fea291232fb4c9e6e0f3377d18
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933052"
---
# <a name="null-dacls-and-empty-dacls-ad-ds"></a>Null Dacl 和空白的 Dacl (AD DS) 

在任何物件的 [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) 屬性中， (DACL) 的 null 任意存取控制清單是否存在，可能會造成嚴重的安全性風險。 Null DACL 會授與所有要求使用者的完整存取權;對物件而言，不會執行一般的安全性檢查。 Null DACL 不應與空白的 DACL 混淆。 空白的 DACL 是正確配置和初始化的 DACL，其中不包含 (Ace) 的存取控制專案。 空白的 DACL 不會授與指派給它的物件存取權。

如需詳細資訊，請參閱 [Null dacl 和空白的 dacl](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls)。

 

 