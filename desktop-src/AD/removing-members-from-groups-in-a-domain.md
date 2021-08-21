---
title: 移除網域中群組的成員
description: 您可以從群組中移除使用者、群組或連絡人。
ms.assetid: 036f2882-7da9-4293-87a0-a087235b212f
ms.tgt_platform: multiple
keywords:
- 群組 AD，移除網域中群組的成員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f282cf2938996059ad13fe74bc9818e984967d1c8f3a4dbfffae7b505cbe1b9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025156"
---
# <a name="removing-members-from-groups-in-a-domain"></a>移除網域中群組的成員

您可以從群組中移除使用者、群組或連絡人。 **群組** 物件的 **成員** 屬性包含群組的所有直接成員。

從群組中移除成員最簡單的方法，就是在您想要從中移除成員的群組物件的 [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)介面上，呼叫 [**IADsGroup。**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove)

 

 