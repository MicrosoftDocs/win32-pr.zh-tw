---
title: 列舉群組中的成員
description: 瞭解如何列舉 Azure Active Directory 群組中的成員。 群組的成員會儲存在名為 member 的多重值屬性中。
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- 列舉群組中的成員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 916b988cd26ee4df59eaf27cc5ffd690bca1458a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407421"
---
# <a name="enumerating-members-in-a-group"></a>列舉群組中的成員

群組的成員會儲存在名為 **member** 的多重值屬性中。 對於具有小型到中型成員資格的群組，請使用 [**IADsGroup**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) 來取得 [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) 物件的指標，其中包含所有成員的清單。 然後使用 [**IADsMembers：： get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum)取得列舉值物件，您可以用來列舉成員。

如果預期的群組成員資格將是1000或更多成員，請使用範圍，一次取出一個範圍的使用者。 如需使用範圍列舉成員的詳細資訊，請參閱 [列舉包含許多成員的群組](enumerating-groups-that-contain-many-members.md)。

 

 