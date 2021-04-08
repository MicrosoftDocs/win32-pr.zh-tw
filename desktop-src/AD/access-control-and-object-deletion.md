---
title: 存取控制和物件刪除
description: Active Directory 可讓您刪除物件，如果您有權刪除對物件或 ADS 的存取權，您可以刪除 \_ \_ \_ \_ 父容器上物件類型的子系。
ms.assetid: 87027c25-e3c9-4bad-8df3-cb6205e40ef6
ms.tgt_platform: multiple
keywords:
- 存取控制和物件刪除 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bddcd2b563e144743689f2a26c17bd417db14ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681626"
---
# <a name="access-control-and-object-deletion"></a>存取控制和物件刪除

如果您有下列其中一個存取權限，Active Directory Domain Services 可讓您刪除物件：

-   刪除物件本身的存取權
-   ADS \_ RIGHT \_ DS \_ \_ 會刪除父容器上該物件類型的子存取

請注意，系統會在拒絕刪除之前，先驗證物件及其父系的安全描述項。 這表示如果使用者已刪除父系的子系存取權，則明確拒絕使用者刪除存取權的 ACE 將沒有任何作用 \_ 。 同樣地， \_ 如果物件本身允許刪除存取權，就可以覆寫在父系上拒絕刪除子存取的 ACE。

若要執行樹狀結構刪除作業（例如使用 [**IADsDeleteOps：:D eleteobject**](/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject) 方法），您必須擁有 \_ \_ \_ 該物件的 ADS 正確 DS 刪除 \_ 樹狀結構存取權。 如果您有這個存取權限，就可以刪除該物件和任何子物件，不論子物件上的保護為何。 如果您沒有 ADS \_ RIGHT DS delete tree 存取權來刪除樹狀結構 \_ \_ \_ ，則必須以遞迴方式跨越樹狀結構，並個別刪除每個物件。 在此情況下，您必須對樹狀結構中的每個物件具有必要的刪除或刪除 \_ 子存取權。

> [!WARNING]
> 如果使用者的 ADS 具有 \_ 適當的 \_ DS \_ 刪除 \_ 樹狀結構存取權，這讓他們能夠刪除整個子樹，包括所有子物件。 基於這個理由，您可以考慮撤銷父容器上所有使用者的「刪除子樹」存取權限。

 

 

 