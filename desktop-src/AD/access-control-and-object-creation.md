---
title: 存取控制和物件建立
description: 如果呼叫端沒有 ADS \_ RIGHT \_ DS 在 \_ \_ 父容器上為該物件類型建立子系，Active Directory 伺服器將無法建立子物件。
ms.assetid: 52f56e2a-580c-44b5-ba97-21388f6258bc
ms.tgt_platform: multiple
keywords:
- 存取控制和物件建立廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b99251cd9c9c93177e0b6cfc362c7003078c870e809b48c9aba351e620e1a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118025721"
---
# <a name="access-control-and-object-creation"></a>存取控制和物件建立

如果呼叫端沒有 ADS RIGHT DS 在父容器上為該物件類型 **\_ \_ \_ 建立 \_ 子** 系，Active Directory 伺服器將無法建立子物件。 若要判斷呼叫者可以在目錄物件中建立的子物件類型，請讀取物件的 **allowedChildClassesEffective** 屬性。

當您使用 [**IADsContainer：： create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) 方法來建立子物件時，除非在新的物件上呼叫 [**IADs：： SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) ，否則物件不會成為持續性。 在 **Create** 和 **SetInfo** 呼叫之間，建立執行緒可以將值放入任何新物件的屬性。 在 **SetInfo** 呼叫之後，建立執行緒不一定具有存取權來設定新物件的屬性。 若要確保呼叫端具有這些許可權，請在建立期間指定明確的安全描述項。 DACL 應該有一個 ACE，讓呼叫端具有物件的必要存取權限。

如需存取控制和建立物件的詳細資訊，請參閱 [如何在新的目錄物件上設定安全描述項](how-security-descriptors-are-set-on-new-directory-objects.md)。

 

 